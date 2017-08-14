# 新共享播放器API说明
## 对外提供简单的API实现视频的播放，暂停，快进或者快退，全屏操作。
+ API列表
  - 播放：window.__toThirdPartyAPI.play();
  - 暂停：window.__toThirdPartyAPI.pause();
  - 快进：window.__toThirdPartyAPI.progress(seconds);  ***seconds: 快进的秒数***
  - 快退：window.__toThirdPartyAPI.back(seconds);  ***seconds: 后退的秒数***
  - 进入全屏：window.__toThirdPartyAPI.fullScreen();  
  - 退出全屏：window.__toThirdPartyAPI.exitFullScreen(); 

## 播放器初始化完成后，向document对象抛出“videoReady"事件，用户可以监听这个事件,监听方法格式如下：
```
    /*
     * 回调函数在'videoReady'触发后调用
     * 参数e: 事件对象
     * 参数msg: 'Video is ready!'
    */
    $(document).on('videoReady', function(e, msg){
        console.log(msg); 
    });
```
