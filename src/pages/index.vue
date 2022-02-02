<script setup>
import { reactive } from "vue";

import IncrementButton from "~/components/IncrementButton.vue";

const data = reactive({
	number: 0
});

function incrementNumber() {
	data.number++;
}
</script>

<template>
	<div class="flex justify-center items-center h-screen">
		<div class="text-3xl text-center">
			<p class="my-6">
				Value: {{ data.number }}
			</p>
			<IncrementButton @click="incrementNumber" />
		</div>
	</div>
</template>
