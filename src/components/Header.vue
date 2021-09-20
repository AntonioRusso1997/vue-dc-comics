<template>
  <header>
    <a href="/">
    <img class="logo-home" src="../assets/img/dc-logo.png" alt="">
    </a>
    <nav class="navbar">
      <ul>
        <li v-for="(link, index) in links" :key="index">
          <a :class="(link.current) ? 'active' : null" :href="link.url">
            {{ link.text }}
          </a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header',
  
  data() {
    return {      
      links: [
        {
          text: "CHARACTERS",
          url: "#",
          current: false
        },
        {
          text: "COMICS",
          url: "#",
          current: true
        },
        {
          text: "MOVIES",
          url: "#",
          current: false
        },
        {
          text: "TV",
          url: "#",
          current: false
        },
        {
          text: "GAMES",
          url: "#",
          current: false
        },
        {
          text: "COLLECTIBLES",
          url: "#",
          current: false
        },
        {
          text: "VIDEOS",
          url: "#",
          current: false
        },
        {
          text: "FANS",
          url: "#",
          current: false
        },
        {
          text: "NEWS",
          url: "#",
          current: false
        },
        {
          text: "SHOP",
          url: "#",
          current: false
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

header {
  width: 70%;
  height: 120px;
  margin: 0 auto;
  @include center();
  justify-content: space-between;
  padding: 10px;
}

.logo-home {
  width: 90px;
}

ul {
  @include center();
  list-style: none;

  li a {
    display: inline-block;
    margin: 15px;
    text-decoration: none;
    font-weight: 800;
    height: 120px;
    line-height: 120px;
    vertical-align: middle;

    &.active,
    &:hover {
      color: $blue;
      border-bottom: 5px solid $blue;
    }
  }
}
</style>
