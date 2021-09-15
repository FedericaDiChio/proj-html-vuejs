<template>
  <main>
    <section id="jumbotron" class="d-flex align-items-center">
      <div class="container">
        <div class="row">
          <Jumbotron />
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import Jumbotron from "../components/Jumbotron.vue"
export default {
    components: { Jumbotron },
    name: "Main",

};
</script>

<style>
</style>