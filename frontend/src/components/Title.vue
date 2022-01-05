<template>
    <section class="section-title">
        {{ title }}
        <div>{{ nameTitle }}</div>
    </section>
</template>
<script>
    export default {
        name: 'Title',
        data () {
            return {
                title: 'discover',
                nameTitle: '#projects'
            }
        }
    }
</script>
<style scope lang="scss">
    $black-color: #1d1d1b;
    .section-title {
    	padding: 10vw 34vw;
    	font-size: 5.56vw;
    	font-weight: bold;
    	color: #1d1d1b;
    	text-align: center;
    	letter-spacing: -7px;
    	text-transform: uppercase;
        &.active {
            div { color: #cdc6be; transform: rotate(1.2deg);
                &:after { width: 100%; }
            }
        }
    	div { position: relative; color: #fff; transition: 1s ease; transform: rotate(0deg);
    		&:after {
    			content: '';
    			position: absolute;
    			top: 0px;
    			left: 0px;
    			width: 0%;
    			height: 100%;
    			background: $black-color;
    			z-index: -1;
                transition: 1s ease;
    		}
    	}
    }
</style>
