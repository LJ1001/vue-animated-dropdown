<template>
  <div class="absolute w-64 custom-top custom-transform bg-gray-800 overflow-hidden
              border border-gray-700 border-p-4 rounded-lg">
    <div v-if="activeMenu === 'main'">
      <DropdownItem>
        <template>
          My Profile
        </template>
      </DropdownItem>

      <DropdownItem>
        <template #leftIcon>
          <Cog />
        </template>
        <template>
          Settings
        </template>
        <template #rightIcon>
          <Chevron />
        </template>
      </DropdownItem>
    </div>
  </div>
</template>

<script>
import DropdownItem from './DropdownItem';
import Cog from './icons/Cog';
import Chevron from './icons/Chevron';

export default {
  name: 'DropDownMenu',
  components: {
    DropdownItem,
    Cog,
    Chevron,
  },
  data() {
    return {
      activeMenu: 'main',
    };
  },
  methods: {
    setActiveMenu(menu) {
      this.activeMenu = menu;
    },
  },
};
</script>

<style scoped>
  .custom-top {
    top: 58px;
  }
  .custom-transform {
    transform: translateX(-45%);
  }
</style>
