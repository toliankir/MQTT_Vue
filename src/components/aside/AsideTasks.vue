<template>
  <div>
    <AsideTask :title="'Completed Tasks'" :count="3" />
    <AsideTask :title="'Open Tasks'" :count="22" />
  </div>
</template>
<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import AsideTask from './AsideTask.vue';

@Component({
  components: {
    AsideTask,
  },
})
export default class AsideTasks extends Vue {}
</script>

<style scoped lang="less">
@import "../../style/constants";

div {
  margin: 1.5rem 0;
  display: flex;
  justify-content: space-between;
}
</style>