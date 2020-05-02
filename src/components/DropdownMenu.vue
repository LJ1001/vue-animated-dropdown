<template>
  <div class="absolute w-64 custom-top custom-transform bg-gray-800 overflow-hidden
              border border-gray-700 border-p-4 rounded-lg flex">
    <transition name="menu-primary">
      <div v-if="activeMenu === 'main'">
        <DropdownItem>
          <template>
            My Profile
          </template>
        </DropdownItem>

        <DropdownItem @click.native="setActiveMenu('settings')">
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
    </transition>

    <transition name="menu-secondary">
      <div v-if="activeMenu === 'settings'">
        <DropdownItem @click.native="setActiveMenu('main')">
          <template #leftIcon>
            <Arrow />
          </template>
        </DropdownItem>
        <DropdownItem >
          <template>
            Settings
          </template>
        </DropdownItem>
      </div>
    </transition>
  </div>
</template>

<script>
import DropdownItem from './DropdownItem';
import Arrow from './icons/Arrow';
import Cog from './icons/Cog';
import Chevron from './icons/Chevron';

export default {
  name: 'DropDownMenu',
  components: {
    DropdownItem,
    Arrow,
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
  .menu-primary-enter {
    position: absolute;
    transform: translateX(-110%);
  }
  .menu-primary-enter-to {
    position: absolute;
    transform: translateX(0%);
  }
  .menu-primary-enter-active {
    transition: all 0.5s ease;
  }
  .menu-primary-leave {
    position: absolute;
    transform: translateX(0%);
  }
  .menu-primary-leave-to {
    transform: translateX(-110%);
  }
  .menu-primary-leave-active {
    transition: all 0.5s ease;
  }
  .menu-secondary-enter {
    position: absolute;
    transform: translateX(110%);
  }
  .menu-secondary-enter-to {
    position: absolute;
    transform: translateX(0%);
  }
  .menu-secondary-enter-active {
    transition: all 0.5s ease;
  }
  .menu-secondary-leave {
    position: absolute;
    transform: translateX(0%);
  }
  .menu-secondary-leave-to {
    transform: translateX(110%);
  }
  .menu-secondary-leave-active {
    transition: all 0.5s ease;
  }
</style>
