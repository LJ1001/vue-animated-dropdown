<template>
  <div id="app">
    <NavBar>
      <NavItem>
        <template #icon>
          <Arrow/>
        </template>
      </NavItem>

      <NavItem>
        <template #icon>X</template>
      </NavItem>

      <NavItem>
        <template #icon>X</template>
      </NavItem>
    </NavBar>
  </div>
</template>

<script>
import NavBar from './components/NavBar';
import NavItem from './components/NavItem';
import Arrow from './components/icons/Arrow';

export default {
  name: 'App',
  components: {
    NavBar,
    NavItem,
    Arrow,
  },
};
</script>
