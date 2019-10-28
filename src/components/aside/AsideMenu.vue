<template>
  <nav>
    <p>MENU</p>
    <a href="#">Home</a>
    <a href="#">My Tasks</a>
    <a href="#">
      Notifications
      <AsideMenuCounter :counter='4' />
    </a>
  </nav>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import AsideMenuCounter from '@/components/aside/AsideMenuCounter.vue';

@Component({
  components: {
    AsideMenuCounter,
  },
})
export default class AsideMenu extends Vue {
}
</script>

<style scoped lang="less">
nav {
  display: flex;
  flex-direction: column;

  & p {
    margin: 1rem 0;
    color: #9b9b9b;
    font-size: 1rem;
  }

  & a {
    margin: 0.9rem 0;
    color: #ffffff;
    font-size: 1.1rem;
    text-decoration: none;


  }
}
</style>