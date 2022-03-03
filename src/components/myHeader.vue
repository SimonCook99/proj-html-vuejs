<template>
  <header class="container">

    <div class="section-top">
      <div>
        <span>Download App</span>
        <button>iOS</button>
        <span>Advertise with us</span>
      </div>
      <div class="social">
        <i class="fa-brands fa-facebook-f"></i>
        <i class="fa-brands fa-instagram"></i>
        <i class="fa-brands fa-twitter"></i>
        <i class="fa-brands fa-youtube"></i>
      </div>
    </div>


    <div class="section-bottom">
      <img src="../assets/img/avada-food-logo.png" alt="avada food logo">
      <nav>
        <ul>
          <li v-for="(item, index) in lista" :key="index">
            <a :class="index == 0 ? 'active':'' " href="#">{{item}}</a>
          </li>
          <li><i class="fa-solid fa-magnifying-glass"></i></li>
        </ul>
      </nav>
    </div>
  </header>

</template>

<script>
export default {
  name: 'myHeader',
  props: ["lista"]
  
}
</script>


<style scoped lang="scss">

  @import "SCSS/colors.scss";

  header{
    padding-top: 20px;
  }

  .section-top{
    color: grey;
    display: flex;
    justify-content: space-between;
    margin-bottom: 10px;
  }

  button{
    padding: 5px;
    margin-left: 10px;
    margin-right: 20px;
    border-radius: 5px;
    font-size: 12px;
  }

  .social svg{
    margin: 0px 20px;
  }

  .section-bottom{
    display: flex;
    flex-direction: column;
    align-items: center;

    li{
      display: inline-block;
      margin: 30px;
      text-decoration: none;

      a{
        text-decoration: none;
        color: black;
        border-bottom: 2px solid transparent;
        padding-bottom: 10px;

        &.active{
          color: $buttonColor;
          border-bottom: 3px solid $buttonColor;
        }
      }
    }
  }

</style>
