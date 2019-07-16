
### Infinite-Notice-Bar

> 无限滚动的消息通知栏,简单实用,适用于任意场景,长度高度可定制 
> Add this notice bar on your H5 page! You can use just simple array or more complex config to define your own notice bar!

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```


- 使用方式:

  

  ```html
  <template>
    <div>
      // 建议放在任意位置使用绝对定位将通知栏定位 
      <NoticeBar
          class="notice-bar"
          has-icon bar-color="rgba(255,255,255,0.5)"
          :notice-list="noticeList"
          time-str
         ></NoticeBar>
    </div>	
  </template>
  <script>
    export default {
    name: 'NoticeBar',
    data () {
      return {
        number: 0,
        notices: [
          {
            name: '旧巷笔录1',
            icon: 'http://youlehe-pic.yiyayouxi.com/icon/900001.jpg',
            content: 'vivo X27Pro',
            timeStr: '3秒前'
          },
          {
            name: '旧巷笔录2',
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
