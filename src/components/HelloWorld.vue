<template>
	<h1 v-text="state.title"></h1>
	<h2 v-text="state.subTitle"></h2>

	<button @click="editTitle('Hello world Edited')">Éditer title</button>
	<button @click="editSubTitle('80')">Éditer subTitle</button>
</template>

<script setup lang="ts">
import { reactive } from "vue";

const state = reactive({
	title: "Hello World!" as string,
	subTitle: 90 as string | number,
});

const editTitle = (editTitle: string) => {
	state.title = editTitle;
};
const editSubTitle = (editSubTitle: string | number) => {
	state.subTitle = editSubTitle;
};
</script>
