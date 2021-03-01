<template>
        <button type="button" @click="onSubmit()">Submit</button>
</template>

<script>
import axios from 'axios'

export default {
    name: 'HelloWorld',
    data: function () {
        return {
            data: {}
        }
    },
    created () {


    },
    methods: {
        onSubmit() {

            const options = {
                method: 'GET',
                url: 'http://api-with-cors.local/api/product',
                params: {

                },
                headers: {
                    'X-Accept': 'accept-header',
                }
            };

            axios.request(options).then(function (response) {
                console.log(response.data);
            }).catch(function (error) {
                console.error(error);
            });
        }
    }
}
</script>

<style scoped>

</style>
