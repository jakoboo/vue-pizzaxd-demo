<template>
  <div id="app">
    <header>
      <menu class="container">
        <h1>PizzaXD</h1>

        <ul>
          <li><a href="#menu">Menu</a></li>
          <li><a href="#contact">Contact</a></li>
          <li><a href="#find-us">Find Us</a></li>
        </ul>
      </menu>
    </header>
    <Hero />
    <Menu :menu="menu_data" />
  </div>
</template>

<script>
import Hero from './components/Hero'
import Menu from './components/Menu'

import { menu_data } from './assets/menu_data.json'

export default {
  name: 'App',
  components: {
    Hero,
    Menu
  },
  data: function() {
    return {
      menu_data
    };
  }
}
</script>

<style lang="scss">
@import url(https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap);

*,
*::after,
*::before {
  box-sizing: border-box;
}

html {
  font-size: clamp(16px, 1vw, 20px)
}

body {
  margin: 0;

  color: white;
  background-color: #0C070B;
}

.container {
  margin: auto;
  padding: 0 1.5rem;
  width: 100%;

  @media screen and (min-width: 920px) {
    width: 920px;
  }

  @media screen and (min-width: 1200px) {
    width: 95%;
  }
}

header {
  height: 70px;
  width: 100%;

  position: fixed;
  top: 0;
  z-index: 99;

  background-color: #0C070B;

  menu {
    display: flex;
    align-content: center;
  }

  h1 {
    display: left;
  }

  ul {
    display: left;
    list-style: none;

    li {
      float: left;

      a {
        padding: .5rem;
        color: white;
        text-decoration: none;
      }
    }
  }
}

#app {
  font-family: 'Montserrat', Arial, Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
