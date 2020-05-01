<template>
  <nav class=" h-16 bg-gray-800 border-b-2 border-gray-700 px-4">
    <ul class="max-w-full h-full flex justify-end">
      <slot></slot>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'NavBar',
};
</script>
