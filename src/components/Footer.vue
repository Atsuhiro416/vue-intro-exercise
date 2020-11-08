<template>
  <footer>
    <div class="footer-content flex between">
      <h1 class="footer-logo">estra inc.</h1>
      <nav class="footer-nav">
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
    <small>Copyright 2019 estra inc. All Rights Reserved.</small>
  </footer>
</template>

<script>
export default {

}
</script>

<style scoped>
footer {
  height: 100px;
  background: #000;
}

footer small {
  color: #f2f2f2;
  display: block;
  text-align: center;
}

.footer-logo {
  font-size: 20px;
  font-weight: bold;
  margin-left: 35px;
  color: #f2f2f2;
  line-height: 70px;
}

.footer-nav li {
  display: inline-block;
  margin-right: 35px;
  font-size: 16px;
}

.footer-nav a {
  color: #f2f2ff;
}

@media screen and (max-width: 768px) {

  .footer-logo {
    margin: 0 auto;
  }
  .footer-nav {
    display: none;
  }
}
</style>
