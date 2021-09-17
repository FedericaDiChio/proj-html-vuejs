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
              <li class="news ms-2">new</li>
              <li><button class="ms-5 px-4 py-2">Schedule a workout</button></li>
              <li>
                <a href=""><i class="fas fa-shopping-cart mx-5 text-grey"></i></a>
                <a href=""><i class="fas fa-search text-grey"></i></a>
              </li>
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
  i:hover, 
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