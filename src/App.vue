<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="scss">
input.def {
  padding: 5px 6px;
  border: 1px solid gainsboro;
  border-radius: 2px;
  font-size: 16px;
}
* {
  font-family: arial;
  font-size: 15px;
  color: #484848;
  outline: none;
}
body {
}
body, html {
  margin: 0;
  padding: 0;
}
h1,h2,h3,h4,h5,ul,li,p {
  padding: 0;
  margin: 0;
}
li {
  list-style: none;
}
a, a:hover, a:visited, a:active, a:link {
  color: black;
  text-decoration: none;
}
</style>
