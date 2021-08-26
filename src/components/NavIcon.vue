<template>
  <div class="nav-icon" :class="{'select-highlight': activeNav}">
    <div>
       <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "Icon",
  props: {
    activeNav: Boolean,
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
 .nav-icon{
   display: flex;
   justify-content: center;
   align-items: center;
   padding: 30px;
   cursor: pointer;
 }

 .select-highlight:before{
   content:"";
   position: absolute;
   left: 0;
   width: 5px;
   height: 86px;
   background-color: #FBBC05;
 }
</style>
