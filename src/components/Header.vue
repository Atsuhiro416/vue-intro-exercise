<template>
  <header>
    <div class="header-content flex between">
      <h1 class="header-logo">estra inc.</h1>
      <nav class="header-nav">
        <ul>
          <li><a href="#">home</a></li>
          <li><a href="#">about</a></li>
          <li><a href="#">service</a></li>
          <li><a href="#">works</a></li>
          <li><a href="#">price</a></li>
          <li><a href="#">content</a></li>
        </ul>
      </nav>
    </div>

    <div id="hamburger" @click="hamburger" :class="{close: show}">
      <span></span>
      <span></span>
      <span></span>
    </div>

    <nav class="menu-content" :class="{open: show}">
      <p class="menu-title">estra inc.</p>
      <ul>
        <li><a href="#">home</a></li>
        <li><a href="#">about</a></li>
        <li><a href="#">service</a></li>
        <li><a href="#">works</a></li>
        <li><a href="#">price</a></li>
        <li><a href="#">contact</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  data() {
    return {
      show: false
    };
  },
  methods: {
    hamburger() {
      this.show = !this.show;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header {
  height: 70px;
  background: #000;
}

.header-logo {
  font-size: 20px;
  font-weight: bold;
  margin-left: 35px;
  color: #f2f2f2;
  line-height: 70px;
}

.header-nav li {
  display: inline-block;
  margin-right: 35px;
  font-size: 16px;
}

.header-nav a {
  color: #f2f2ff;
}

.menu-content {
  display: none;
}

@media screen and (max-width: 768px) {
  .wrap {
    margin-bottom: 5%;
  }
  #hamburger {
    width: 40px;
    height: 40px;
    position: absolute;
    cursor: pointer;
    z-index: 100;
    top: 15px;
    right: 20px;
    -webkit-transition: 0.4px;
    transition: 0.4px;
  }
  #hamburger span {
    position: absolute;
    left: 2px;
    display: block;
    width: 35px;
    height: 2px;
    background-color: #fff;
    -webkit-transition: 0.8s;
    transition: 0.8s;
  }
  #hamburger span:nth-last-of-type(1) {
    top: 10px;
  }
  #hamburger span:nth-last-of-type(2) {
    top: 20px;
  }
  #hamburger span:nth-last-of-type(3) {
    top: 30px;
  }
  .header-nav {
    display: none;
  }

  #hamburger.close {
    z-index: 999;
    position: fixed;
  }
  #hamburger.close span {
    background-color: #000;
  }

  #hamburger.close span:nth-of-type(1) {
    top: 20px;
    transform: rotate(225deg);
  }

  #hamburger.close span:nth-of-type(2) {
    opacity: 0;
  }
  #hamburger.close span:nth-of-type(3) {
    top: 20px;
    transform: rotate(-225deg);
  }
  .menu-content {
    display: block;
    width: 100%;
    height: 100%;
    text-align: center;
    transition: 0.2s;
    position: fixed;
    top: 0;
    left: -100%;
    background: #fff;
    color: #333333;
    /* box-shadow: 80px 0 rgba(38, 98, 213, 0.3); */
    z-index: 800;
  }
  .menu-content .menu-title {
    margin: 40px 20px;
    font-size: 2.2rem;
    color: #333333;
    text-align: center;
    font-weight: bold;
  }
  .menu-content li a {
    color: #333333;
    font-size: 200%;
    margin: 30px;
    padding: 5px;
    border-bottom: 0.5px solid #2662d5;
    text-decoration: none;
    display: block;
  }
  .menu-content li {
    width: 100%;
    text-align: center;
  }
  .menu-content.open {
    left: 0;
  }
}
</style>
