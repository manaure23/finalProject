<template>
  <div>
    <h2 class="h2-titles">Hombre</h2>
    <select v-model="filter" name="filter" id="filter-options">
      <option value="all">Todos</option>
      <option value="zapatillas">Zapatillas</option>
      <option value="camisetas">Camisas</option>
      <option value="pantalones">Pantalones</option>
      <option value="abrigos">Abrigos</option>
    </select>
    <section id="items">
      <div v-for="item in filterArticles" :key="item" class="product-card">
        <router-link
          :to="{
            name: 'ProductDescriptionSection',
            params: {
              id: item.id,
            },
          }"
          ><img :src="item.img" :alt="item.name" class="img-product" />
          <p class="item-name">{{ item.name }}</p>
          <p class="item-type">{{ item.type }}</p>
        </router-link>
      </div>
    </section>
  </div>
</template>

<script>
import { manproducts } from "../assets/Data/Products.json";
export default {
  name: "ManPage",
  data() {
    return {
      items: manproducts,
      filter: "all",
    };
  },
  computed: {
    filterArticles() {
      let filtered = this.items;
      let value = this.filter;
      let filteredItems = filtered.filter((article) => {
        return value === "all" ? article : article.type === value;
      });
      return filteredItems;
    },
  },
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
#filter-options {
  padding: 5px 70px;
  text-align: center;
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
  width: 235px;
  height: 300px;
  margin-left: 10px;
  margin-right: 20px;
  margin-top: 10px;
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
.img-product {
  width: 210px;
  height: 230px;
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
