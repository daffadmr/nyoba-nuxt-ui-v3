<template>
  <div class="shadow">
    <div class="container mx-auto py-4 flex justify-between items-center">
      <h1>Ini Header</h1>
      <ul class="flex items-center gap-2">
        <li>Home</li>
        <li><USwitch v-model="theme" /></li>
      </ul>
    </div>
  </div>
</template>

<script setup>
const colorMode = useColorMode();
const theme = ref(false);

watchEffect(() => {
  if (theme.value === false) {
    colorMode.value = "light";
  } else {
    colorMode.value = "dark";
  }
});
</script>

<style></style>
