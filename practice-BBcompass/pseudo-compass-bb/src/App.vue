<script setup lang="ts">
import MinimapImg from '@/components/MinimapImg.vue';
import { ref } from 'vue';

const mapLocate = ref("第3採掘島");
const mapType = ref("夕暮れの戦火");
// const changeMap = ():void => {
//   if(minimap !==  undefined){
//     if(minimap.value !== undefined){
//       minimap.value.onChangeMap();
//     }
//   }
// }
</script>

<template>
  <header>
  </header>
  <p>マップ場所
    <select v-model="mapLocate">
      <option>第3採掘島</option>
      <option>第3採掘島あ</option>
    </select>
  </p>
  <p>マップ種類
    <select v-model="mapType" v-on:change="">
      <option>夕暮れの戦火</option>
      <option>臨海決戦</option>
    </select>
  </p>
  <MinimapImg v-bind:map-locate="mapLocate" v-bind:map-type="mapType"/>
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
