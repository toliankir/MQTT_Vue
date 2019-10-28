<template>
  <span>{{ counter }}</span>
</template>

<script lang="ts">
import { Vue, Component, Prop } from 'vue-property-decorator';

@Component
export default class AsideMenuCounter extends Vue {
  @Prop()
  private counter!: number;
  private mounted() {
      console.warn(this.counter);
  }
}
</script>

<style scoped lang="less">
span {
  display: inline-block;
  margin-left: 1rem;
  font-size: 1.05rem;
  color: #000000;
  background-color: #ffc200;
  height: 1.5rem;
  width: 1.5rem;
  text-align: center;
  border-radius: 50%;
  & .bg-red {
      background-color: red;
  }
  & .bg-yellow {
      background-color: #ffc200;
  }
}

</style>