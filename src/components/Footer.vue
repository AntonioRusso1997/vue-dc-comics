<template>
  <footer>
    <div class="footer-top">
      <div class="footer-content">
        <div class="section-1">
          <ul>            
            <h3>DC COMICS</h3>
            <li><a href="#">Characters</a></li>
            <li><a href="#">Comics</a></li>
            <li><a href="#">Movies</a></li>
            <li><a href="#">TV</a></li>
            <li><a href="#">Games</a></li>
            <li><a href="#">Videos</a></li>
            <li><a href="#">News</a></li>
          </ul>

          <ul>
            <h3>SHOP</h3>
            <li><a href="#">Shop DC</a></li>
            <li><a href="#">Shop DC Collectibles</a></li>
          </ul>
        </div>

        <div class="section2">
          <ul>            
            <h3>DC</h3>
            <li><a href="#">Terns Of Use</a></li>
            <li><a href="#">Privacy policy(New)</a></li>
            <li><a href="#">Ad Choices</a></li>
            <li><a href="#">Advertising</a></li>
            <li><a href="#">Jobs</a></li>
            <li><a href="#">Subscriptions</a></li>
            <li><a href="#">Talent Workshops</a></li>
            <li><a href="#">CPSC Certification</a></li>
            <li><a href="#">Ratings</a></li>
            <li><a href="#">Shop Help</a></li>
            <li><a href="#">Contact Us</a></li>
          </ul>
        </div>

        <div class="section-3">
          <ul>
            <h3>SITES</h3>
            <li><a href="#">DC</a></li>
            <li><a href="#">MAD Magazine</a></li>
            <li><a href="#">DC Kids</a></li>
            <li><a href="#">DC Universe</a></li>
            <li><a href="#">DC Power Visa</a></li>
          </ul>
        </div>
      </div>
    <img src="@/assets/img/dc-logo-bg.png" alt="">
    </div>


    <div class="footer-bottom">
      <div class="footer-bottom-content">
        <button>SIGN-UP NOW!</button>

        <div class="footer-nav">
          <h3>FOLLOW US</h3>
          <ul>
            <li><a href="#"> <img src="@/assets/img/footer-facebook.png" alt=""></a></li>
            <li><a href="#"> <img src="@/assets/img/footer-twitter.png" alt=""></a></li>
            <li><a href="#"> <img src="@/assets/img/footer-youtube.png" alt=""></a></li>
            <li><a href="#"> <img src="@/assets/img/footer-pinterest.png" alt=""></a></li>
            <li><a href="#"> <img src="@/assets/img/footer-periscope.png" alt=""></a></li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

@import "../style/mixins";
@import "../style/vars";

footer {
  background-image: url(../assets/img/footer-bg.jpg);
  background-size: cover;
}

.footer-top {
  width: 70%;
  margin: 0 auto;
  @include center();
  justify-content: space-between;
  align-items: flex-start;
  height: 400px;
  overflow: hidden;
  padding: 0 10px;
  position: relative;

  img {
    position: absolute;
    right: 10px;
    top: 50%;
    transform: translateY(-50%)
  }

  .footer-content {
  @include center(hprizontal);
  justify-content: space-between;
  width: 30%;
  margin: 15px 0;

  ul {
    list-style: none;

    h3 {
      color: white;
      margin: 15px 0;
    }

    li a {
      text-decoration: none;
      color: #959595;
      font-size: 12px;

    }
  }
}
}

.footer-bottom {
  background-color:#434343;

  .footer-bottom-content {
    width: 70%;
    margin: 0 auto;
    @include center();
    justify-content: space-between;
    padding: 30px 10px;

    button {
      font-size: 18px;
      background: none;
      padding: 15px 10px;
      color: white;
      font-weight: 600;
      border: 3px solid $blue;

      &:hover {
        background-color: $blue;
        cursor: pointer;
      }
    }

    .footer-nav {
      @include center();

      h3 {
          margin: 20px;
          color: $blue;
        }

      ul {
        list-style: none;
        @include center();

        li a {
          margin: 10px;

          &:hover {
            opacity: 80%;
          }
        }
      }
    }
  }

}
</style>
