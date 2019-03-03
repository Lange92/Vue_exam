<template>
  <div class="Product">
    <div class="landing-page">
      <img
        src="../assets/imgs/product-landing-pic.png"
        alt="Landing page picutre"
        class="img-landing-page"
      />
    </div>
    <div class="width-container">
      <div class="Pcontainer">
        <div>
          <img src="../assets/imgs/productpic1.png" alt />
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
              <h3 class="Pcontainer__price--line">107</h3>
              <h3>
                <span>£</span>
              </h3>
              <h3>89.99</h3>
            </div>
          </div>
          <div class="Pcontainer__elem">
            <div class="Pcontainer__info">
              <h4>
                AVAILABILITY:
                <span>In stock</span>
              </h4>
              <h4>
                PRODUCT CODE:
                <span>#499577</span>
              </h4>
              <h4>
                TAGS:
                <span class="Pcontainer__info--blue"
                  >Classic, Casual, V-Neck, Loose</span
                >
              </h4>
            </div>
          </div>
          <div class="Pcontainer__infotext">
            <p>
              Donec sem lorem laoreet tempor un risus vitae, rutrum sodales nibh
              suspendisse est congue metus nunc, id viverra elit loreti rhoncus
              quis consecteur es. Donec pulvinar tempor lorem a pretium justo
              interdum.
            </p>
            <ul class="Pcontainer__infotext--circle">
              <li>Elsaticated cuffs</li>
              <li>Casual fit</li>
              <li>100% Cotton</li>
              <li>Free Shipping with 4 days delivery</li>
            </ul>
          </div>
          <div class="Pcontainer__input">
            <div>
              <h3>Colour</h3>
              <select name id="Pcontainer__input--option">
                <option value="GDP">Select Colour</option>
                <option value="DKK">Red</option>
                <option value="EURO">Blue</option>
                <option value="EURO">Green</option>
              </select>
            </div>
            <div>
              <h3>size</h3>
              <select name id="Pcontainer__input--option">
                <option value="GDP">Select Size</option>
                <option value="DKK">S</option>
                <option value="EURO">M</option>
                <option value="EURO">L</option>
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
              <h5>Nunc egestas posuere enim, eu maximus erat posuere eget</h5>
              <p>
                Sed ut mi mollis, consequat nulla lacinia, hendrerit turpis.
                Nulla sapien magna, interdum quis pretium nec, pharetra at
                felis. Curabitur dictum sapien est, eget ultricies turpis porta
                vel. Nam suscipit nec lacus sed imperdiet. Vestibulum a purus
                risus. Nulla et dictum augue, nec efficitur mi. Nam sit amet
                pretium elit. Aliquam congue, ligula id vehicula vestibulum,
                orci ex vulputate lacus, ac malesuada elit dolor eget ex. Sed
                quis aliquet risus, ut cursus lectus. In eget lorem tellus.
                Quisque eleifend varius nisi nec sagittis. Nulla ullamcorper
                imperdiet justo, ut venenatis purus lobortis ut. Nunc sagittis
                urna et hendrerit sodales. Nunc molestie risus nec fringilla
                lacinia. Nulla facilisi. Etiam neque velit, tristique eget
                sollicitudin eget, placerat at metus. Proin dictum lobortis
                velit, id suscipit orci faucibus ut. Aliquam erat volutpat.
                Vivamus feugiat justo in diam placerat, id dignissim elit
                auctor. Vestibulum scelerisque sem et lobortis ultricies. Morbi
                suscipit nulla urna. Suspendisse potenti. Nullam varius quam sed
                nisl dignissim, vel faucibus ipsum blandit. Vivamus at suscipit
                augue. Nam finibus gravida lorem eu viverra. Praesent rhoncus
                imperdiet ultricies. Nullam pretium cursus augue auctor
                vulputate. Quisque a convallis diam commodo eget diam id,
                eleifend dictum libero. Etiam varius, nisi vel dignissim
                sodales, enim dui posuere mauris, in aliquet lorem eros eget
                neque.
              </p>
            </div>
            <div v-if="activetab === 2" class="tabcontent">
              <h5>Video</h5>
              <p>
                Sed ut mi mollis, consequat nulla lacinia, hendrerit turpis.
                Nulla sapien magna, interdum quis pretium nec, pharetra at
                felis. Curabitur dictum sapien est, eget ultricies turpis porta
                vel. Nam suscipit nec lacus sed imperdiet. Vestibulum a purus
                risus. Nulla et dictum augue, nec efficitur mi. Nam sit amet
                pretium elit. Aliquam congue, ligula id vehicula vestibulum,
                orci ex vulputate lacus, ac malesuada elit dolor eget ex. Sed
                quis aliquet risus, ut cursus lectus. In eget lorem tellus.
                Quisque eleifend varius nisi nec sagittis. Nulla ullamcorper
                imperdiet justo, ut venenatis purus lobortis ut. Nunc sagittis
                urna et hendrerit sodales. Nunc molestie risus nec fringilla
              </p>
            </div>
            <div v-if="activetab === 3" class="tabcontent">
              <h5>Here you can find sizes</h5>
              <p>
                Sed ut mi mollis, consequat nulla lacinia, hendrerit turpis.
                Nulla sapien magna, interdum quis pretium nec, pharetra at
                felis. Curabitur dictum sapien est, eget ultricies turpis porta
                vel. Nam suscipit nec lacus sed imperdiet. Vestibulum a purus
                risus. Nulla et dictum augue, nec efficitur mi. Nam sit amet
                pretium elit. Aliquam congue, ligula id vehicula vestibulum,
                orci ex vulputate lacus, ac malesuada elit dolor eget ex. Sed
                quis aliquet risus, ut cursus lectus. In eget lorem tellus.
                Quisque eleifend varius nisi nec sagittis. Nulla ullamcorper And
                there is a lot more to find if you look
              </p>
            </div>
            <div v-if="activetab === 4" class="tabcontent">
              <h5>WE DONT DELIVER OR RETURN</h5>
              <p>
                Sed ut mi mollis, consequat nulla lacinia, hendrerit turpis.
                Nulla sapien magna, interdum quis pretium nec, pharetra at
                felis. Curabitur dictum sapien est, eget ultricies turpis porta
                vel. Nam suscipit nec lacus sed imperdiet. Vestibulum a purus
                risus. Nulla et dictum augue, nec efficitur mi. Nam sit amet
                pretium elit. Aliquam congue, ligula id vehicula vestibulum,
                orci ex vulputate lacus, ac malesuada elit dolor eget ex. Sed
                quis aliquet risus, ut cursus lectus. In eget lorem tellus.
                Quisque eleifend varius nisi nec sagittis. Nulla ullamcorper And
                there is a lot more to find if you look
              </p>
            </div>
          </div>
          <div v-if="activetab === 5" class="tabcontent">
            <h5>Our reviews are wonderful, you wouldnt believe it</h5>
            <p>
              Sed ut mi mollis, consequat nulla lacinia, hendrerit turpis. Nulla
              sapien magna, interdum quis pretium nec, pharetra at felis.
              Curabitur dictum sapien est, eget ultricies turpis porta vel. Nam
              suscipit nec lacus sed imperdiet. Vestibulum a purus risus. Nulla
              et dictum augue, nec efficitur mi. Nam sit amet pretium elit.
              Aliquam congue, ligula id vehicula vestibulum, orci ex vulputate
              lacus, ac malesuada elit dolor eget ex. Sed quis aliquet risus, ut
              cursus lectus. In eget lorem tellus. Quisque eleifend varius nisi
              nec sagittis. Nulla ullamcorper And there is a lot more to find if
              you looklacus, ac malesuada elit dolor eget ex. Sed quis aliquet
              risus, ut cursus lectus. In eget lorem tellus. Quisque eleifend
              varius nisi nec sagittis. Nulla ullamcorper And there is a lot
              more to find if you look
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: function() {
    return { activetab: 1 }
  }
}
</script>

<style></style>
