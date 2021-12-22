<template>
    <ui-header/>
    <article id="container">
        <router-view/>
    </article>
    <ui-cursor/>
</template>
<script>
import Header from '@/components/Header.vue';
import Cursor from '@/components/Cursor.vue';
export default {
    name: 'App',
    components: {
        'ui-header': Header,
        'ui-cursor': Cursor
    }
}
</script>
<style lang="scss">
    @import '@/assets/sass/common.scss';
</style>
