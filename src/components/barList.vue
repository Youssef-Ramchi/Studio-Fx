<template>
  <nav>
    <h2>Studio<span class="green">FX</span></h2>
    <ul>
      <li><router-link to="/">Home</router-link></li>
      <li>About</li>
      <li>Help</li>
      <li>Contact Us</li>
    </ul>
  </nav>
</template>

<script></script>

<style scoped lang="scss">
nav {
  border-bottom: 0.2px solid rgb(94, 94, 94);
  margin: 0 100px;
  align-items: center;
  color: white;
  h2 {
    float: left;
    width: 300px;
    margin: 0;
    text-align: left;
    cursor: pointer;
    .green {
      color: rgb(155, 238, 155);
    }
  }
  ul {
    text-align: right;
    margin: 0;
    li {
      display: inline-block;
      margin-left: 30px;
      font-weight: 100;
      color: rgb(181, 181, 181);
    }
    li:hover {
      opacity: 100%;
      cursor: pointer;
    }
  }
}

@media (max-width: 400px) {
  nav {
    margin: 25px 10px;
    padding: 0 0 15px;
    h2 {
      float: none;
      margin: 0 auto 25px;
      width: fit-content;
      font-size: 23px;
      cursor: pointer;
    }
    ul {
      text-align: center;
      padding: 0;
      width: 100%;
      li {
        margin: 0 15px;
      }
    }
  }
}
</style>
