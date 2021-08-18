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
        <div v-for="item in items" :key="item" class="product-card">
          <router-link
            :to="{
              name: 'ProductDescriptionSection',
              params: {
                id: item.id,
                img: item.img,
                brand: item.brand,
                price: item.price,
                name: item.name,
                color: item.color,
                type: item.type,
                sizes: item.sizes,
              },
            }"
            ><img :src="item.img" :alt="item.name" class="img-provisional" />
            <p class="item-name">{{ item.name }}</p>
            <p class="item-type">{{ item.type }}</p>
          </router-link>
        </div>
      </section>
    </nav>
  </div>
</template>

<script>
import { manproducts } from "../assets/Data/Products.json";
export default {
  name: "ManPage",
  data() {
    return {
      items: manproducts,
    };
  },
  mounted() {
    console.log(this.items);
  },
  methods() {},
};
</script>

<style scoped>
.h2-titles {
  margin-top: 40px;
  margin-left: 70px;
  margin-right: 70px;
  margin-bottom: 40px;
  text-align: center;
  border-radius: 10px;
  font-size: 40px;
  background-color: rgba(90, 90, 250, 0.13);
}
.menu-filter-buttons {
  display: inline-flex;
  justify-content: space-around;
  flex-wrap: wrap;
  padding: 0px;
  width: 100%;
}
.filter-button {
  width: 200px;
  height: 40px;
  border: 1px solid rgba(90, 90, 250, 0.301);
  border-radius: 10px;
  background-color: rgba(90, 90, 250, 0.144);
}
#items {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  margin-top: 30px;
  margin-left: 80px;
  margin-right: 80px;
  margin-bottom: 30px;
}
.product-card {
  text-align: center;
  width: 250px;
  height: 300px;
  margin-left: 10px;
  margin-right: 20px;
}
.product-card:hover {
  border: 1px solid black;
  border-radius: 15px;
}
a {
  text-decoration: none;
  color: black;
  font-size: 30px;
}
.img-provisional {
  width: 160px;
  height: 190px;
}
.item-name {
  font-size: 19px;
  margin: 0px;
}
.item-type {
  font-size: 15px;
  color: rgba(56, 56, 56, 0.699);
}
@media (max-width: 450px) {
  #items {
    margin-left: 0px;
    margin-right: 0px;
  }
  .product-card {
    margin-left: 27px;
  }
  .filter-button {
    width: 250px;
    margin-top: 3px;
    margin-bottom: 3px;
  }
}
@media (min-width: 451px) and (max-width: 968px) {
  .h2-titles {
    margin-bottom: 25px;
  }
  .filter-button {
    width: 400px;
    margin-top: 5px;
  }
  .menu-filter-buttons {
    flex-direction: column;
  }
}
</style>
