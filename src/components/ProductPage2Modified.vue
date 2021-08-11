<script>
import Navbar from './Navbar.vue'
import Header1 from './Header1.vue'
import Footer from './Footer.vue'
export default {
  name: 'ProductPage2Modified',
  components: {
    Navbar,
    Header1,
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
          size: 'small',
        },
        {
          id: 2,
          image: '/images/Rectangle56.png',
          title: 'NEW',
          text: 'UNSTICHED 3PC PREMIUM ',
          price: 'PKR 4,990.00',
          size: 'small',
        },
        {
          id: 3,
          image: '/images/Rectangle63.png',
          title: 'NEW',
          text: 'UNSTICHED 3PC PREMIUM ',
          price: 'PKR 4,990.00',
          size: 'large',
        },
        {
          id: 4,
          image: '/images/Rectangle64.png',
          title: 'NEW',
          text: 'UNSTICHED 3PC PREMIUM ',
          price: 'PKR 4,990.00',
          size: 'small',
        },
        {
          id: 5,
          image: '/images/Rectangle63.png',
          title: 'NEW',
          text: 'UNSTICHED 3PC PREMIUM ',
          price: 'PKR 4,990.00',
          size: 'small',
        },
        {
          id: 6,
          image: '/images/Rectangle64.png',
          title: 'NEW',
          text: 'UNSTICHED 3PC PREMIUM ',
          price: 'PKR 4,990.00',
          size: 'large',
        },
        {
          id: 7,
          image: '/images/Rectangle63.png',
          title: 'NEW',
          text: 'UNSTICHED 3PC PREMIUM ',
          price: 'PKR 4,990.00',
          size: 'small',
        },
        {
          id: 8,
          image: '/images/Rectangle64.png',
          title: 'NEW',
          text: 'UNSTICHED 3PC PREMIUM ',
          price: 'PKR 4,990.00',
          size: 'small',
        },
      ],
    }
  },
  render() {
    return (
      <div>
        <Navbar />
        <Header1 />
        <div id="productpage2-row-wrapper" class="productpage2-row">
          <div className="productpage2-myclass">
            {this.products && this.products.length
              ? this.products.map((item) =>
                  this.products.indexOf(item) === 2 ||
                  (this.products.indexOf(item) > 2 &&
                    (this.products.indexOf(item) + 1) % 3 === 0) ? (
                    <div className="productpage2-myclass2">
                      <img class="card img-top" src={item.image} alt="" />
                      <div class="card-body">
                        <h5 class="card-title">
                          <strong>{item.title}</strong>
                        </h5>
                        <p class="card-text">
                          <strong>{item.text}</strong>
                        </p>
                        <p class="card-text">
                          <small class="text-muted">{item.price}</small>
                        </p>
                      </div>
                    </div>
                  ) : (
                    <div id="card-child" class="card border-0">
                      <img
                        id="img-width"
                        class="card img-top"
                        src={item.image}
                        alt=""
                      />
                      <div id="productpage1-content" class="card-body">
                        <h5 class="card-title">
                          <strong>{item.title}</strong>
                        </h5>
                        <p class="card-text">
                          <strong>{item.text}</strong>
                        </p>
                        <p class="card-text">
                          <small class="text-muted">{item.price}</small>
                        </p>
                      </div>
                    </div>
                  ),
                )
              : null}
          </div>
        </div>
        <Footer />
      </div>
    )
  },
}
</script>
<style scoped>
#productpage2-row-wrapper {
  display: flex;
  justify-content: center;
  width: 100%;
  margin-right: 0px;
  margin-left: 0px;
}

.productpage2-myclass {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  width: 100%;
  margin-left: 10%;
}

.productpage2-myclass2 {
  display: flex;
  flex-direction: column;
  margin-right: 30%;
  margin-left: 20%;
  width: 30%;
}

#card-child {
  margin-right: 200px;

  width: 30%;
}
#productpage1-content {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
@media only screen and (max-width: 768px) {
  .productpage2-myclass2 {
    margin-right: 0;
    margin-left: 0;
    width: 90%;
  }
  #card-child {
    margin-right: 0px;
    width: 90%;
  }
  #productpage2-row-wrapper {
    margin-right: 0px;
  }
}
</style>
