<template>
  <a
    href="#"
    class="h-12 w-64 text-gray-300 flex items-center rounded-lg transition-colors duration-300 p-2
           hover:bg-gray-600"
  >
    <span class="w-8 h-8 bg-gray-700 rounded-full p-1 ml-1 mr-2 flex justify-center items-center
            transition duration-300 hover:bg-gray-600">
      <slot name="leftIcon"></slot>
    </span>

    <slot></slot>

    <span class="ml-auto">
      <slot name="rightIcon"></slot>
    </span>
  </a>
</template>
