<template>
  <div class="header-icon">
    <div>
      <slot></slot>
    </div>
    <div class="title">
      {{title}}
    </div>
  </div>
</template>

<script>
export default {
  name: "HeaderIcon",

  props:{
    title: String,
  }
}
</script>

<style scoped>
.header-icon{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: #F8F8FA;
  padding-right: 20px;
  margin-left: 20px;
  border-right: 1px solid white;
}

/*.header-icon:after{
  content: "";
  width: 2px;
  height: 48px;
  position: absolute;
  right: -20px;
  background-color: white;
}*/
</style>