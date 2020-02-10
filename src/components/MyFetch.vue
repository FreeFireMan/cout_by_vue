<template>
    <div>
        {{ name }}, {{ username }}, {{ email }}
    </div>
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
