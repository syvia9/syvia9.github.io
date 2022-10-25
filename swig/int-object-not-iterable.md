方法的多重赋值会导致TypeError:Int在Python中不可编辑
/big_share2/pacific/user/yaliuliu/sdkmas/driver/shared/test/api/pfc/pfc_watchdog.py
state, pfc_rx = mac_port.get_pfc_queue_state(self.tc_value)

-I-MAC_PORT-1- mac_port la_mac_port_base(oid=540)#SerDes 2/0/4# changed state to UP
-I-MAC_PORT-1- mac_port la_mac_port_base(oid=606)#SerDes 3/1/8# changed state to UP
s  
--Call--  
> /big_share2/pacific/user/yaliuliu/sdkmas/driver/gibraltar/out/opt3-debug/pylib/leaba/hldcli.py(19602)get_pfc_queue_state()  
-> def get_pfc_queue_state(self, *args):  
(Pdb) n  
> /big_share2/pacific/user/yaliuliu/sdkmas/driver/gibraltar/out/opt3-debug/pylib/leaba/hldcli.py(19603)get_pfc_queue_state()  
-> return _hldcli.la_mac_port_get_pfc_queue_state(self, *args)  
(Pdb) s  
--Return--  
> /big_share2/pacific/user/yaliuliu/sdkmas/driver/gibraltar/out/opt3-debug/pylib/leaba/hldcli.py(19603)get_pfc_queue_state()->0  
-> return _hldcli.la_mac_port_get_pfc_queue_state(self, *args)  
(Pdb) s  
***TypeError: 'int' object is not iterable***  
> /big_share2/pacific/user/yaliuliu/sdkmas/driver/shared/test/api/pfc/pfc_watchdog.py(88)watchdog_test()  
-> state, pfc_rx = mac_port.get_pfc_queue_state(self.tc_value)  


root cause:
there are two defines of get_pfc_queue_state  in the sdk:
    la_status get_pfc_queue_state(la_pfc_priority_t pfc_priority, pfc_queue_state_e& out_state) override;
    la_status get_pfc_queue_state(la_pfc_priority_t pfc_priority, pfc_queue_state_e& out_state, bool& out_pfc_rx) override;
in the swig:
    OUTARG_ENUM_TYPEMAPS(silicon_one::la_mac_port::pfc_queue_state_e, out_state)
    OUTARG_BOOL_TYPEMAPS(out_pfc_rx)
swig_wrap.cxx:


SWIGINTERN PyObject *_wrap_la_mac_port_get_pfc_queue_state(PyObject *self, PyObject *args) {
  Py_ssize_t argc;
  PyObject *argv[3] = {
    0
  };
  Py_ssize_t ii;
  
  if (!PyTuple_Check(args)) SWIG_fail;
  argc = args ? PyObject_Length(args) : 0;
  for (ii = 0; (ii < 2) && (ii < argc); ii++) {
    argv[ii] = PyTuple_GET_ITEM(args,ii);
  }
  ***if (argc == 2) {***  
        return _wrap_la_mac_port_get_pfc_queue_state__SWIG_0(self, args);  
  }  
  ***if (argc == 2) {***  
        return _wrap_la_mac_port_get_pfc_queue_state__SWIG_1(self, args);   
  }   
  
  ***As you can see, the condition statement is not correct, the two conditions are the same, there is no switch to handle (argc == 3)***  
  
  
