<template>
<div class="card text-white border-0 cardo">
  <img :src="training.img" class="card-img img-fluid" alt="...">
  <div class="card-img-overlay caption">
    <h4 class="card-title">{{ training.title }}</h4>
    <p class="card-text">{{ training.text }}</p>
  </div>
</div>

    
</template>

<script>
export default {
    name: "Cards",
    props: ["training"],
}
</script>

<style lang="scss">  
        .cardo {
            height: 200px;
            width: 300px;
        }
</style>