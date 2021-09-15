<template>
  <header class="d-flex align-items-center justify-content-around">
    <figure>
      <img :src="logo" alt="logo" />
    </figure>
    <nav class="d-flex">
      <ul v-for="(menu, index) in menus" :key="index">
        <li>
          <a class="text-light" :href="menu.url">{{ menu.text }}</a>
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

<style>
</style>