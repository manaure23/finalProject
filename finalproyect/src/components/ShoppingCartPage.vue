<template>
  <div>
    <h2 id="shopping-cart-title">TU CESTA</h2>
    <div id="main">
      <section id="cart-description">
        <div class="cart-product">
          <div class="cart-product-img">
            <img class="img" :src="product.img" alt="" />
          </div>
          <div class="cart-product-description">
            <h4>
              <strong>{{ product.brand }}</strong>
            </h4>
            <h4>{{ product.name }}</h4>
            <h4>Talla:</h4>
            <h4>Precio: {{ product.price }}</h4>
          </div>
          <div class="counter">
            <button class="button-counter" @click="substract">-</button>
            <p>{{ numberArticle }}</p>
            <button class="button-counter" @click="add">+</button>
          </div>
        </div>
      </section>
      <section id="cart-price">
        <h3 class="text-cart-price" id="title-total-price">
          <strong>TOTAL</strong>
        </h3>
        <h4 class="text-cart-price">
          Subtotal: {{ (price = product.price * numberArticle) }}
        </h4>
        <h4 class="text-cart-price">Envio</h4>
        <h3 class="text-cart-price" id="text-total-price">Total {{ price }}</h3>
        <button class="checkout"><strong>Tramitar pedido</strong></button>
      </section>
    </div>
  </div>
</template>

<script>
import { womanproducts } from "../assets/Data/Products.json";
import { manproducts } from "../assets/Data/Products.json";
export default {
  props: ["id"],
  data() {
    return {
      items: [...womanproducts, ...manproducts],
      numberArticle: 1,
      product: [],
      cartArticles: [],
      price: 10,
      totalPrice: 1,
      size: "",
    };
  },
  mounted() {
    this.product = this.items.find((item) => item.id == this.$route.params.id);
    this.cartArticles.push(this.product);
    console.log(this.cartArticles);
    this.size = this.$route.params.size;
    console.log(this.size);
  },
  methods: {
    add() {
      this.numberArticle++;
    },
    substract() {
      if (this.numberArticle === 0) {
        this.numberArticle = 0;
      } else this.numberArticle--;
    },
  },
};
</script>

<style scoped>
h4 {
  line-height: 1.1;
}
#shopping-cart-title {
  text-align: left;
  font-size: 40px;
  margin-top: 30px;
  margin-left: 30px;
  letter-spacing: 1px;
  font-style: italic;
}
#main {
  display: flex;
  flex-wrap: wrap;
  margin-top: 10px;
  margin-bottom: 50px;
}
#cart-description {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin-left: 20px;
  margin-top: 20px;
}
.cart-product {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  background-color: rgba(90, 90, 250, 0.226);
  margin-top: 15px;
  margin-bottom: 15px;
  height: 130px;
  border-radius: 10px;
}
.cart-product-img {
  width: 120px;
  height: 130px;
  margin-right: 40px;
}
.img {
  width: 130px;
  height: 130px;
}
.ocultar {
  display: none;
}
.cart-product-description {
  width: 350px;
  height: 130px;
  text-align: left;
}
.counter {
  display: flex;
  justify-content: space-between;
  width: 120px;
  height: 130px;
  text-align: center;
  margin-right: 20px;
}
.button-counter {
  border-radius: 50%;
  width: 27px;
  height: 27px;
  margin-top: 20px;
}
.counter p {
  margin-top: 20px;
}
#cart-price {
  width: 450px;
  height: 330px;
  background-color: rgba(90, 90, 250, 0.226);
  text-align: left;
  margin-left: 100px;
  margin-top: 35px;
  border-radius: 10px;
}
.checkout {
  width: 300px;
  height: 35px;
  background-color: rgba(90, 90, 250, 0.39);
  margin-left: 80px;
  margin-top: 30px;
  border: 1px black solid;
  border-radius: 9px;
  text-align: center;
  font-size: 20px;
  letter-spacing: 1px;
}
.text-cart-price {
  margin-top: 20px;
  margin-bottom: 20px;
  margin-left: 10px;
}
#text-total-price {
  border-top: 2px solid black;
  padding-top: 10px;
}
@media (max-width: 376px) {
  #cart-description {
    margin-left: 0px;
  }
  h4 {
    font-size: 17px;
  }
  .cart-product {
    margin-left: 3px;
    width: 354px;
    justify-content: space-around;
  }
  .cart-product-img {
    width: 80px;
    height: 120px;
    margin-right: 10px;
    margin-left: 10px;
  }
  .img {
    width: 100px;
  }
  .cart-product-description {
    margin-top: 10px;
    margin-left: 20px;
    width: 160px;
    height: 120px;
  }
  .counter {
    flex-direction: column-reverse;
    justify-content: space-around;
    width: 70px;
    height: 110px;
    margin: 0px;
  }
  .button-counter {
    margin-top: 5px;
  }
  .counter p {
    text-align: left;
    margin-top: 5px;
    margin-bottom: 5px;
    margin-left: 10px;
  }
  #shopping-cart-title {
    margin-left: 0px;
    text-align: center;
  }
  #cart-price {
    margin-left: 3px;
    width: 350px;
  }
  .checkout {
    margin-left: 12px;
    width: 330px;
  }
}
@media (min-width: 377px) and (max-width: 450px) {
  #cart-description {
    margin-left: 0px;
  }
  h4 {
    font-size: 17px;
  }
  .cart-product {
    margin-left: 3px;
    width: 410px;
    justify-content: space-around;
  }
  .cart-product-img {
    width: 80px;
    height: 120px;
    margin-right: 10px;
    margin-left: 10px;
  }
  .img {
    width: 100px;
  }
  .cart-product-description {
    margin-top: 10px;
    width: 160px;
    height: 120px;
  }
  .counter {
    flex-direction: column-reverse;
    justify-content: space-around;
    width: 70px;
    height: 110px;
    margin: 0px;
  }
  .button-counter {
    margin-top: 5px;
  }
  .counter p {
    text-align: left;
    margin-top: 5px;
    margin-bottom: 5px;
    margin-left: 10px;
  }
  #shopping-cart-title {
    margin-left: 0px;
    text-align: center;
  }
  #cart-price {
    margin-left: 3px;
    width: 410px;
  }
  .checkout {
    margin-left: 20px;
    width: 330px;
  }
}
@media (min-width: 451px) and (max-width: 968px) {
  .cart-product {
    width: 700px;
  }
  #cart-price {
    width: 545px;
    height: 400px;
  }
  .checkout {
    width: 345px;
    margin-left: 90px;
  }
}
@media (min-width: 1280px) and (max-height: 950px) {
  #main {
    height: 545px;
  }
}
@media (min-width: 1900px) and (min-height: 1080px) {
  #main {
    height: 670px;
    justify-content: space-around;
  }
}
</style>