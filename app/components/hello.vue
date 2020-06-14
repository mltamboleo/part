<!-- HTML -->
<template>
	<div class="contenedor">
		<p>{{ msg }}</p>	
	</div>
</template>

<!-- JS -->
<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: 'Texto del componente "hello.vue"'
    }
  },
  mounted(){
  	console.log("Init <hello>");
  }
}
</script>

<!-- CSS -->
<style scoped>
.contenedor {
	border: 1px solid black;
	background-color: #cccccc;
	width: 50%;
	margin: 10px auto;	
}
.contenedor p {
  	font-size: 2em;
  	text-align: center;
}
</style>
