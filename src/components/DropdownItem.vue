<template>
  <a
    href="#"
    class="h-12 text-gray-300 flex items-center rounded-lg transition-colors duration-300 p-2
           hover:bg-gray-600"
  >
    <span class="">
      <slot name="leftIcon"></slot>
    </span>

    <slot></slot>

    <span class="ml-auto">
      <slot name="rightIcon"></slot>
    </span>
  </a>
</template>
