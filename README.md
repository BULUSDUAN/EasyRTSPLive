## 介绍 ##
此Demo涉及到EasyRTMP和EasyRTSPClient两个需要商业授权的SDK。
EasyRTMP是EasyDarwin团队开发的一套夸平台的RTMP直播推送功能组件，内部集成了包括：基本RTMP协议、断线重连、异步推送、环形缓冲区、推送网络拥塞自动丢帧、缓冲区关键帧检索、事件回调(断线、音视频数据回调)，支持市面上绝大部分的RTMP流媒体服务器。详见https://github.com/EasyDarwin/EasyRTMP。
EasyRTSPClient是一套全平台支持稳定、易用、支持重连的RTSPClient工具。能够拉取RTSP流地址并解析出视频帧和音频帧数据。详见https://github.com/EasyDarwin/EasyRTSPClient。
两者都是支持多路同时操作的SDK库，这样就方便了我们基于他们做多路RTSP流同时转成RTMP进行推送。由于EasyRTMP和EasyRTSPClient是需要商业授权的SDK，因此商业使用需要联系support@easydarwin.org 。

采用Config.ini配置文件，来配置每路输入的RTSP地址，以及目标RTMP地址。channel必须是channel0到channel1024之间，目标rtmp地址不能重复。

    [channel0]
	rtsp=rtsp://admin:admin@192.168.66.222/11
	rtmp=rtmp://demo.easydss.com:10085/live/test1
	option=1
	[channel1]
	rtsp=rtsp://admin:admin@192.168.66.222/22
	rtmp=rtmp://demo.easydss.com:10085/live/test2

## 编译及运行 ##
Windows上使用Visual Studio 2010开发，当然各位可以改成自己的编译环境。
Linux上编译命令如下：

	清理:	./Buildit clean
	64位编译：./Buildit x64

运行时将Config.ini文件放至于可执行文件相同路径下，然后直接执行可执行程序，不用带参数。

## 下载 ##
可执行程序下载：https://pan.baidu.com/s/1-7lZ3KM4wPl87OLx2tWjTQ

## 获取更多信息 ##

邮件：[support@easydarwin.org](mailto:support@easydarwin.org) 

WEB：[www.EasyDarwin.org](http://www.easydarwin.org)

QQ交流群：[587254841](https://jq.qq.com/?_wv=1027&k=4ASE72a)

Copyright &copy; EasyDarwin.org 2012-2017

![EasyDarwin](http://www.easydarwin.org/skin/easydarwin/images/wx_qrcode.jpg)