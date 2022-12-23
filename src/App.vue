<template>
  <LeftMenu :items="items"/>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import LeftMenu from './components/LeftMenu.vue';

@Options({
  components: {
    LeftMenu,
  },
})
export default class App extends Vue {
  items = [{
    id: 1,
    text: 'Wallet',
    icon: '' 
  },
  {
    id: 2,
    text: 'DEX',
    icon: '' 
  },
  {
    id: 3,
    text: 'TX explorer',
    icon: '' 
  },
  {
    id: 4,
    text: 'Certificates',
    icon: '' 
  },
  {
    id: 5,
    text: 'Tokens',
    icon: '' 
  },
  {
    id: 6,
    text: 'VPN client',
    icon: '' 
  },
  {
    id: 7,
    text: 'VPN service',
    icon: '' 
  },
  {
    id: 8,
    text: 'Console',
    icon: '' 
  },
  {
    id: 9,
    text: 'Logs',
    icon: '' 
  },
  {
    id: 10,
    text: 'Settings',
    icon: '' 
  },
  {
    id: 11,
    text: 'dApps',
    icon: '' 
  }]
}
</script>

<style lang="scss">
html {
  height: 100%;
}
body {
  margin: 0;
  height: 100%;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
}
</style>
