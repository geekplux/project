<template>
  <div id="app" class="app">
    <header>
      <h1 class="title">Project</h1>
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
        <div class="project panel" v-for="p in projects">
          <h3 class="project-title title">{{p.title}}</h3>
          <p class="project-bio">{{p.bio}}</p>
          <a class="project-link" :href="p.link">{{p.link}}</a>
          <div class="project-badges">
          </div>
          <div class="project-image">
            <img alt="" :src="p.img"/>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'app',
    data() {
      return {
        projects: [{
            title: 'markvis',
            bio: 'make visualization in markdown',
            img: './markvis-preview.png',
            link: 'https://github.com/geekplux/markvis'
          }, {
            title: 'netjsongraph.js',
            bio: 'To visualize network topology using the NetJSON format',
            img: './netjsongraph-preview.png',
            link: 'https://github.com/netjson/netjsongraph.js'
          }, {
            title: 'Typing',
            bio: 'a pure and fresh Hexo theme',
            img: './typing-preview.png',
            link: 'https://github.com/geekplux/hexo-theme-typing'
          }, {
            title: 'Basic visualization in Unity',
            bio: 'Basic 2D visualization in Unity',
            img: './unity-preview.png',
            link: 'https://github.com/geekplux/Basic-Visualization-in-Unity'
          }]
      }
    }
  }
</script>

<style>
  * {
    box-sizing: border-box;
  }

  body {
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    font-family: -apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Oxygen,Ubuntu,Cantarell,"Open Sans","Helvetica Neue",sans-serif;
    -moz-font-feature-settings: "liga" on;
  }

  body, .app {
    width: 100%;
  }

  h1, h2, h3, h4, h5 {
    font-weight: 200;
  }

  .links {
    position: fixed;
    top: 50vh;
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
    padding-top: 10vh;
    text-align: center;
  }

  .title {
    font-family: serif;
  }

  h1 {
   font-size: 72px;
  }

  h2 {
    font-size: 20px;
    margin: 0 0 10px 0;
  }


  .container {
    width: 100%;
  }

  .projects {
    width: 60%;
    margin: 10vh auto 0 auto;
  }

  .project {
    border-radius: 5px;
    margin-bottom: 10vh;
  }

  .project-title {
    font-size: 25px;
    font-weight: bolder;
  }

  .project-bio {
    color: #939393;
    font-weight: 200;
  }

  .project-link {
    color: #000;
    font-style: italic;
    text-decoration: none;
  }

  .project-badges {
    padding: 5px;
    border-bottom: 1px solid #939393;
  }

  .project-image img {
    width: 100%;
  }
</style>
