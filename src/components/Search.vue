<template>
  <div class="search">
    <input type="text" placeholder="Facility Search" class="search__input">
    <img src="image/magnifier.png" width="18" height="18" alt="">
  </div>
</template>

<script>
export default {
  name: "Search"
}
</script>

<style scoped>

.search {
  display: flex;
  align-items: center;
  padding: 12px 17px;
  border-radius: 12px;
  background-color: #F8F8FA;
}

.search__input {
  font-size: 18px;
  line-height: 26px;
  border: 0;
  outline: none;
  background-color: #F8F8FA;
}
</style>