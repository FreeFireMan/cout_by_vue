<template>
    <div class="card" style="width: 18rem;">

        <div class="card-body">
            <h5 class="card-title">{{name}}</h5>
            <p class="card-text">{{username}}</p>
            <a href="#" class="btn btn-primary">{{ email }}</a>
        </div>
    </div>
<!--    <div>-->
<!--        {{ name }}, {{ username }}, {{ email }}-->
<!--    </div>-->
</template>

<script>
    export default {
        name: "MyFetch",
        props: {
            name: String, username: String, email: String
        },
    }
</script>

<style scoped>

</style>
