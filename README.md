### Infinite-Notice-Bar

> 无限滚动的消息通知栏,简单实用,适用于任意场景,长度高度可定制 

- 使用方式:
  - 一个条完整的通知由下面的json组成 

  - ```javascript
    {
        name:"玩家姓名",
        icon:"马化腾",
        action:"得到",
        content:"法拉利",
        timeStr:"1秒前"
    }
  	```
  	- 一个简单的通知仅仅是一个数组,包含消息字符串
   - ```javascript
    ["哈哈哈","哈哈哈是"]
    ``` 
  
  		<img src="https://iule-app.oss-cn-hangzhou.aliyuncs.com/img/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-07-16%20%E4%B8%8B%E5%8D%887.00.54.png">    就像这样  !
	
		
	- 将src目录下,infinite-notice-bar.vue 拷贝出来
  - 放到自己的目录
  - 页面中引入此组件
  - 如下


  ```html
  <template>
    <div>
      // 建议放在任意位置使用绝对定位将通知栏定位 
      // 若是非H5应用(没有做rem和px的转换) 大小需要自行调整
      <NoticeBar
          class="notice-bar"
          has-icon
          bar-color="rgba(255,255,255,0.5)" // 通知栏组件的颜色,建议使用rgba,可以设置透明度,最后一位0.5即是透明度
          :notice-list="noticeList" // 可以传入一个复杂的list,不可以和simple-list共存
          :simple-list="simpleList" // 可以传入一个简单的list,不可以和notice-list共存
          time-str // 默认有时间戳文字 ( 3s前 ,1s前 这样) 
         ></NoticeBar>
    </div>	
  </template>
  <script>
    import NoticeBar from './infinite-notice-bar/infinite-notice-bar'
    export default {
    name: 'NoticeBar',
    data () {
      return {
        number: 0,
        simpleList: [
          "你在说什么?",
          "你要给我一个赞吗?"
        ],
        noticesList: [
          {
            name: '哈哈哈',
            icon: 'http://youlehe-pic.yiyayouxi.com/icon/900001.jpg',
            content: 'vivo X27Pro',
            timeStr: '3秒前'
          },
          {
            name: '啦啦啦',
            icon: 'http://youlehe-pic.yiyayouxi.com/icon/900001.jpg',
            content: 'vivo X27Pro',
            timeStr: '3秒前'
          }
        ]
      }
    }
  }
  </script>
  <style scoped>
  </style>
  ```

|     字段      |                             含义                             |                             示例                             |         默认值          |
| :-----------: | :----------------------------------------------------------: | :----------------------------------------------------------: | :---------------------: |
|   has-icon    | 是否包含icon,如果是,则需要在传入的noticeList里增加icon的字段 |                          `true锁定`                          |         `true`          |
|  simpleList   |               简单的消息列表,是一个字符串数组                |                       `["a","b","c"]`                        |            -            |
|   bar-color   |  通知条背景颜色,除了颜色也可以传入图片(css的background格式)  | ```Rgba(255,255,255,0.5)```  或 `#FFFFFF `或  `url("图片的地址")` | `Rgba(255,255,255,0.5)` |
|   font-size   |                       通知栏文字的大小                       |                    `0.3rem`,`100px`,`20%`                    |          `35%`          |
|   time-str    |                  是否包含最后的时间返回指示                  |                            `true`                            |         `true`          |
|     speed     |                       滚动停留时间 ms                        |                            `3000`                            |         `2000`          |
| content-color |          奖品文字颜色(如果是simple模式,此字段失效)           |             `Rgba(255,255,255,1)` 或 `#FFFFFF `              |        `#c95354`        |
|     width     |                         通知栏的长度                         |                      `85%` 或 `9rem` 或                      |         `9rem`          |
|    height     |                         通知栏的高度                         |                           `1.2rem`                           |        `1.2rem`         |




