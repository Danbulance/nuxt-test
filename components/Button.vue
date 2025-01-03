<script setup>
const count = useState("count", () => 0);

const handleClick = () => {
  count.value++;
};
</script>

<template>
  <button @click="handleClick">Click me</button>
  <p>Count is {{ count }}</p>
</template>
