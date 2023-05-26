<template>
	<h1 v-text="title"></h1>
	<h2 v-text="subTitle"></h2>

	<button @click="editTitle('Hello world Edited')">Éditer title</button>
	<button @click="editSubTitle('80')">Éditer subTitle</button>
</template>

<script setup lang="ts">
import { ref } from "vue";

// const state = reactive({
// 	title: "Hello World!" as string,
// 	subTitle: 90 as string | number,
// });
const title = ref<string>("Hello World!");
const subTitle = ref<string|number>(90);

console.log(title.value);

const editTitle = (editTitle: string) => {
	title.value = editTitle;
};
const editSubTitle = (editSubTitle: string | number) => {
	subTitle.value = editSubTitle;
};
</script>
