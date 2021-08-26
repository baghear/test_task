<template>
  <div class="profile">
    <HeaderIcon v-for="item in headerMenu" :key="item.title"
      :title=item.title
    >
      <component :is='item.icon'/>
    </HeaderIcon>
    <img src="image/photo.png" class="profile__photo" alt="">
    <div class="profile__name">Arian Z.</div>
    <div class="profile__selector">
      <div class="profile__arrow"></div>
    </div>
  </div>
</template>

<script>
import HeaderIcon from "@/components/HeaderIcon";
import IconBell from "@/components/svg/header_icon/IconBell";
import IconChat from "@/components/svg/header_icon/IconChat";

export default {
  name: 'Profile',

  components: {
    HeaderIcon,
  },

  data: function () {
    return {
      headerMenu: [
        {
          icon: IconBell,
          title: 'Notification'
        },
        {
          icon: IconChat,
          title: 'chat'
        },
      ]
    }
  }
}
</script>

<style scoped>

.profile {
  display: flex;
  align-items: center;
  border-radius: 12px;
  overflow: hidden;
  background-color: #F8F8FA;
}

.profile__photo{
  width: 50px;
  height: 50px;
  border-radius: 50%;
  margin-left: 20px;
}

.profile__name{
  font-size: 20px;
  line-height: 30px;
  font-weight: 500;
  margin: 0 15px;
}

.profile__selector{
  position: relative;
  width: 30px;
}

.profile__arrow{
  position: absolute;
  top: -12px;
  width: 15px;
  height: 15px;
  transform: rotate(45deg);
  border-bottom: 3px solid #FBBC05;
  border-right: 3px solid #FBBC05;
  margin-right: 10px;
}
</style>