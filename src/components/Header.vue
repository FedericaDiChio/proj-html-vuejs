<template>
  <header class="d-flex align-items-center justify-content-around">
    <figure>
      <img :src="logo" alt="logo" />
    </figure>
    <nav>
      <ul class="d-flex">
        <li v-for="(menu, index) in menus" :key="index">
          <a class="px-4 text-grey" 
          :class="{active: menu.current}" 
          :href="menu.url">{{ menu.text }}</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: ["menus", "logo"],
};
</script>

<style lang="scss">
   ul li {  
    a:hover,
    a.active {
      color: #ffff;
    }
   }

</style>