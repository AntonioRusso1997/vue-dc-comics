<template>
  <div class="card">
    <div class="card-img">
    <img :src="com.thumb" :alt="com.series">
    </div>
    <h3>{{ com.series.toUpperCase() }}</h3>
  </div>
</template>

<script>
export default {
  name: 'ComicsCard',
  props: ['com']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.card {
  width: calc(100% / 6);
  height: 200px;
  font-size: 12px;
  margin-bottom: 40px;
  cursor: pointer;
  
  .card-img {
    width: 175px;
    height: 175px;
    overflow: hidden;
    margin-bottom: 15px;

    img {
      width: 100%;
    }

  }
  h3 {
    width: 90%;
    
  }

}

</style>
