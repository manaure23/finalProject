<template>
  <div>
    <a href="#"><img class="commercial" src="../assets/commercialImg.png" alt=""></a> 
    <h2 class="h2-titles">Novedades</h2>
    <section id="novelties">
        <div class="novelty-card">
            <router-link to="/product-description-section"><img src="../assets/Icons/zapatillas.svg" class="img-provisional" alt=""> zapatilla</router-link>
        </div>
        <div class="novelty-card">
            <router-link to="/product-description-section"><img src="../assets/Icons/pantalones-deportivos.svg" class="img-provisional" alt=""> pantalon</router-link>
        </div>
        <div class="novelty-card">
            <router-link to="/product-description-section"><img src="../assets/Icons/camiseta.svg" class="img-provisional" alt=""> camiseta</router-link>
        </div>
        <div class="novelty-card">
            <router-link to="/product-description-section"><img src="../assets/Icons/abrigo-largo.svg" class="img-provisional" alt=""> abrigo</router-link>
        </div>
    </section>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.commercial{
  border: 2px solid rgba(90, 90, 250, 0.39);
  border-radius: 12px;
  width: 80%;
  height: 350px;
  margin-left: 50px;
  margin-top: 50px;
}
.h2-titles{
  margin-top: 50px;
  margin-left: 20px;
  margin-bottom: 20px;
  text-align: left;
  font-size: 40px;
}
#novelties{
  display: inline-flex;
  justify-content: space-between;
  width: 80%;
  margin-left: 10px;
  margin-bottom: 50px;
}
.novelty-card{
  text-align: center;
  width: 180px;
  height: 250px;
}
a{
    text-decoration: none;
    color: black;
    font-size: 30px;
}
.img-provisional{
    width: 170px;
    height: 200px;
}
</style>