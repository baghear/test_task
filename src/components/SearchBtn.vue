<template>
  <div class="search-btn" :style="{'borderColor' : color}">
    <img :src=image alt="">
    <div class="search-btn__text" :style="{'color' : color}">{{title}}</div>
  </div>
</template>

<script>
export default {
  name: "SearchBtn",
  props: {
    title: String,
    image: String,
    color: String
  }
}
</script>

<style scoped>

.search-btn{
  display: flex;
  align-items: center;
  padding: 12px 32px 12px 12px;
  margin-left: 20px;
  background-color: #F8F8FA;
  border-radius: 12px;
  border: 1px solid;
}

.search-btn__text {
  font-size: 18px;
  line-height: 27px;
  font-weight: 500;
  color: #2D2D2D;
  margin-left: 5px;
}
</style>