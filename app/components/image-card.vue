<!-- HTML -->
<template>
	<figure class="is-flex is-paddingless">	
		<img v-bind:id="'image_#' + id" v-bind:src="imagen" v-bind:alt="titulo" />
		<figcaption>{{ titulo }}</figcaption>
	</figure>
</template>

<!-- JS -->
<script>
    export default {
        props: {
			id: String,
            imagen: String,
            titulo: String
        },
		mounted(){
			console.log("Init <image-card>");		
		}
    }
</script>

<!-- SCSS -->
<style scoped lang="scss">

	/* Helpers */
	@import "helpers";

	/* Main styles */
	figure {
		@extend %item_box;
		margin: $xs_separation;
		flex-direction: column;
		&:hover{
			cursor: pointer; 
		}

		@media (max-width:768px){
			height:420px;
			margin: $md_separation;		
		}		
	}
	figure:hover{
		border-color: darken($light-black, 5%);
		background-color: darken($white, 5%);
		figcaption {
			background-color: darken($light-gray, 5%);		
		}	
	}

	figcaption {
		color: $light-black; 
		font-size: 20px; 
		border-top: 1px solid gray;	
		background-color: $light-gray; 
		text-align: center;
		padding: $sm_separation;

		@media (max-width:768px){
			padding: $xs_separation;			
		}
	}
	img { 
		width: 150px; 
		height: auto;
		margin: auto;
	}
</style>
