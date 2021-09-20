<template>
  <main>
    <div class="main-content">
      <h1> Content goes here </h1>
    </div>

      <div class="main-bottom">
        <div class="bottom-content">
          <ul>
            <li><a href="#">Prova</a></li>
            <li><a href="#">Prova</a></li>
            <li><a href="#">Prova</a></li>
            <li><a href="#">Prova</a></li>
            <li><a href="#">Prova</a></li>
          </ul>
        </div>
      </div>
  </main>
</template>

<script>
export default {
  name: 'Main',
  
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
      margin: 30px;
      color: white;
      text-decoration: none;
    }
  }
}

</style>
