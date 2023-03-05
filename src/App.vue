<template>
  <qr-code :qr-code-path="qrCodePath" />
</template>

<script setup>
import QrCode from './components/QrCode.vue'

const qrCodePath = '/src/assets/img/qr-code.png'

</script>