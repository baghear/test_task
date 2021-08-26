<template>
  <svg width="22" height="22" viewBox="0 0 22 22" fill="none" xmlns="http://www.w3.org/2000/svg"
       :class="{'svgActive' : activeIcon}">
    <path d="M1 5.28292L11 1L21 5.28292M1 5.28292L11 9.56585M1 5.28292V5.28571M21 5.28292L11 9.56585M21 5.28292V16.7143L11 21M21 5.28292L11 9.57143V21M11 9.56585V21M11 9.56585L1 5.28571M11 21L1 16.7143V5.28571" stroke="#F8F8FA" stroke-width="1.8" stroke-linejoin="round"/>
  </svg>
</template>

<script>
export default {
  name: "IconCube",

  props: {
    activeIcon: Boolean,
  },
}
</script>

<style scoped>
  .svgActive path{
    stroke: #FBBC05;
  }
</style>