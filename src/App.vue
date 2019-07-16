<template>
  <div class="container">
      <NoticeBar
        class="notice-bar"
        has-icon
        bar-color="rgba(255,255,255,0.5)"
        :notice-list="noticeList"
        time-str=""
      >得到</NoticeBar>
      <div style="position: absolute;top: 50%;left: 10%;">
        无限滚动 建议用rem做移动端适配
      </div>
  </div>
</template>

<script>
  import NoticeBar from './infinite-notice-bar/infinite-notice-bar'

  export default {
    name: 'share',
    components: {
      NoticeBar
    },
    data () {
      return {
        simpleNoticeList: [
          '你在说什么',
          '柚子是世界上最帅的男人?'
        ],
        noticeList: [
          {
            name: '马化腾',
            icon: 'http://youlehe-pic.yiyayouxi.com/icon/900001.jpg',
            content: '法拉利'
          },
          {
            name: '马云',
            icon: 'http://youlehe-pic.yiyayouxi.com/icon/900001.jpg',
            content: '太阳系'
          }
        ]
      }
    },
    created () {
    },
    methods: {

    }
  }
</script>

<style scoped>
  .notice-bar {
    position: absolute;
    left: 5%;
    box-shadow: #191919;
  }
  .container{
    width:100%;
    height:100vh;
    background:rgba(254,213,190,1);
  }
  .background {
    /*position: absolute;*/
    /*background: url('../assets/share_background.png');*/
    background-size: cover;
    width:10rem;
    height:18.13rem;
    overflow: hidden;
  }
  body{
    margin: 0 auto;
  }
  html{
    margin: 0 auto;
  }
</style>
