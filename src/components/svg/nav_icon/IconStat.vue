<template>
  <svg width="20" height="18" viewBox="0 0 20 18" fill="none" xmlns="http://www.w3.org/2000/svg"
    :class="{'svgActive' : activeIcon}"
  >
    <path d="M20 9H15.3333M4.66667 9H0M11.3333 9H8.66667M15.3333 13.6667H11.3333V4.33333H15.3333V13.6667ZM8.66667 17H4.66667V1H8.66667V17Z" stroke="#F8F8FA" stroke-width="1.8"/>
  </svg>
</template>

<script>
export default {
  name: "IconStat",

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