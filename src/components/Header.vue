<template>
  <header>
    <div class="container">
      <div class="d-flex justify-content-between">
          <figure>
            <img :src="logo" alt="logo" />
          </figure>
          <nav>
            <ul>
              <li v-for="(menu, index) in menus" :key="index">
                <a
                  class="ms-4 text-grey"
                  :class="{ active: menu.current }"
                  :href="menu.url"
                  >{{ menu.text }}</a
                >
              </li>
              <span class="news ms-2">new</span>
              <button class="ms-5 px-4 py-2">Schedule a workout</button>
            </ul>
          </nav>
        </div>
    </div>
     
  </header>
</template>

<script>
export default {
  name: "Header",
  props: ["menus", "logo"],
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/_mixin.scss";
li {
  a:hover,
  a.active {
    color: #ffff;
  }
}

button {
  @include buttons("blue");
  font-size: 12px;
}
</style>