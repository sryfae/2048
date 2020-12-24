<template>
  <router-view/>
</template>

<style lang="less">
html, body, header, footer, nav, section, aside, article, div, ol, ul, li, dl, dt, dd, p, blockquote, figure, figcaption, fieldset, legend, pre, iframe, hr, h1, h2, h3, h4, h5, h6 {
  margin: 0;
  padding: 0;
  border: none;
  line-height: 1;
  font-style: normal;
  font-weight: normal;
  box-sizing: border-box;
  -webkit-tap-highlight-color:transparent;
  -webkit-font-smoothing: antialiased;
  &:hover{
      outline: none;
  }
}
html, body {
  max-width: 100vw;
  width: 100%;
  overflow-x: hidden;
  overflow-y: auto;
}
html {
 min-height: 100%;
 font-size: 13.33vw;
}
body {
  padding: 0;
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

</style>
