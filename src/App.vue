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
    icon: 'Wallet' 
  },
  {
    id: 2,
    text: 'DEX',
    icon: 'DEX' 
  },
  {
    id: 3,
    text: 'TX explorer',
    icon: 'TX Explorer' 
  },
  {
    id: 4,
    text: 'Certificates',
    icon: 'Certificates' 
  },
  {
    id: 5,
    text: 'Tokens',
    icon: 'Tokens' 
  },
  {
    id: 6,
    text: 'VPN client',
    icon: 'VPN client' 
  },
  {
    id: 7,
    text: 'VPN service',
    icon: 'VPN service' 
  },
  {
    id: 8,
    text: 'Console',
    icon: 'Console' 
  },
  {
    id: 9,
    text: 'Logs',
    icon: 'Logs' 
  },
  {
    id: 10,
    text: 'Settings',
    icon: 'Settings' 
  },
  {
    id: 11,
    text: 'dApps',
    icon: 'dApps' 
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
