<template>
  <div class="content">
    <div ref="playerCont"></div>
    <div class="buttom">
      <button @click="play()">点击播放</button>
      <button @click="pause()">暂停</button>
      <button @click="changeUrl()">换一个</button>
    </div>
  </div>
</template>

<script>
import DPlayer from 'dplayer'
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }, 
  data(){
    return {
      options: {
        video: {
          url: require('./../assets/demo1.mp4'),
          pic: require('./../assets/videoImg.jpg')
        },
        autoplay: false,
        contextmenu: [
            {
                text: 'GitHub',
                link: 'https://github.com/MoePlayer/vue-dplayer'
            }
        ]
      },
      dp: null
    }
  },
  mounted() {
    this.options.container = this.$refs.playerCont
    this.dp = new DPlayer(this.options)
  },
  methods:{
    play(){
      console.log(this.dp)
      this.dp.play()
    },
    pause(){
      this.dp.pause()
    },
    changeUrl(){
      this.options.video.url = require('./../assets/demo2.mp4')
      this.dp = new DPlayer(this.options)
      this.play()
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.content{
  max-width: 959px;
  margin: 0 auto;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
button {
  margin: 40px;
}
</style>
