<template>
  <div>
    <h2>PROJECTUS</h2>
    <button>
      <img src="@/assets/Search@3x.svg" alt="Aside logo" />
    </button>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class AsideTitle extends Vue {
  @Prop() private msg!: string;
}
</script>

<style scoped lang="less">
div {
  margin: 2.5rem 0;
  display: flex;
  justify-content: space-between;
  & h2 {
    color: #ffffff;
    margin: 0 0 0 3rem;
    font-size: 1.3rem;

    &::before {
      position: absolute;
      width: 40px;
      height: 100%;
      content: "";
      background: url(../../assets/Logo@3x.svg) no-repeat;
      background-size: 32px;
      left: -3rem;
    }
  }
  & button {
    cursor: pointer;
    background-color: #000000;
    border: none;
    outline: none;

    & img {
      width: 130%;
    }
  }
}
</style>
