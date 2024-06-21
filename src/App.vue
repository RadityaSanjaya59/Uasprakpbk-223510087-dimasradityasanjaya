<template>
  <div id="app">
    <div class="content">
      <router-view />
    </div>
  </div>
</template>

<script>
export default {
  name: 'App'
};
</script>

<style>
:root {
  --main-font-family: 'Arial, sans-serif';
  --main-text-color: #000000;
  --main-link-color: #000000;
  --main-link-hover-color: #000000;
  --background-color: #ffffff;
  --primary-color: #000000;
  --secondary-color: #ff9800;
}

body {
  margin: 0;
  font-family: var(--main-font-family);
  color: var(--main-text-color);
  background-color: var(--background-color);
  overflow: hidden;
}

#app {
  position: relative;
  width: 100%;
  height: 100vh;
  overflow: hidden;
}

.content {
  position: relative;
  z-index: 1;
  padding: 20px;
}

a {
  color: var(--main-link-color);
  text-decoration: none;
}

a:hover {
  color: var(--main-link-hover-color);
}

* {
  box-sizing: border-box;
}

h1, h2, h3, h4, h5, h6 {
  font-family: var(--main-font-family);
  color: var(--primary-color);
}

button {
  font-family: var(--main-font-family);
  color: #fff;
  background-color: var(--primary-color);
  border: none;
  padding: 10px 20px;
  cursor: pointer;
}

button:hover {
  background-color: var(--secondary-color);
}

input, textarea {
  font-family: var(--main-font-family);
  border: 1px solid var(--primary-color);
  padding: 10px;
  width: 100%;
}
</style>
