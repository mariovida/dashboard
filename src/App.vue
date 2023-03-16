<template>
  <div id="app">
    <nav>
      <div class="wrapper">
        <router-link to="/">Home</router-link>
        <router-link to="/about"><font-awesome-icon icon="fa-solid fa-info" />About</router-link>
        <b-dropdown id="dropdown-1" text="More">
          <button v-b-toggle.collapse-1>Toggle Collapse<font-awesome-icon icon="fa-solid fa-chevron-down" /></button>
          <b-collapse id="collapse-1">
            <b-card>
              <a href="./"><font-awesome-icon icon="fa-solid fa-house" />Home</a>
              <a href="./about"><font-awesome-icon icon="fa-solid fa-info" />About</a>
            </b-card>
          </b-collapse>
          <b-dropdown-item href="./about">About</b-dropdown-item>
        </b-dropdown>
        <a href="/more">More</a>
      </div>
    </nav>
    <router-view/>
  </div>
</template>

<style lang="scss">
  @import './styles.scss';
</style>
