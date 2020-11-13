<template>
    <div>
        <h2>This is a profile page</h2>

        <section>
            <p>The query params {{$route.params.id}} </p>
        </section>
    </div>
</template>
<script>
export default {
    mounted(){

        console.log(this.$route.params.id)
    },

    watch: {

        $route(to, from){

            console.log('to', to)
            console.log('from', from)
        }
    }
}
</script>
<style>

</style>