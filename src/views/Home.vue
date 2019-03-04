<template>
  <div class="home">
    <div class="promo-slider">
      <img
        src="../assets/imgs/landingpageguy.png"
        alt="landing page picture"
        class="img-responsive"
      />
      <button class="slide-btn">Shop Men's collection</button>
    </div>
    <div class="width-container-two">
      <hr />
      <div class="clothing-deals">
        <ul>
          <div>
            <li>popular</li>
          </div>
          <div>
            <li>new arrivals</li>
          </div>
          <div>
            <li>best sellers</li>
          </div>
          <div>
            <li>special offers</li>
          </div>
          <div>
            <li>coming soon</li>
          </div>
        </ul>
      </div>
    </div>
    <div class="width-container-two">
      <div class="container">
        <div
          v-for="product in products"
          :key="product.id"
          class="image-container"
        >
          <router-link :to="'/Productview/' + product.id">
            <img src="../assets/imgs/homepagegrid1.png" />
          </router-link>
          <div class="top-left"><span>$</span>89.99</div>
          <div class="product-desc">
            <span>womens burnt orange casual tee $29.95</span>
            Classic casual t-short for women on the move. 100% cotton.
          </div>
        </div>
        <!-- <div class="image-container">
          <img src="../assets/imgs/homepagegrid2.png" />
          <div class="top-left"><span>$</span>47.50</div>
          <div class="product-desc">
            <span>womens burnt orange casual tee $29.95</span>
            Classic casual t-short for women on the move. 100% cotton.
          </div>
        </div>
        <div class="big image-container">
          <img src="../assets/imgs/homepagegrid3.png" alt />
          <div class="top-left"><span>$</span>89.99</div>
          <div class="product-desc big-pic">
            <span>womens burnt orange casual tee $29.95</span>
            Classic casual t-short for women on the move. 100% cotton.
          </div>
        </div>
        <div class="big image-container">
          <img src="../assets/imgs/homepagegrid4.png" alt />
          <div class="top-left"><span>$</span>69.95</div>
          <div class="product-desc big-pic">
            <span>womens burnt orange casual tee $29.95</span>
            Classic casual t-short for women on the move. 100% cotton.
          </div>
        </div>
        <div class="image-container">
          <img src="../assets/imgs/homepagegrid5.png" alt />
          <div class="top-left"><span>$</span>29.95</div>
          <div class="product-desc">
            <span>womens burnt orange casual tee $29.95</span>
            Classic casual t-short for women on the move. 100% cotton.
          </div>
        </div>
        <div class="image-container">
          <img src="../assets/imgs/homepagegrid6.png" alt />
          <div class="top-left"><span>$</span>34.79</div>
          <div class="product-desc">Hello</div>
          <div class="product-desc">
            <span>womens burnt orange casual tee $29.95</span>
            Classic casual t-short for women on the move. 100% cotton.
          </div>
        </div>-->
      </div>
      <hr />
    </div>
    <div class="width-container-three">
      <div class="lookbook-container__item">
        <div class="image-container__two">
          <img src="../assets/imgs/lookbook1.png" alt="pic" />
          <div class="lookbook-container__button">
            <h2>
              men's
              <span>lookbook</span>
            </h2>
            <p>
              Lorem ipsum dolor sit amet eras facilisis consectetur adipiscing
              elit lor, integer lorem consecteur dignissim laciniqui. Elementum
              metus facilisis ut phasellu.
            </p>
          </div>
          <button>view now</button>
        </div>
        <div class="image-container__two">
          <img src="../assets/imgs/lookbook2.png" alt="pic" />
          <div class="lookbook-container__button">
            <h2>
              women's
              <span>lookbook</span>
            </h2>
            <p>
              Lorem ipsum dolor sit amet eras facilisis consectetur adipiscing
              elit lor, integer lorem consecteur dignissim laciniqui. Elementum
              metus facilisis ut phasellu.
            </p>
          </div>
          <button>view now</button>
        </div>
        <div class="image-container__two">
          <img src="../assets/imgs/lookbook3.png" alt="pic" />
          <div class="lookbook-container__button">
            <h2>
              your
              <span>lookbook</span>
            </h2>
            <p>
              Lorem ipsum dolor sit amet eras facilisis consectetur adipiscing
              elit lor, integer lorem consecteur dignissim laciniqui. Elementum
              metus facilisis ut phasellu.
            </p>
          </div>
          <button>view now</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  data() {
    return {
      products: []
    }
  },
  created() {
    this.getData()
  },
  methods: {
    getData() {
      axios
        .get('https://my-json-server.typicode.com/Lange92/Vue_exam/products')
        .then(response => {
          this.products = response.data
          console.log(this.products)
        })
        .catch(err => console.log(err.message))
    }
  }
}
</script>
