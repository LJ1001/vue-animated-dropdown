<template>
  <div id="app">
    <NavBar>
      <NavItem>
        <template #icon>
          <Arrow/>
        </template>
      </NavItem>

      <NavItem>
        <template #icon>
          <Bell/>
        </template>
      </NavItem>

      <NavItem>
        <template #icon>
          <Messenger/>
        </template>
      </NavItem>

      <NavItem>
        <template #icon>
          <Caret/>
        </template>
        <template #dropdown>
          <!-- <p>Toggle</p> -->
        </template>
      </NavItem>
    </NavBar>
  </div>
</template>

<script>
import NavBar from './components/NavBar';
import NavItem from './components/NavItem';
import Arrow from './components/icons/Arrow';
import Bell from './components/icons/Bell';
import Messenger from './components/icons/Messenger';
import Caret from './components/icons/Caret';

export default {
  name: 'App',
  components: {
    NavBar,
    NavItem,
    Arrow,
    Bell,
    Messenger,
    Caret,
  },
};
</script>
