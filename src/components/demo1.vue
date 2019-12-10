<template>
    <div>
        <p>dd</p>
        <button @click="sayHaha">哈哈</button>
    </div>
</template>

<script>
    import axios from 'axios'

    export default {
        name: "demo1",
        components: {},
        methods: {
            sayHaha: function () {
                axios({
                    method: 'post',
                    url: 'localhost:8080/test/t2',
                    data: {
                        name: 'kk',
                        age: '17'
                    }
                }).then(res => {
                    console.log(res);
                });
            }
        },
        created() {

        }
    }
</script>

<style scoped>

</style>
