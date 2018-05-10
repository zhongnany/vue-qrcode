<template>
  <div v-show="qrcodeUrl" class="response">
    <p>{{msg}}</p>
    <qrcode 
    :value="qrcodeUrl" 
    v-if="qrcodeUrl" 
    :options="{ size: 170 }">
    </qrcode>
    <p>请扫码访问百度</p>
  </div>
</template>

<script>
import QRcode from '@xkeshi/vue-qrcode'
export default {
  name: 'HelloWorld',
  data () {
    return {
      qrcodeUrl:"http://www.baidu.com",
      msg: 'Welcome to use vue-qrcode'
    }
  },
  components: {
    qrcode : QRcode
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
</style>
