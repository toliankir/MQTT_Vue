<template>
  <div>
    <div class="user-card">
      <img src="@/assets/photos/1.jpg" alt="User photo" />
      <div class="user-data">
        <p class="user-name">Jean Gonzales</p>
        <p class="user-state">Product Owner</p>
      </div>
    </div>
    <div class="user-details">
      <button>
        <span class="dots"></span>
      </button>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class AsideProfile extends Vue {
}
</script>

<style scoped lang="less">
div {
  background-color: #202020;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-top: 1rem;
  padding-bottom: 1rem;

  & .user-details {
    margin-right: -0.5rem;

    & button {
      height: 40px;
      min-width: 40px;
      background: none;
      border: none;
      display: flex;
      justify-content: center;
      align-items: center;
      cursor: pointer;
      border-radius: 20px;
      outline: none;
      padding: 0;
      margin: 0;
    }
  }

  & .user-card {
    display: flex;

    & img {
      width: 64px;
      height: 64px;
      border-radius: 50%;
      margin-right: 1rem;
    }

    & .user-data {
      display: flex;
      flex-direction: column;
      justify-content: center;

      & .user-name {
        color: #ffffff;
        margin: 0;
      }

      & .user-state {
        color: #9b9b9b;
        margin: 0;
      }
    }
  }
}

.dots {
    position: absolute;
    display: block;
    width: 5px;
    height: 5px;
    border-radius: 50%;
    background-color: #9b9b9b;

    &::before {
        position: absolute;
        left: -150%;
        top: 0;
        display: block;
        content: "";
        width: inherit;
        height: inherit;
        border-radius: inherit;
        background-color: inherit;
    }

    &::after {
        position: absolute;
        left: 175%;
        top: 0;
        display: block;
        content: "";
        width: inherit;
        height: inherit;
        border-radius: inherit;
        background-color: inherit;
    }
}
</style>