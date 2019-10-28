<template>
  <div>
    <p class="task-count">{{count}}</p>
    <p class="task-description">{{ title }}</p>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class AsideTask extends Vue {
  @Prop()
  private title!: string;
  @Prop()
  private count!: number;
}
</script>

<style scoped lang="less">
@import "../../style/constants";
div {
  width: 48%;
  display: flex;
  flex-direction: column;

  & .task-count {
    color: @aside-main-text-main-color;
    font-size: 1.5rem;
    margin: 0;
  }

  & .task-description {
    color: @aside-secondary-text-color;
    margin: 0;
    font-size: 0.95rem;
  }
}
</style>