<template>
	<div class="son">
		<h1>{{title}}</h1>
		<p>{{$attrs.text}}</p>
		<button v-bind="$attrs" v-on="$listeners" v-if="$listeners['submit-value']" @click="keller">提交</button>
	</div>
</template>
  
  <script>
export default {
	name: "HelloWorld",
	inheritAttrs: false,
	props: {
		title: {
			type: String,
			default: ""
		}
	},
	data() {
		return {
			msg: "Vue.js"
		};
	},
	methods: {
		keller() {
			this.$emit("submit-value", "fuck");
		}
	},
	mounted() {
		console.log("$attrs", this.$attrs);
		console.log("$listeners", this.$listeners);
	}
};
</script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
</style>
  