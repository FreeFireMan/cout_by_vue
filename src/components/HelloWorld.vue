<template>
    <div class="hello">
        <div class="card" style="width: 18rem;">
            <img src=".././assets/logo.png" class="card-img-top" alt="Vue logo">
            <div class="card-body">
                <h2 class="text-center">{{msg}}</h2>
                <!--        <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>-->
                <!--        <a href="#" class="btn btn-primary">Go somewhere</a>-->
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'HelloWorld',
        props: {
            msg: Number
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
    /*h3 {*/
    /*  margin: 40px 0 0;*/
    /*}*/
    /*ul {*/
    /*  list-style-type: none;*/
    /*  padding: 0;*/
    /*}*/
    /*li {*/
    /*  display: inline-block;*/
    /*  margin: 0 10px;*/
    /*}*/
    /*a {*/
    /*  color: #42b983;*/
    /*}*/
</style>
