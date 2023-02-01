<template>
	<div>
		<button class="btn btn-success" @click="toggleColorScheme">Toggle Color Scheme</button>
	</div>
</template>

<script setup>

const toggleColorScheme = () => {
	if (getComputedStyle(document.documentElement).getPropertyValue("--color-background") === "#ffffff") {
		document.documentElement.style.setProperty("--color-background", "#181818");
		document.documentElement.style.setProperty("--color-background-soft", "#222222");
		document.documentElement.style.setProperty("--color-background-mute", "#282828");
		document.documentElement.style.setProperty("--color-border", "rgba(84, 84, 84, 0.48)");
		document.documentElement.style.setProperty("--color-border-hover", "rgba(84, 84, 84, 0.65)");
		document.documentElement.style.setProperty("--color-heading", "#ffffff");
		document.documentElement.style.setProperty("--color-text", "rgba(235, 235, 235, 0.64)");
	} else {
		document.documentElement.style.setProperty("--color-background", "#ffffff");
		document.documentElement.style.setProperty("--color-background-soft", "#f8f8f8");
		document.documentElement.style.setProperty("--color-background-mute", "#f2f2f2");
		document.documentElement.style.setProperty("--color-border", "rgba(60, 60, 60, 0.12)");
		document.documentElement.style.setProperty("--color-border-hover", "rgba(60, 60, 60, 0.29)");
		document.documentElement.style.setProperty("--color-heading", "#2c3e50");
		document.documentElement.style.setProperty("--color-text", "#2c3e50");
	}
}

</script>