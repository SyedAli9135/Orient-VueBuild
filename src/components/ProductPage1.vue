<template>
  <div>
    <Navbar />
    <Header2 />
    <div>
      <div className="productpage1">
        <div v-for="product in products" :key="product.id">
          <div className="productpage1-column">
            <img :src="product.image" style="width: 100%;" />
            <strong>{{ product.title }}</strong>
            <p>
              <strong>{{ product.text }}</strong>
            </p>
            <p>{{ product.price }}</p>
            <div className="productpage1-buttons">
              <button>EN M/ US M</button>
              <router-link to="productcheckout"><button>ADD</button></router-link>
            </div>
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>
<script>
import Navbar from './Navbar.vue'
import Header2 from './Header2.vue'
import Footer from './Footer.vue'
export default {
  name: 'ProductPage1',
  components: {
    Navbar,
    Header2,
    Footer,
  },
  data() {
    return {
      products: [
        {
          id: 1,
          image: '/images/Rectangle55.png',
          title: 'NEW',
          text: 'UNSTICHED 3PC PREMIUM ',
          price: 'PKR 4,990.00',
        },
        {
          id: 2,
          image: '/images/Rectangle56.png',
          title: 'NEW',
          text: 'UNSTICHED 3PC PREMIUM ',
          price: 'PKR 4,990.00',
        },
        {
          id: 3,
          image: '/images/Rectangle63.png',
          title: 'NEW',
          text: 'UNSTICHED 3PC PREMIUM ',
          price: 'PKR 4,990.00',
        },
        {
          id: 4,
          image: '/images/Rectangle64.png',
          title: 'NEW',
          text: 'UNSTICHED 3PC PREMIUM ',
          price: 'PKR 4,990.00',
        },
        {
          id: 5,
          image: '/images/Rectangle63.png',
          title: 'NEW',
          text: 'UNSTICHED 3PC PREMIUM ',
          price: 'PKR 4,990.00',
        },
        {
          id: 6,
          image: '/images/Rectangle64.png',
          title: 'NEW',
          text: 'UNSTICHED 3PC PREMIUM ',
          price: 'PKR 4,990.00',
        },
        {
          id: 7,
          image: '/images/Rectangle63.png',
          title: 'NEW',
          text: 'UNSTICHED 3PC PREMIUM ',
          price: 'PKR 4,990.00',
        },
        {
          id: 8,
          image: '/images/Rectangle64.png',
          title: 'NEW',
          text: 'UNSTICHED 3PC PREMIUM ',
          price: 'PKR 4,990.00',
        },
      ],
    }
  },
}
</script>
<style scoped>
* {
  box-sizing: border-box;
}
.productpage1-column {
  float: left;
  width: 25%;
  padding: 10px;
}
.productpage1-column strong {
  display: flex;
  justify-content: center;
  align-items: center;
}
.productpage1-column p {
  display: flex;
  justify-content: center;
  align-items: center;
}
.productpage1-buttons {
  display: flex;
  justify-content: center;
  align-items: center;
}
/* Clearfix (clear floats) */
.productpage1::after {
  content: '';
  clear: both;
  display: table;
}

/* Responsive layout - makes the three columns stack on top of each other instead of next to each other */
@media screen and (max-width: 768px) {
  .productpage1-column {
    width: 100%;
  }
}
</style>
