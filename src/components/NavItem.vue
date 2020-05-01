<template>
  <li class="w-12 flex justify-center items-center">
    <a
      href="#"
      class="w-8 h-8 bg-gray-700 rounded-full p-1 m-1 flex justify-center items-center
            transition duration-300 hover:bg-gray-600"
      @click="toggleOpen">
      <slot name="icon"></slot>
    </a>

    <slot v-if="open" name="dropdown"></slot>
  </li>
</template>

<script>
export default {
  name: 'NavItem',
  data() {
    return {
      open: false,
    };
  },
  methods: {
    toggleOpen() {
      this.open = !this.open;
    },
  },
};
</script>
