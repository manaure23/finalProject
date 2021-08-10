<template>
  <div>
    <h2 class="h2-titles">Hombre</h2>
    <nav>
      <ul class="menu-filter-buttons">
        <li><button class="filter-button">Camisas</button></li>
        <li><button class="filter-button">Pantalones</button></li>
        <li><button class="filter-button">Zapatillas</button></li>
        <li><button class="filter-button">Abrigos</button></li>
      </ul>
      <section id="items">
        <div class="product-card">
            <router-link to="/product-description-section"><img src="../assets/Icons/zapatillas.svg" class="img-provisional" alt=""> zapatillas</router-link>
        </div>
        <div class="product-card">
            <router-link to="/product-description-section"><img src="../assets/Icons/camiseta.svg" class="img-provisional" alt=""> camiseta</router-link>
        </div>
        <div class="product-card">
            <router-link to="/product-description-section"><img src="../assets/Icons/zapatillas.svg" class="img-provisional" alt=""> zapatillas</router-link>
        </div>
        <div class="product-card">
            <router-link to="/product-description-section"><img src="../assets/Icons/abrigo-largo.svg" class="img-provisional" alt=""> abrigo</router-link>
        </div>
        <div class="product-card">
            <router-link to="/product-description-section"><img src="../assets/Icons/pantalones-deportivos.svg" class="img-provisional" alt=""> pantalones</router-link>
        </div>
        <div class="product-card">
            <router-link to="/product-description-section"><img src="../assets/Icons/zapatillas.svg" class="img-provisional" alt=""> zapatillas</router-link>
        </div>
        <div class="product-card">
            <router-link to="/product-description-section"><img src="../assets/Icons/camiseta.svg" class="img-provisional" alt=""> camiseta</router-link>
        </div>
        <div class="product-card">
            <router-link to="/product-description-section"><img src="../assets/Icons/abrigo-largo.svg" class="img-provisional" alt=""> abrigo</router-link>
        </div>
      </section>
    </nav>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.h2-titles{
  margin-top: 40px;
  margin-left: 70px;
  margin-right: 70px;
  margin-bottom: 40px;
  text-align: center;
  border-radius: 10px;
  font-size: 40px;
  background-color: rgba(90, 90, 250, 0.13);
}
.menu-filter-buttons{
  display: inline-flex;
  justify-content: space-around;
  padding: 0px;
  width: 100%;
}
.filter-button{
  width: 200px;
  height: 40px;
  border: 1px solid rgba(90, 90, 250, 0.301);
  border-radius: 10px;
  background-color: rgba(90, 90, 250, 0.144);
}
#items{
  display: inline-flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin-top: 30px;
  margin-left: 80px;
  margin-right: 80px;
  margin-bottom: 30px;
}
.product-card{
  text-align: center;
  width: 250px;
  height: 300px;
}
.product-card:hover{
  border: 1px solid black;
  border-radius: 15px;
}
a{
    text-decoration: none;
    color: black;
    font-size: 30px;
}
.img-provisional{
    width: 160px;
    height: 190px;
}
</style>