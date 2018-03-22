# 微信小程序 wepyjs 第三方 消息提示插件

### 效果：
![toast](http://oyz3pjs26.bkt.clouddn.com/blog/180321/9mf0KAbIhj.gif)






## 使用

### 安装组件
```
npm install wepy-message --save
```

### 引入组件
```javascript
// index.wpy
<template>
    <message></message>
</template>
<script>
    import wepy from 'wepy';
    import message from 'wepy-message';

    export default class Index extends wepy.page {
        data={
            
        }
        components = {
            message
        };
        
        onLoad(){
            this.$invoke('message', 'success', '删除成功');
            this.$invoke('message', 'error', '删除成功');
            this.$invoke('message', 'error', '删除成功');
            this.$invoke('message', 'info', '删除成功');
            this.$invoke('message', 'info', '删除成功');
            this.$invoke('message', 'info', '删除成功',3000).then(()=>{
                //do somethings....
            });
            //第一个参数         组建名             msssage                             必填
            //第二个参数         类型              提供4种（success,error,info,warning） 必填
            //第三个参数         提示内容            字符串                              必填
            //第四个参数         显示时长            number                             选填
            //支持自动隐藏完回调
        }
        
       
    }
    
</script>
```



### 更新日志
20180321            init
20180322            修改默认时间
20180322            修改位置和定位方式


[本人博客：callmesoul.cn](http://callmesoul.cn)

![toast](http://nowechat.oss-cn-shenzhen.aliyuncs.com/qrcode_for_gh_b4c00b84720c_258.jpg)

