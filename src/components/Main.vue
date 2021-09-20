<template>
  <main>
    <div class="main-content">
      <h1> Content goes here </h1>
    </div>
      <div class="main-bottom">
        <div class="bottom-content">
          <ul>
            <li v-for="(comic, index) in comics" :key="index">
              <a :href="comic.url">
              <img  :src="comic.img" alt="">
              {{ comic.text }}
              </a>
            </li>
          </ul>
        </div>
      </div>
  </main>
</template>

<script>
export default {
  name: 'Main',

  data() {
    return {
      comics: [
        {
          text: "DIGITAL COMICS",
          img: require("../assets/img/buy-comics-digital-comics.png"),
          url: "#"
        },
        {
          text: "DC MERCHANDISE",
          img: require("../assets/img/buy-comics-merchandise.png"),
          url: "#"
        },
        {
          text: "SUBSCIPTION",
          img: require("../assets/img/buy-comics-subscriptions.png"),
          url: "#"
        },
        {
          text: "COMIC SHOP LOCATOR",
          img: require("../assets/img/buy-comics-shop-locator.png"),
          url: "#"
        },
        {
          text: "DC POWER VISA",
          img: require("../assets/img/buy-dc-power-visa.svg"),
          url: "#"
        }
      ]
    }
  }  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

@import "../style/mixins";
@import "../style/vars";


main {
  background-color: black;
}

.main-content {
  width: 70%;  
  padding: 50px 10px;
  margin: 0 auto;
  color: white;
}

.main-bottom {
  background-color: $blue;
}

.bottom-content {
  width: 70%;
  margin: 0 auto;
  padding: 50px;
  @include center();

  ul {
    list-style: none;
    @include center(vertical);
    
    li a {
      margin-right: 60px;
      color: white;
      text-decoration: none;
      font-size: 15px;
      @include center();

      img {
        height: 60px;
        margin-right: 10px; 
      }
    }

    li:last-child a img {
      height: 40px;
    }
  }
}

</style>
