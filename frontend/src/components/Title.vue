<template>
    <section class="section-title">
        DISCOVER
        <div>#projects</div>
    </section>
</template>
<script>
    export default {
        name: 'Title'
    }
</script>
<style scope lang="scss">
    $black-color: #1d1d1b;
    .section-title {
    	padding: 10vw 34vw;
    	font-size: 5.56vw;
    	font-weight: bold;
    	color: #111;
    	text-align: center;
    	letter-spacing: -7px;
    	text-transform: uppercase;
    	div {
    		position: relative;
    		color: #fff;
    		transform: rotate(1.2deg);
    		&:after {
    			content: '';
    			position: absolute;
    			top: 0px;
    			left: 0px;
    			width: 100%;
    			height: 100%;
    			background: $black-color;
    			z-index: -1;
    		}
    	}
    }
</style>
