<template>
  <div class="Product">
    <div class="landing-page">
      <img
        src="../assets/imgs/product-landing-pic.png"
        alt="Landing page picutre"
        class="img-landing-page"
      />
    </div>
    <div class="width-container-two">
      <div class="Pcontainer">
        <div>
          <img :src="require('@/assets/imgs/' + product.image)" alt />
        </div>
        <div class="Pcontainer__elem">
          <h1 class="Pcontainer__elem--h1">Ave classic sweatshirt</h1>
          <div class="Pcontainer__elem--review">
            <div>
              <p>
                <i class="far fa-star"></i>
                <i class="far fa-star"></i>
                <i class="far fa-star"></i>
                <i class="far fa-star"></i>
                <i class="far fa-star"></i> 3 Review(s)
              </p>
            </div>
            <div>
              <p>|</p>
            </div>
            <div>
              <p>Add a review</p>
            </div>
            <div>
              <p>|</p>
            </div>
            <div>
              <p>Share:</p>
            </div>
            <div>
              <i class="fab fa-facebook-f"></i>
            </div>
            <div>
              <i class="fab fa-twitter"></i>
            </div>
            <div>
              <i class="fab fa-instagram"></i>
            </div>
            <div>
              <i class="fab fa-pinterest"></i>
            </div>
          </div>
          <div class="Pcontainer__elem">
            <div class="Pcontainer__price">
              <h3>
                <span>£</span>
              </h3>
              <h3 class="Pcontainer__price--line">{{ product.price }}</h3>
              <h3>
                <span>£</span>
              </h3>
              <h3>{{ product.price }}</h3>
            </div>
          </div>
          <div class="Pcontainer__elem">
            <div class="Pcontainer__info">
              <h4>
                AVAILABILITY:
                <span>{{ product.availability }}</span>
              </h4>
              <h4>
                PRODUCT CODE:
                <span>{{ product.id }}</span>
              </h4>
              <h4>
                TAGS:
                <span class="Pcontainer__info--blue">{{ product.tags }}</span>
              </h4>
            </div>
          </div>
          <div class="Pcontainer__infotext">
            <p>{{ product.shortDescription }}</p>
            <ul class="Pcontainer__infotext--circle">
              <li>{{ product.descriptionPerks[0] }}</li>
              <li>{{ product.descriptionPerks[1] }}</li>
              <li>{{ product.descriptionPerks[2] }}</li>
              <li>{{ product.descriptionPerks[3] }}</li>
            </ul>
          </div>
          <div class="Pcontainer__input">
            <div>
              <h3>Colour</h3>
              <select name id="Pcontainer__input--option">
                <option value="GDP">Select Colour</option>
                <option value="DKK">{{ product.color[0] }}</option>
                <option value="EURO">{{ product.color[1] }}</option>
                <option value="EURO">{{ product.color[2] }}</option>
                <option value="EURO">{{ product.color[3] }}</option>
                <option value="EURO">{{ product.color[4] }}</option>
              </select>
            </div>
            <div>
              <h3>size</h3>
              <select name id="Pcontainer__input--option">
                <option value="GDP">Select Size</option>
                <option value="DKK">{{ product.sizes[0] }}</option>
                <option value="EURO">{{ product.sizes[1] }}</option>
                <option value="EURO">{{ product.sizes[2] }}</option>
              </select>
            </div>
            <div>
              <h3>qty</h3>
              <input type="number" name="quantity" min="1" max="9" />
            </div>
          </div>
          <div class="Pcontainer__button">
            <button>
              <i class="fas fa-shopping-cart"></i>
              <h3>Add to cart</h3>
            </button>
            <button>
              <i class="far fa-heart"></i>
              <h3>add to lookbook</h3>
            </button>
          </div>
          <div class="Pcontainer__compare">
            <i class="fas fa-search"></i>
            <p>Add to compare</p>
          </div>
        </div>
        <div id="tabs" class="container__details">
          <div class="tabs">
            <a
              v-on:click="activetab = 1"
              v-bind:class="[activetab === 1 ? 'active' : '']"
              >Description</a
            >
            <a
              v-on:click="activetab = 2"
              v-bind:class="[activetab === 2 ? 'active' : '']"
              >video</a
            >
            <a
              v-on:click="activetab = 3"
              v-bind:class="[activetab === 3 ? 'active' : '']"
              >SIze &amp; Specs</a
            >
            <a
              v-on:click="activetab = 4"
              v-bind:class="[activetab === 4 ? 'active' : '']"
              >Delivery &amp; returns</a
            >
            <a
              v-on:click="activetab = 5"
              v-bind:class="[activetab === 5 ? 'active' : '']"
              >Reviews</a
            >
          </div>

          <div class="content">
            <div v-if="activetab === 1" class="tabcontent">
              <h5>{{ product.longDescription.highlightText }}</h5>
              <p>{{ product.longDescription.longText }}</p>
            </div>
            <div v-if="activetab === 2" class="tabcontent">
              <h5>Video</h5>
              <p>{{ product.longDescription.longText }}</p>
            </div>
            <div v-if="activetab === 3" class="tabcontent">
              <h5>Here you can find sizes</h5>
              <p>{{ product.sizeTab }}</p>
            </div>
            <div v-if="activetab === 4" class="tabcontent">
              <h5>WE DONT DELIVER OR RETURN</h5>
              <p>{{ product.delivery }}</p>
            </div>
          </div>
          <div v-if="activetab === 5" class="tabcontent">
            <h5>Our reviews are wonderful, you wouldnt believe it</h5>
            <p>{{ product.reviews }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  data: function() {
    return { activetab: 1, product: {} }
  },
  created() {
    this.getData()
  },
  methods: {
    getData() {
      let productId = this.$route.params.id
      axios
        .get(
          'https://my-json-server.typicode.com/Lange92/Vue_exam/products/' +
            productId
        )
        .then(response => {
          this.product = response.data
          console.log(this.product)
        })
        .catch(err => console.log(err.message))
    }
  }
}
</script>
