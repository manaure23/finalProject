<template>
  <div>
      <footer>
        <section id="rrss">
            <a href="#"><img class="icons-rrss" src="../assets/Icons/github.svg" alt=""></a>
            <a href="#"><img class="icons-rrss" src="../assets/Icons/twitter.svg" alt=""></a>
            <a href="#"><img class="icons-rrss" src="../assets/Icons/whatsapp.svg" alt=""></a>
            <a href="#"><img class="icons-rrss" src="../assets/Icons/mail.svg" alt=""></a>
        </section>
        <section id="about-us">
            <a href="#">colabora</a>
            <a href="">publicidad</a>
            <a href="">aviso de privacidad</a>
            <a href="">acerca de <strong>NOMBRE EMPRESA</strong></a>
        </section>
      </footer>
  </div>
</template>

<script>
export default {

}
</script>

<style>
footer{
     background-color: rgba(90, 90, 250, 0.226);
}
#rrss{
    display: flex;
    justify-content: space-evenly;
    align-items: center;
}
.icons-rrss{
    width: 40px;
    height: 40px;
    margin-top: 20px;
}
#about-us{
    margin-top: 60px;
    display: flex;
    justify-content: space-around;
}
#about-us a{
    text-decoration: none;
    color: black;
    font-size: 20px;
    margin-bottom: 10px;
}

</style>