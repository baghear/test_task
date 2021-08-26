<template>
  <div class="selector">
    <div class="selector__text">COVID-19</div>
    <div class="selector__arrow">
      <div class="arrow"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SelectorComponent"
}
</script>

<style scoped>
.selector{
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #F8F8FA;
  border-radius: 12px;
  padding: 22px;
}

.selector__text{
  font-size: 20px;
  line-height: 30px;
  margin-right: 50px;
}

.selector__arrow{
  display: flex;
  justify-content: center;
  align-self: flex-start;
}

.arrow{
  width: 15px;
  height: 15px;
  transform: rotate(45deg);
  border-bottom: 3px solid #FBBC05;
  border-right: 3px solid #FBBC05;
}
</style>