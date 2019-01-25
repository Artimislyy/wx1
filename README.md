＃WX1  
**微信小程序第一周总结**  
总结人：罗杨阳   
**tarBar**
(```)
"tabBar":{
    "backgroundColor": "#000000",
    "selectedColor": "green",
    "list":[{
      "pagePath":"pages/index/index",
      "text":"首页"
    },
   {
      "pagePath":"pages/test/test",
      "text":"测试"
    },{
      "pagePath":"pages/lyy/lyy",
      "text":"我的"
    }]
  }
  (```)   
  
  **页面跳转**  
  (```)
  <navigator hover-class='active'  url='../logs/logs'>跳转到logs</navigator>
  totext:function(){
    wx.navigateTo({
      url: '../logs/logs',
    });
  }
  (```)
  *注意：navigateTo, redirectTo 只能打开非 tabBar 页面*  
  
  **设置按钮**
  (```)
  <view>我的名字是  {{name}}</view>
<button bindtap='clickme'>点击我</button>
clickme(){
    this.setData({
      name:"Artimis"
    })
  }, 
  (```)  
  
  **page中获取全局变量**
  (```)
  const app = getApp()
    globalData:{
        name:"lyy",
        pass:"12345"
  }
  (```)
