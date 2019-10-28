<template>
  <div>
    <aside>
      <AsideTitle />
      <AsideProfile />
      <AsideTasks />
      <AsideMenu />
    </aside>
    <div class="main-wrapper">123</div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import AsideTitle from '@/components/aside/AsideTitle.vue';
import AsideProfile from '@/components/aside/AsideProfile.vue';
import AsideMenu from '@/components/aside/AsideMenu.vue';
import AsideTasks from '@/components/aside/AsideTasks.vue';

@Component({
  components: {
    AsideTitle,
    AsideProfile,
    AsideMenu,
    AsideTasks,
  },
})
export default class App extends Vue {}
</script>

<style scoped lang="less">
div {
  display: flex;
  font-family: "Open Sans", sans-serif;
}
aside {
  min-height: 100vh;
  min-width: 350px;
  max-width: 455px;
  width: 21%;
  background-color: #000000;
  display: flex;
  flex-direction: column;
  & > * {
    padding-right: 1.5rem;
    padding-left: 2.5rem;
  }
}

div.main-wrapper {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
}
</style>

