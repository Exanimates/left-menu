<template>
  <div class="menu">
    <div class="menu__header">
      <img src="../assets/cellframe-logo.svg">
    </div>
    <div class="menu__items">
      <template :key="item.id" v-for="(item, index) in items">
        <div class="menu__item" :class="{ insert: index + 1 === activeItem }" @click="activeItem = index + 1">
          <img class="menu__image" :src="getImgUrl(item.icon)">
          <div class="menu__title">{{ item.text }}</div>
        </div>
      </template>
    </div>
  </div>
</template>

<script lang="ts">
import { Vue, prop } from 'vue-class-component';
import { MenuItem } from '../dto'

export default class LeftMenu extends Vue.with(class {
  items = prop<MenuItem[]>({ type: Array, required: true, default: () => [] })
}) {
  activeItem = 1

  getImgUrl(img: string) {
    return require('../assets/navigation/' + img + '.svg')
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.menu {
    width: 180px;
    height: 100%;
    
    background: #2D3037;
    border-radius: 0px 0px 16px 0px;
    padding-right: 10px;
    box-shadow: 14px 11px 8px 0px rgba(34, 31, 24, 0.2);


    &__header {
      height: 50px;
      display: flex;
      justify-content: left;
      align-items: center;

      padding-top: 10px;
      padding-left: 15px;
      
      color: #FFFFFF;
    }
    &__items {
      display: flex;
      flex-direction: column;

      height: 90%;
      justify-content: space-around;
    }
    &__item {
      display: flex;
      align-items: center;

      height: 52px;
      cursor: pointer;
      color: #FFFFFF;
      background: #2E3138;
      border-radius: 0px 16px 16px 0px;
    }

    &__image {
      margin-left: 28px;
    }

    &__title {
      margin-left: 20px;
    }
}

.insert {
  box-shadow: 1px 1px 0px rgba(107, 102, 126, 0.49), inset 3px 3px 5px rgba(8, 7, 13, 0.25);
}
</style>
