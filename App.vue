<template>
  <div id="app" class="app">
    <header class="title">
      <h1>Project</h1>
      <h2>Do some cool stuff</h2>
      <h2>做一点微小的贡献</h2>
    </header>
    <div class="container">
      <ul class="links">
        <li><a href="http://geekplux.com/archives">Blog</a></li>
        <li><a href="http://geekplux.com/wiki">Wiki</a></li>
        <li><a href="https://github.com/geekplux">GitHub</a></li>
        <li><a href="https://about.geekplux.com">About</a></li>
        <li><a href="https://donate.geekplux.com">Donate</a></li>
      </ul>
      <div class="projects">
        <div class="project panel">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'app',
  }
</script>

<style>
  body {
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    font-family: -apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Oxygen,Ubuntu,Cantarell,"Open Sans","Helvetica Neue",sans-serif;
    -moz-font-feature-settings: "liga" on;
  }

  h1, h2, h3, h4, h5 {
    font-weight: 100;
  }

  .links {
    position: fixed;
    top: 50%;
  }

  li {
    list-style: none;
    margin-bottom: 10px;
  }

  li a {
    font-size: 16px;
    color: #939393;
    font-family: monospace;
    transition: .5s;
  }
  li:hover a {
    color: #262626;
    font-size: 18px;
  }


  header {
    text-align: center;
  }

  h1 {
   font-family: serif;
   font-size: 72px;
  }

  h2 {
    font-size: 20px;
    margin: 0 0 10px 0;
  }
</style>
