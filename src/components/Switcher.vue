<template>
  <div class="switch">
    <div v-for="(switchItem, switchIndex) in items" :key="switchIndex"
         class="switch__item"
         @click="switchOn(switchIndex)"
         :class="{switchActive : switchItem.isActive}"
         :style="{'padding' : padding}"
    >
      <component :is="switchItem.icon"></component>
      <div>{{switchItem.text}}</div>
    </div>
  </div>
</template>

<script>
import IconEarth from "@/components/svg/header_icon/IconEarth";
import IconLocation from "@/components/svg/header_icon/IconLocation";

export default {
  name: "Switcher",

  props: {
    items: Array,
    padding: String,
  },

  data: function (){
    return{
      activeSwitch: 1,
    }
  },

  components: {
    IconEarth,
    IconLocation,
  },

  methods: {
    switchOn: function (index) {
      this.items[this.activeSwitch].isActive = false
      this.activeSwitch = index;
      this.items[this.activeSwitch].isActive = true;

      /*console.log(this.switchData)*/
    }
  }
}
</script>

<style scoped>

.switch{
  display: flex;
  align-items: center;
  background-color: #F8F8FA;
  border-radius: 12px;
  margin: 0 20px;
}

.switch__item{
  padding: 12px 32px;
  border-radius: 12px;
  transition: background-color 1.2s;
  font-size: 18px;
  line-height: 24px;
}

.switchActive{
  color: #F8F8FA;
  background-color: #FBBC05;
}
</style>