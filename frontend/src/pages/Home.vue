<template>
    <section class="top__banner">
        <div class="top--marquee">
            <div class="text text-stroke">WELCOME TO THIS PLACE</div>
            <div class="text text-stroke">WELCOME TO THIS PLACE</div>
            <div class="text text-stroke">WELCOME TO THIS PLACE</div>
            <div class="text text-stroke">WELCOME TO THIS PLACE</div>
        </div>
        <img class="banner" src="@/assets/image/common/hedaer_bg.jpg" alt="">
        <!-- <p class="banner--text">
            <span class="text">
                <span class="text--inner">Always</span>
            </span>
            <span class="text">
                <span class="text--inner">Improve,</span>
            </span>
            <span class="text">
                <span class="text--inner">Never</span>
            </span>
            <span class="text">
                <span class="text--inner">Change.</span>
            </span>
        </p> -->
        <div class="banner__marquee--text">
            <div class="text text-stroke">WELCOME TO THIS PLACE</div>
            <div class="text text-stroke">WELCOME TO THIS PLACE</div>
            <div class="text text-stroke">WELCOME TO THIS PLACE</div>
            <div class="text text-stroke">WELCOME TO THIS PLACE</div>
        </div>
    </section>
    <section class="section-title">
        DISCOVER
        <div>#projects</div>
    </section>
    <section class="loading">
        <div class="loading--circle"></div>
        <div class="loading--circle"></div>
        <div class="loading--circle"></div>
    </section>
    <section id="scroll-handler" class="prologue">
        <div class="prologue--text text-stroke effect-dot">
            hello
            <span class="inner-dot"></span>
        </div>
        <div class="prologue--text text-stroke effect-line">
            <span>my style</span>
        </div>
        <div class="prologue--text text-stroke effect-blur">
            <span>trust me.</span>
        </div>
    </section>
</template>

<script>


export default {
    name: 'Home',
    mounted:function () {
        this.sectionHandle();
    },
    methods: {
        sectionHandle: function() {
            const target = document.getElementById('scroll-handler');
            const sectionTopValue = target.getBoundingClientRect();
            const relativeTop = sectionTopValue.top + 600;
            window.addEventListener('scroll', function () {
                if (window.scrollY > relativeTop) {
                    target.classList.add('active');
                }
            });
        }
    }
}
</script>
