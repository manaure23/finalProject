<template>
  <section id="product-description">
    <div id="img">
      <img :src="img" alt="" class="img-main" />
    </div>
    <div id="description">
      <h3 class="text-description">{{ brand }}</h3>
      <h2 class="text-description">
        <strong>{{ name }}</strong>
      </h2>
      <h3 class="text-description">{{ price }} €</h3>
      <h4 class="text-description">Color: {{ color }}</h4>
      <select name="size" id="n-size">
        <option v-for="size in sizes" :key="size" :value="size">
          {{ size }}
        </option>
      </select>
      <div id="add-favorite">
        <button id="add">Añadir a la cesta</button>
        <button id="favorite">
          <img class="fav-img" src="../assets/Icons/favorite.svg" alt="" />
        </button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: ["id"],

  data() {
    return {
      img: this.$route.params.img,
      brand: this.$route.params.brand,
      price: this.$route.params.price,
      color: this.$route.params.color,
      name: this.$route.params.name,
      sizes: this.$route.params.sizes,
    };
  },
  mounted() {
    console.log(this.tallas);
  },
  ready: function () {
    window.beforeUnload(alert("no"));
  },
};
</script>

<style scoped>
#product-description {
  display: inline-flex;
  justify-content: space-around;
  flex-wrap: wrap;
  margin-top: 30px;
  width: 100%;
}
#img {
  width: 400px;
  height: 500px;
  margin-left: 20px;
  margin-right: 20px;
}
.img-main {
  width: 380px;
  height: 480px;
}
#description {
  width: 400px;
  height: 500px;
  text-align: left;
  margin-top: 50px;
}
#n-size {
  width: 280px;
  height: 30px;
  margin-bottom: 10px;
  border-radius: 5px;
}
#add-favorite {
  display: flex;
  justify-content: space-between;
  width: 350px;
  margin-top: 20px;
}
#add {
  width: 280px;
  height: 35px;
  border: 1px solid black;
  border-radius: 8px;
}
#favorite {
  width: 40px;
  height: 35px;
  border: 1px solid black;
  border-radius: 5px;
}
.fav-img {
  width: 25px;
  height: 25px;
}
.text-description {
  margin-top: 18px;
  margin-bottom: 18px;
}
@media (max-width: 450px) {
  #img {
    margin: 0px;
    width: 375px;
    height: 350px;
  }
  .img-main {
    width: 320px;
    height: 340px;
  }
  #description {
    width: 375px;
    height: 370px;
    margin-top: 10px;
  }
  .text-description {
    margin-left: 10px;
    margin-bottom: 12px;
    margin-top: 12px;
  }
  #n-size {
    margin-left: 25px;
    width: 320px;
  }
  #add-favorite {
    width: 375;
  }
  #add {
    margin-left: 15px;
  }
}
</style>