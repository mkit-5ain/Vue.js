<template>
    <header id="header" class="header">
        <section class="text__toggle">
            <div class="text__inner">
                <span class="text">
                    <span>W</span>
                </span>
                <span class="text">
                    <span>e</span>
                </span>
                <span class="text">
                    <span>l</span>
                </span>
                <span class="text">
                    <span>c</span>
                </span>
                <span class="text">
                    <span>o</span>
                </span>
                <span class="text">
                    <span>m</span>
                </span>
                <span class="text">
                    <span>e</span>
                </span>
                <span class="text">
                    <span>t</span>
                </span>
                <span class="text">
                    <span>o</span>
                </span>
                <span class="text">
                    <span>t</span>
                </span>
                <span class="text">
                    <span>h</span>
                </span>
                <span class="text">
                    <span>i</span>
                </span>
                <span class="text">
                    <span>s</span>
                </span>
                <span class="text">
                    <span>p</span>
                </span>
                <span class="text">
                    <span>l</span>
                </span>
                <span class="text">
                    <span>a</span>
                </span>
                <span class="text">
                    <span>c</span>
                </span>
                <span class="text">
                    <span>e</span>
                </span>
                <span class="text">
                    <span>.</span>
                </span>
            </div>
            <div class="text__inner">
                <span class="text">
                    <span>W</span>
                </span>
                <span class="text">
                    <span>e</span>
                </span>
                <span class="text">
                    <span>l</span>
                </span>
                <span class="text">
                    <span>c</span>
                </span>
                <span class="text">
                    <span>o</span>
                </span>
                <span class="text">
                    <span>m</span>
                </span>
                <span class="text">
                    <span>e</span>
                </span>
                <span class="text">
                    <span>t</span>
                </span>
                <span class="text">
                    <span>o</span>
                </span>
                <span class="text">
                    <span>t</span>
                </span>
                <span class="text">
                    <span>h</span>
                </span>
                <span class="text">
                    <span>i</span>
                </span>
                <span class="text">
                    <span>s</span>
                </span>
                <span class="text">
                    <span>p</span>
                </span>
                <span class="text">
                    <span>l</span>
                </span>
                <span class="text">
                    <span>a</span>
                </span>
                <span class="text">
                    <span>c</span>
                </span>
                <span class="text">
                    <span>e</span>
                </span>
                <span class="text">
                    <span>.</span>
                </span>
            </div>
        </section>
        <img class="logo" src="@/assets/image/common/full-logo.svg" alt="limjunesu">
        <ul class="menu__list">
            <li class="list scale"><router-link to="/">Home</router-link></li>
            <li class="list scale"><router-link to="/contact">Contact</router-link></li>
            <li class="list scale"><router-link to="/Experience">Experience</router-link></li>
        </ul>
        <button class="etc--btn scale">
            <a href="https://github.com/mkit-5ain" target="_blank">
                <img src="@/assets/image/common/github.png" alt="">
            </a>
        </button>
    </header>
</template>

<script>
    export default {
        name: 'Header',
        mounted: function () {
            this.scroll();
        },
        methods: {
            scroll: function () {
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
<style lang="scss"></style>
