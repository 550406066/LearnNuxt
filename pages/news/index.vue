<template>
    <div>
        {{news}}
        id:{{$route.params.Id}}
        <ul>
            <li><nuxt-link :to="url">NEWS</nuxt-link></li>
        </ul>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                url:"/news/123",
                news: "xxxx"
            }
        },
    }
</script>

<style scoped>

</style>