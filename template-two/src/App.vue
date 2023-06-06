<template>
 
 <NavbarView/>
<!-- HERO SECTION -->
 <div class="header-wrapper">

<!-- HEADER TEXT -->
  <div class="header-left">

    <h1 class="text-large">BUY YOUR <br> SHOES TODAY</h1>
    <div id="separator"></div>
    <p class="text-desc">Is post each that just leaf no. He connection interested so we an sympathize advantages. 
      <br> To said is it shed want do. Occasional middletons everything so to. 
      <br> Have spot part for his quit may. 
      Enable it is square my an regard. 
      Often merit stuff first oh up hills as he..</p>

      <button class="shop-btn"> SHOP NOW</button>

  </div>
  <!-- HEADER TEXT -->

    <!-- HEADER IMAGE -->
    <div class="header-right">
      <img src="@/assets/shoe.png">
    </div>
    <!-- HEADER IMAGE -->

 </div>
 <!-- HERO SECTION -->

 <h2 id="separation">OUR BEST PRODUCTS!</h2>

 <!-- CARDS -->
 <div class="all-cards">

  <div class="card-section" v-for="item in items" :key="item.id">

    <div class="card">
      
      <img class="card-img" :src="`${api_url}${item.attributes.image.data.attributes.formats.thumbnail.url}`" height="200" width="200"/>
      <p class="card-type">{{ item.attributes.type }}</p>
      <p class="card-name">{{ item.attributes.name }}</p>
      <p class="card-reviews">{{ item.attributes.reviews }} reviews</p>
      <p class="card-price">{{ item.attributes.price }}€</p>
      <button class="purchase-btn">Buy Now</button>

    </div>

  </div>

 </div>
  <!-- CARDS -->

<FooterView />

</template>

<script>
import NavbarView from "./components/NavbarView.vue"
import FooterView from "./components/FooterView.vue"

export default {
  components: {
    NavbarView,
    FooterView,
  },

  data() {
    return {
      items: [],
      api_url: "http://localhost:1337",
    }
  },

  
methods: {
  async getItems() {
            try {
              fetch('http://localhost:1337/api/items?populate=*')
                .then(response => response.json())
                .then(data => {
                  const items = Object.values(data)[0];
                  for ( let i = 0; i < items.length; i++) {
                    this.items.push(items[i])
                  }
        
                  console.log(items)
                })
                .catch(error => {
                  console.error(error);
                });
        
            } catch (error) {
              console.error(error);
            }
            },
            
            emptyStore() {
              this.items = [];
            }
},

created() {
  this.getItems()
  console.log(this.items)
},
}



</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700;900&display=swap');




.card-type {
  color: gray;
}

.card-name {
  font-weight: 600;
  font-size: 1.25em;
  color: #110f42;
}

.card-reviews {
  color: gray;
}

.card-price {
  color: #110f42;
  font-weight: 800;
  font-size: 1.5em;
}

.purchase-btn {
  border: 2px solid #1F6AAD;
  border-radius: 40px;
  padding-top: 8%;padding-bottom: 8%;
  padding-left: 16%;padding-right: 16%;
  font-size: 1em;
  background-color: white;
  font-weight: 600;
  transition: 0.2s;
}

.purchase-btn:hover {
  border-color: white;
  background-color: #1F6AAD;
  color: white;
  transform: scale(1.1);
}

body {
  background-color: #F5F6FF;
    font-family: Roboto;
    padding: 0;
    margin: 0;
    top: 0;
    overflow-x: hidden;
  }

  #separation {
    position: relative;
    padding-top: 25px;margin-bottom: 25px;
    left:45%;
    text-decoration: underline;
  }

.header-wrapper {
  color: white;
  background-image: url(@/assets/landing-hero-background.jpg);
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  padding-bottom: 5%;
}

#separator {
  border: 1px solid white;
  width: 20%;
}

.header-left {
  position: relative;
  top: 50%;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
}

.text-large {
  margin-top: 15%;
  font-size: 46px;
}

.text-desc {
  padding-bottom: 10%;
}

.shop-btn {
  font-weight: 700;
  font-size: 1em;
  background-color: white;
  border: none;
  width: fit-content;
  padding-top: 25px;
  padding-bottom: 25px;
  padding-left: 50px;
  padding-right: 50px;
  border-radius: 40px;
  transition: 0.1s;
  height: 68px;
}

.shop-btn:hover {
  transform: scale(1.1);
  border: 2px solid #110f42;
}

.all-cards {
  margin: 5%;
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  flex-basis: 50%;
  flex-wrap: wrap;

}

.card-section {
  width: 20%;
  padding-left: 9%;
}

.card {
  width: 80%;
  padding: 3%;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: white;
  border-radius: 18px;
  box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
  margin-bottom: 10%;
  transition: 0.2s;
}

.card:hover {
  transform: scale(1.1);
}

@media screen and (max-width:900px){
  .all-cards {
    display: flex;
    flex-wrap: wrap;
  }

  .card-section {
  width: 70%;
  padding-left: 9%;
}

.header-wrapper {
  display: block;
  overflow: hidden;
}
}

</style>