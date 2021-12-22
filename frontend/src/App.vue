<template>
    <ui-header/>
    <article id="container">
        <router-view/>
    </article>
    <div class="cursor"></div>
</template>
<script>
    import Header from '@/components/Header.vue';
    export default {
        name: 'App',
        components: {
            'ui-header': Header
        },
        mounted: function () {
            this.cursorPointer(),
            this.cursorActive();
        },
        methods: {
            cursorPointer() {
                const cursor = document.querySelector(".cursor");

                document.addEventListener('mousemove', (e) => {
                    const mouseX = e.clientX;
                    const mouseY = e.clientY;
                    cursor.style.left = mouseX + 'px';
                    cursor.style.top = mouseY + 'px';
                    cursor.style.opacity = '1';
                });

            },
            cursorActive() {
                const cursor = document.querySelector(".cursor");
                const cursorLink = document.querySelectorAll(".scale");

                cursorLink.forEach(ele => ele.addEventListener("mouseover", () => {
                    cursor.style.transform = 'scale(3.2)';
                }));

                cursorLink.forEach(ele => ele.addEventListener("mouseout", () => {
                    cursor.style.transform = 'scale(1)';
                }));
            }
        }
    }
</script>
<style lang="scss">
    @import '@/assets/sass/common.scss';
</style>
