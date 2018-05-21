<template>
    <div>
{{about}}
   id:{{$route.query.Id}}
    </div>
</template>

<script>
    export default {
        data() {
            return {
                about: "我是about页面"
            }
        },
        head(){
            return {
                title:"这是about页面",
                meta:[
                        {hid:'description',name:'about',content:'This is about page'}
                ]
            }
        }
    }
</script>

<style scoped>

</style>