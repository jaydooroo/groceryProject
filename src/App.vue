<template>
  <div id="app">
    <div id="menu">
      <div id="brand">
        <router-link to="/">
          <img src="/images/logo.png" />
        </router-link>
      </div>
      <div id="side">
        <router-link to="/browse">
          <div class="menu-item browse">
            <img src="/images/globe.png" />
            <p>Browse</p>
          </div>
        </router-link>
        <router-link to="/cart">
          <div class="menu-item">
            <img src="/images/love.png" />
            <p>{{ this.$root.$data.cart.length }} items</p>
          </div>
        </router-link>
      </div>
    </div>
    <router-view />
     <footer>
          Contact Info: abcd@gamil.com  
          <br>
          Phone Number: +1) 805-999-9999 
          <br>
          github:<a href = https://github.com/jaydooroo/groceryProject.git>https://github.com/jaydooroo/groceryProject.git</a>
      </footer>
  </div>
</template>
<style>
* {
  box-sizing: border-box;
}

body {
  margin: 50px 100px;
}

#menu {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-column-gap: 5px;
  grid-template-areas: "none brand side";
  margin-bottom: 50px;
}

#menu a {
  color: #b84901;
}

#brand {
  grid-area: brand;
  display: flex;
  justify-content: center;
}

#brand img {
  height: 200px;
}

#side {
  grid-area: side;
  display: flex;
  justify-content: flex-end;
}

#side img {
  width: 50px;
}

.menu-item {
  display: flex;
  flex-direction: column;
}

.menu-item p {
  margin: 0px;
}

.browse {
  margin-right: 50px;
}
footer{
    height: 100px;
    font-family:  "Times New Roman", Times, serif;
    font-size: medium;
    color: rgb(27, 25, 25);;
    font-weight: bold;
    text-align: center;
}
</style>
