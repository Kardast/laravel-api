<template>
    <div class="container">
        <!-- qui andrà il tuo codice vue per creare le cards -->
        ciao
    </div>
</template>

<script>
import Axios from 'axios'

    export default {
        name: 'App',
        data(){
            return{
                baseUrl: window.location.origin,
                posts: []
            }
        },
        created(){
            Axios.get('http://localhost:8000/api/posts')
                .then(res => {
                    this.res.data.response.data;
                    console.log(res);
                })
                .catch(error => console.log('errore!'));
        }
    }
</script>

<style lang="scss" scoped>
    @import 'bootstrap/scss/bootstrap';
</style>
