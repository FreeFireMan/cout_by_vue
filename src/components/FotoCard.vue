<template>
    <div class="card" style="width: 18rem;">
        <img :src="url" class="card-img-top" alt="...">

        <div class="card-body">
            <h5 class="card-title">{{id}}</h5>
            <p class="card-text">{{title}}</p>
            <a href="#" class="btn btn-primary">Go somewhere</a>
        </div>
    </div>
</template>

<script>
  export default {
    name: "FotoCard",
    props: ['url','id','title']
  }
</script>

<style scoped>

</style>
