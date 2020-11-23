<template>
	<section class="container">
		<h2>My Course Goal</h2>
		<h3 v-if="show">{{ goal }}</h3>
		<button @click="toggle">Toggle Goal</button>
	</section>
</template>

<script>
// import { reactive } from 'vue';
export default {
	// setup() {
	// => Separate refs
	// const goal = ref('Learn more about vue');
	// const show = ref(true);
	// function toggle() {
	// 	show.value = !show.value;
	// }
	// return { goal, show, toggle };
	//=> Ref Object
	// const object = ref({
	// 	show: false,
	// 	goal: 'learn more about vue3',
	// });
	// function toggle() {
	// 	object.value.show = !object.value.show;
	// }
	// return { object, toggle };
	// => Reactive Object
	// 	const object = reactive({
	// 		show: true,
	// 		goal: 'learn more about vue3',
	// 	});
	// 	function toggle() {
	// 		object.show = !object.show;
	// 	}
	// 	return { object, toggle };
	// },

	// ------Options-API-----

	data() {
		return {
			show: true,
			goal: 'learn more about vue3',
		};
	},
	methods: {
		toggle() {
			this.show = !this.show;
		},
	},
};
</script>

<style>
* {
	box-sizing: border-box;
}

html {
	font-family: sans-serif;
}

body {
	margin: 0;
}

.container {
	margin: 3rem auto;
	max-width: 30rem;
	border-radius: 12px;
	box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
	padding: 1rem;
	text-align: center;
}
</style>