<template>
    <section class="typograph">
        JUNESU
    </section>
    <ui-title class="scroll-handler"></ui-title>
    <section class="top__banner">
        <div class="top--marquee">
            <div class="text text-stroke">WELCOME TO THIS PLACE</div>
            <div class="text text-stroke">WELCOME TO THIS PLACE</div>
            <div class="text text-stroke">WELCOME TO THIS PLACE</div>
            <div class="text text-stroke">WELCOME TO THIS PLACE</div>
        </div>
        <!-- <div class="banner__marquee--text">
            <div class="text text-stroke">WELCOME TO THIS PLACE</div>
            <div class="text text-stroke">WELCOME TO THIS PLACE</div>
            <div class="text text-stroke">WELCOME TO THIS PLACE</div>
            <div class="text text-stroke">WELCOME TO THIS PLACE</div>
        </div> -->
    </section>
    <ui-title class="scroll-handler"></ui-title>
    <section class="scroll-handler prologue">
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
    <section class="loading">
        <div class="loading--circle"></div>
        <div class="loading--circle"></div>
        <div class="loading--circle"></div>
    </section>
    <section class="card">
        <div class="card__marquee--text marquee--2">
            <div class="text text-stroke">ALWAYS IMPROVE</div>
            <div class="text text-stroke">ALWAYS IMPROVE</div>
            <div class="text text-stroke">ALWAYS IMPROVE</div>
            <div class="text text-stroke">ALWAYS IMPROVE</div>
        </div>
        <div class="card__marquee--text marquee--3">
            <div class="text text-stroke">ALWAYS IMPROVE</div>
            <div class="text text-stroke">ALWAYS IMPROVE</div>
            <div class="text text-stroke">ALWAYS IMPROVE</div>
            <div class="text text-stroke">ALWAYS IMPROVE</div>
        </div>
        <div class="card--image"><img src="@/assets/image/common/card.jpg" alt=""></div>
        <div class="card__info--text">
            <p>ALWAYS IMPROVE,</p>
            <p>NEVER</p>
            <p>CHANGE. LET'S</p>
            <p>NAVIGATE</p>
            <p>IDENTITY, SET</p>
            <p>OUR</p>
            <p>IMAGINATION</p>
            <p>FREE AND</p>
            <p>BECOME US AS</p>
            <p>WE WISH.</p>
            <div class="inner--text">
                <p>As humans, we celebrate beauty as</p>
                <p>something unique. We believe self-</p>
                <p>expression is about embracing who we are,</p>
                <p>letting our imagination run free and our</p>
                <p>true colors shine through.</p>
            </div>
        </div>
    </section>
    <section class="appeal">
        <p class="appeal--text left--direction">
            <span class="text-stroke">WANT TO KNOW</span>
        </p>
        <p class="appeal--text right--direction">
            <span class="text-stroke">WHAT<img class="appeal--image" src="@/assets/image/common/junesu.png" alt="">MAKES</span>
        </p>
        <p class="appeal--text left--direction">
            <span class="text-stroke">LJS SO LJS?</span>
        </p>
    </section>
    <section class="work">
        <div class="work__list">
            <a class="work__list--link link" href=""></a>
            <img class="work__list--img" src="" alt=""/>
            <div class="work__list--marquee">
                <div class="marquee--text">
                    <div class="text">1</div>
                    <div class="text">2</div>
                    <div class="text">3</div>
                    <div class="text">4</div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    import Title from '@/components/Title.vue';

    import gsap from 'gsap';
    import ScrollTrigger from "gsap/ScrollTrigger";
    gsap.registerPlugin(ScrollTrigger);

    export default {
        name: 'Home',
        data () {
            return {
                title: '',
                nameTitle: ''
            }
        },
        components: {
            'ui-title': Title
        },
        mounted:function () {
            // this.getTodos();
            window.addEventListener("scroll", this.sectionHandle);

            gsap.to(".left--direction", {
                xPercent: 20,
                ease: "none",
                scrollTrigger: {
                    trigger: ".appeal",
                    scrub: 2,
                    start: "top center"
                },
            });

            gsap.to(".right--direction", {
                xPercent: -20,
                ease: "none",
                scrollTrigger: {
                    trigger: ".appeal",
                    scrub: 2,
                    start: "top center"
                },
            });

            gsap.to(".card--image", {
                xPercent: -7,
                ease: "none",
                scrollTrigger: {
                    trigger: ".card",
                    scrub: 1,
                    start: "top center"
                },
                rotation: -2
            });

            gsap.to(".card__info--text", {
                xPercent: 7,
                ease: "none",
                scrollTrigger: {
                    trigger: ".card",
                    scrub: 1,
                    start: "top center"
                },
                rotation: 2
            });

        },
        methods: {
            // sectionHandle: function() {
            //     const target = document.querySelectorAll('.scroll-handler');
            //     const sectionTopValue = target.getBoundingClientRect();
            //     const relativeTop = sectionTopValue.top - 500;
            //     let i;
            //     window.addEventListener('scroll', function () {
            //         for (i = 0; i < target.length; i++) {
            //             if (window.scrollY > relativeTop) {
            //                 target[i].classList.add('active');
            //             }
            //         }
            //     });
            // }
            sectionHandle: function () {
                let target = document.querySelectorAll(".scroll-handler");
                let targetPosition;
                for ( let i = 0; i < target.length; i++ ) {
                    targetPosition = target[i].getBoundingClientRect().top;
                    let screenSize = window.innerHeight;
                    if ( targetPosition < screenSize && !target[i].classList.contains("active") ) {
                        target[i].classList.add("active");
                    }
                }
            }
        }
    }
</script>
