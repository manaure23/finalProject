<template>
  <div>
    <h2 id="shopping-cart-title">TU CESTA</h2>
    <div id="main">
        <section id="cart-description">
            <div class="cart-product">
              <div class="cart-product-img">
                <img class="img" src="../assets/Icons/zapatillas.svg" alt="">
              </div>
              <div class="cart-product-description">
                <h4><strong>Marca</strong></h4>
                <h4>Modelo articulo</h4>
                <h4>Talla:</h4>
              </div>
              <div class="counter">
                <button class="button-counter">-</button>
                <p>N</p>
                <button class="button-counter">+</button>
              </div>
            </div>
            <div class="cart-product">
              <div class="cart-product-img">
                <img class="img" src="../assets/Icons/zapatillas.svg" alt="">
              </div>
              <div class="cart-product-description">
                <h4><strong>Marca</strong></h4>
                <h4>Modelo articulo</h4>
                <h4>Talla:</h4>
              </div>
              <div class="counter">
                <button class="button-counter">-</button>
                <p>N</p>
                <button class="button-counter">+</button>
              </div>
            </div>
            <div class="cart-product">
              <div class="cart-product-img">
                <img class="img" src="../assets/Icons/zapatillas.svg" alt="">
              </div>
              <div class="cart-product-description">
                <h4><strong>Marca</strong></h4>
                <h4>Modelo articulo</h4>
                <h4>Talla:</h4>
              </div>
              <div class="counter">
                <button class="button-counter">-</button>
                <p>N</p>
                <button class="button-counter">+</button>
              </div>
            </div>
        </section>
        <section id="cart-price">
          <h3 class="text-cart-price" id="title-total-price"><strong>TOTAL</strong></h3>
          <h4 class="text-cart-price">Subtotal</h4>
          <h4 class="text-cart-price">Envio</h4>
          <h3 class="text-cart-price" id="text-total-price">Total</h3>
          <button class="checkout"><strong>Tramitar pedido</strong></button>
        </section>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>
#shopping-cart-title{
  text-align: left;
  font-size: 40px;
  margin-top: 30px;
  margin-left: 30px;
  letter-spacing: 1px;
  font-style: italic;
}
#main{
  display: flex;
  flex-wrap: wrap;
  margin-top: 10px;
  margin-bottom: 50px;
}
#cart-description{
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin-left: 20px;
  margin-top: 20px;
}
.cart-product{
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  background-color: rgba(90, 90, 250, 0.226);
  margin-top: 15px;
  margin-bottom: 15px;
  height: 130px;
  border-radius: 10px;
}
.cart-product-img{
  width: 120px;
  height: 150px;
  margin-right: 40px;
}
.img{
  width: 100px;
  height: 100px;
}
.cart-product-description{
  width: 350px;
  height: 150px;
  text-align: left;
}
.counter{
  display: flex;
  justify-content: space-between;
  width: 120px;
  height: 150px;
  text-align: center;
  margin-right: 20px;
}
.button-counter{
  border-radius: 50%;
  width: 27px;
  height: 27px;
  margin-top: 20px;
}
.counter p{
  margin-top: 20px;
}
#cart-price{
  width: 450px;
  height: 330px;
  background-color: rgba(90, 90, 250, 0.226);
  text-align: left;
  margin-left: 100px;
  margin-top: 35px;
  border-radius: 10px;
}
.checkout{
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
.text-cart-price{
  margin-top: 20px;
  margin-bottom: 20px;
  margin-left: 10px;
}
#text-total-price{
  border-top: 2px solid black;
  padding-top: 10px;
}
@media (max-width: 375px){
  #cart-description{
    margin-left: 0px;
  }
  .cart-product{
    width: 375px;
    justify-content: space-around;
  }
  .cart-product-img{
    width: 80px;
    height: 120px;
    margin-right: 10px;
    margin-left: 10px;
  }
  .img{
    width: 80px;
  }
  .cart-product-description{
    margin-top: 10px;
    width: 160px;
    height: 120px;
  }
  .counter{
    flex-direction: column-reverse;
    justify-content: space-around;
    width: 70px;
    height: 110px;
    margin: 0px;
  }
  .button-counter{
    margin-top: 5px;
  }
  .counter p{
    text-align: left;
    margin-top: 5px;
    margin-bottom: 5px;
    margin-left: 10px;
  }
  #shopping-cart-title{
    margin-left: 0px;
    text-align: center;
  }
  #cart-price{
    margin-left: 0px;
    width: 375px;
  }
  .checkout{
    margin-left: 20px;
    width: 330px;
  }
}

</style>