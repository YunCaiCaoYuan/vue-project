<template>
  <section>
    <div class="qrcode" ref="qrCodeUrl"></div>
  </section>
</template>

<script>
import QRCode from 'qrcodejs2'

export default {
  data() {
    return {
      qrCodeUrl : ""
    }
  },
  methods: {
    creatQrCode() {
      var qrcode = new QRCode(this.$refs.qrCodeUrl, {
        text: 'http://www.baidu.com', // 需要转换为二维码的内容
        width: 500,
        height: 500,
        colorDark: '#000000',
        colorLight: '#ffffff',
        correctLevel: QRCode.CorrectLevel.H
      })
    },
  },
  mounted() {
    this.creatQrCode();
  },
}
</script>
