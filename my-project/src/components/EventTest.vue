<template>
	<div>
		<button v-on:click="warn('Form cannot be submitted yet.', $event)">
		  Submit
		</button>
	</div>
</template>

<script>
	export default {
		methods: {
			warn: function (message, event) {
			    // 现在我们可以访问原生事件对象
			    if (event) {
			      event.preventDefault()
			    }
			    alert(message)
			  }
		}
	}
</script>

<style>
	
</style>
