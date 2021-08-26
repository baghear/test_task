<template>
  <div class="info">
    <img src="image/download.png" alt="">
    <img src="image/printer.png" alt="" class="info__img">
    <img src="image/share.png" alt="">
  </div>
</template>

<script>
export default {
  name: "Info"
}
</script>

<style scoped>
.info {
  display: flex;
  align-items: center;
  padding: 12px 32px;
  background-color: #F8F8FA;
  border-radius: 12px;
}

.info__img {
  margin: 0 32px;
}
</style>