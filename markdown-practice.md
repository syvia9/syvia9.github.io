# RUNOOB Markdown Test
## Hello World!



## 前人总结的解决办法：

（1）在VScode编辑页面，按快捷键Ctrl+Shift+P，搜索markdown更改预览安全设置，选择允许不安全内容，即可显示预览网页图片。  

（2）本地图片显示预览，要注意.md文件的路径和图片存放的路径，使用图片的相对路径即可显示预览。（注意路径不能有引号" "）  
————————————————
版权声明：本文为CSDN博主「cocoazack」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。  
原文链接：https://blog.csdn.net/givbw/article/details/124028553  

e.g 1. there is a picture online:   
https://github.com/sonic-net/SONiC/blob/master/images/sonic_user_guide_images/section4_images/section4_pic1_high_level.png  
if I copy the very address, and paste to a mardown file, of course using mardown format,  
it won't be showed correctly.  
but if I use "copy image link" to fetch the address :  
https://github.com/sonic-net/SONiC/blob/master/images/sonic_user_guide_images/section4_images/section4_pic1_high_level.png?raw=true  

and paste to markdown, it can be showed properly  
please note that : the "?raw=true" is added in the second copy.  
