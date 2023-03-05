<template>
  <div id="page">
    <div id="qr-code">
      <img id="qr-code-img" :src="qrCodeImage" alt="QR Code" />

      <div id="qr-code-text">
        <h1>Improve your front-end skills by building projects</h1>

        <p>Scan the QR code to visit Frontend Mentor and take your coding skills to the next level</p>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  qrCodeImage: {
    type: Image,
    required: true
  }
});

const qrCodeImg = new URL(props.qrCodePath, import.meta.url).href;
</script>

<style lang="scss" scoped>
  #page {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;


  #qr-code {
    display: flex;
    flex-direction: column;
    align-items: center;
    max-width: 300px;
    // responsive height
    justify-content: center;
    padding: 15px;
    background-color: white;
    border-radius: 5%;
    box-shadow: 0 0 10px 0 rgba(0, 0, 0, 0.1);

    #qr-code-img {
      width: 100%;
      height: 100%;
      object-fit: contain;
      border-radius: 5%;
      margin: 5px;
    }

    #qr-code-text {
      text-align: center;
      padding: 15px;

      h1 {
        font-size: 1.4rem;
        font-weight: 700;
        margin-bottom: 10px;
      }

      p {
        font-weight: 400;
        color: hsl(220, 15%, 55%)
      }
    }
  }
}
</style>