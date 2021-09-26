<template>
  <header id="header">
    <div class="main">
      <router-link to="/"><h1 id="title">TDM</h1> </router-link>
      <router-link to="/shopping-cart-section"
        ><img
          class="icons user-buttons"
          src="../assets/Icons/shoppingCart.svg"
          alt=""
      /></router-link>
    </div>
    <nav class="genders">
      <router-link class="gender-button" to="/man-section">Hombre</router-link>
      <router-link class="gender-button" to="/woman-section">Mujer</router-link>
    </nav>
  </header>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
    prop: Object,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#header {
  background-color: rgba(90, 90, 250, 0.226);
}
.main {
  width: 100%;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  background-color: rgba(90, 90, 250, 0.226);
}

#title {
  margin-left: 10px;
  margin-top: 5px;
  width: 100px;
  text-align: center;
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  font-weight: bold;
}
#icon {
  height: 50px;
  width: 50px;
}
.user-buttons {
  display: inline-flex;
  justify-content: space-between;
  margin-top: 10px;
  margin-right: 20px;
  padding: 0px;
}
.icons {
  width: 40px;
  height: 40px;
}
.genders {
  width: 400px;
  display: inline-flex;
  align-content: center;
  justify-content: space-between;
  padding: 0px;
  margin-top: 10px;
}
.gender-button {
  width: 150px;
  height: 40px;
  color: black;
  text-decoration: none;
  font-size: 33px;
  font-weight: 500;
}
.gender-button:hover {
  color: red;
  text-decoration: underline;
}
ul li {
  list-style: none;
}
a {
  text-decoration: none;
}
@media (max-width: 470px) {
  h1 {
    width: 365px;
  }
  .genders {
    width: 260px;
  }
  .gender-button {
    width: 100px;
  }
  .user-buttons {
    width: 50px;
  }
  .icons {
    width: 30px;
  }
}
@media (min-width: 471px) and (max-width: 968px) {
  h1 {
    width: 768px;
    font-size: 45px;
  }
  .genders {
    width: 500px;
    justify-content: space-between;
  }
}
</style>
