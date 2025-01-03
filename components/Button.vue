<script setup>
const count = useState("count", () => 0);

const handleClick = () => {
  count.value++;
};
</script>

<template>
  <div class="bg-blue-300 text-xl">
    <button @click="handleClick">Click me</button>
    <p>Count is {{ count }}</p>
  </div>
</template>
