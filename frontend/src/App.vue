<template>
    <ui-header/>
        <div id="nav">
            <router-link to="/">Home</router-link>
            <router-link to="/about">About</router-link>
        </div>
    <router-view/>
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
