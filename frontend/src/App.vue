<template>
    <ui-header/>
    <article id="container">
        <div id="nav">
            <router-link to="/">Home</router-link>
            <router-link to="/about">About</router-link>
        </div>
        <section style="width: 500px; height: 1000px; background: fff;"></section>
        <router-view/>
        <section style="width: 500px; height: 1000px; background: fff;"></section>
    </article>
</template>
<script>
    import Header from './components/Header.vue'
    export default {
        name: 'App',
        components: {
            'ui-header': Header
        }
    }
</script>
<style lang="scss">
@import 'assets/sass/common.scss';
</style>
