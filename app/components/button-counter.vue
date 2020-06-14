<!-- HTML -->
<template>
	<div>
		<button class="button is-success is-rounded" @click="contador">Haz clic</button>
	  	<div><b>{{numero}}</b></div>
	</div>
</template>

<!-- JS -->
<script>
export default {
  name: 'button-counter',
  data () {
    return {
     numero: 0
    }
  },
  methods: {
    contador: function (event) {
	  this.numero +=1;
      vue_app_00.numero -=1;	
	}
  },
  mounted() {
    console.log('Init <button-counter>');
  }	
}
</script>

<!-- CSS -->
<style scoped>
div {
	text-align: center;
}
div b{
	font-size:20px;
}
.button {
	font-size: 2em	
}
</style>
