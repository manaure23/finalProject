<template>
  <div>
    <header>
        <div class="principal">
          <h1>nombre empresa</h1>
          <nav class="genders">
            <a class="gender-button" href="#">Hombre</a>
            <a class="gender-button" href="#">Mujer</a>
          </nav>
          <ul class="user-buttons">
            <li><a href="#"><img class="icons" src="../assets/Icons/favorite.svg" alt=""></a></li>
            <li><a href="#"><img class="icons" src="../assets/Icons/shoppingCart.svg" alt=""></a></li>
          </ul>
        </div>
    </header>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

.principal{
  width: 100%;
  display: flex;
  justify-content: space-between;
  background-color: rgba(90, 90, 250, 0.226);
}
h1{
  width: 350px;
}
.user-buttons{
  width: 150px;
  display: inline-flex;
  justify-content: space-between;
  margin-top: 10px;
  margin-right: 20px;
  padding: 0px;
}
.icons{
  width: 40px;
  height: 40px;
}
.genders{
  width: 400px;
  display: inline-flex;
  align-content: center;
  justify-content: space-between;
  padding: 0px;
  margin-top: 10px;
}
.gender-button{
  width: 150px;
  height: 40px;
  margin-top: 7px;
  color: black;
  text-decoration: none;
  font-size: 25px;
}
.gender-button:hover{
  color: red;
  text-decoration: underline;
}
ul li{
  list-style: none;
}
a{
  text-decoration: none;
}

</style>
