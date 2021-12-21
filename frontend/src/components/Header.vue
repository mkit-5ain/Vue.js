<template>
    <div id="header">header1</div>
</template>

<script>
    export default {
        name: 'header',
        mounted: function () {
            this.scroll();
        },
        methods: {
            scroll: function() {
                let scroll = 0;
                let header = document.getElementById('header');
                window.addEventListener('scroll', function () {
                    scroll = window.scrollY;
                    if ( scroll > 0 ) {
                        header.classList.add('active');
                    } else if (scroll == 0 ) {
                        header.classList.remove('active');
                    }
                });
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
    #header {
        position: fixed;
        top: 0px;
        left: 0px;
        z-index: 10;
        width: 100%; 
        height: 50px;
        border-bottom: 1px solid #111;
    }
</style>
