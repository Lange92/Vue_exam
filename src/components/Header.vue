<template>
  <div>
    <div class="navigationbar">
      <div class="main-header">
        <div class="footer-copyright">
          <h5>Currency:</h5>
          <div>
            <select name id="currency">
              <option value="GDP">GDP</option>
              <option value="DKK">DKK</option>
              <option value="EURO">EURO</option>
            </select>
          </div>
          <div class="push"></div>
          <div class="hover-header">
            <router-link to="/register">
              <h5>Register</h5>
            </router-link>
          </div>
          <div class="hover-header">
            <h5>Log in</h5>
          </div>
          <div>
            <ul>
              <li>
                <button class="shopping-cart">
                  <div>
                    <img src="..\assets\imgs\shoppingCartPic.png" />
                  </div>
                  <div>
                    <h5>
                      empty
                      <i class="down i-arrow-white"></i>
                    </h5>
                  </div>
                </button>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div class="width-container-two">
        <div class="second-nav">
          <div class="logo">
            <router-link to="/">
              <h3><span>Avenue</span> Fashion</h3>
            </router-link>
          </div>
          <div class="push">
            <div class="nav-container">
              <nav>
                <ul id="category">
                  <li class="category-menu">
                    <a>
                      Mens
                      <i class="down i-arrow-grey"></i>
                    </a>
                    <div class="category-menu__tab">
                      <div class="category-products">
                        <div class="category__list">
                          <h4>CASUALS</h4>
                          <ul v-for="item in casual" :key="item">
                            <li class="product-item">
                              <a href="#">{{ item }}</a>
                            </li>
                          </ul>
                        </div>
                        <div class="category__list">
                          <h4>Formals</h4>
                          <ul v-for="item in formal" :key="item">
                            <li class="product-item">
                              <a href="#">{{ item }}</a>
                            </li>
                          </ul>
                        </div>
                      </div>
                      <div class="product-item__banner">
                        <span>Autumn Sale!</span>
                        <h4>up to 50% off</h4>
                      </div>
                    </div>
                  </li>
                  <li class="category-menu">
                    <a>
                      Womens
                      <i class="down i-arrow-grey"></i>
                    </a>
                    <div class="category-menu__tab">
                      <div class="category-products">
                        <div class="category__list">
                          <h4>CASUALS</h4>
                          <ul v-for="item in casual" :key="item">
                            <li class="product-item">
                              <a href="#">{{ item }}</a>
                            </li>
                          </ul>
                        </div>
                        <div class="category__list">
                          <h4>Formals</h4>
                          <ul v-for="item in formal" :key="item">
                            <li class="product-item">
                              <a href="#">{{ item }}</a>
                            </li>
                          </ul>
                        </div>
                      </div>
                      <div class="product-item__banner">
                        <span>Autumn Sale!</span>
                        <h4>up to 50% off</h4>
                      </div>
                    </div>
                  </li>
                  <router-link to="Thebrand">
                    <li>the brand</li>
                  </router-link>
                  <li>Local stores</li>
                  <li>look book</li>
                </ul>
              </nav>
              <div class="searchfield-container">
                <form action>
                  <div>
                    <input type="text" name="search" placeholder="Search.." />
                  </div>
                </form>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      casual: [
        'Jackets',
        'Hoodies & Sweatshirts',
        'Polo Shirts',
        'Sportswear',
        'Trousers & Chinos',
        'T-shirts'
      ],
      formal: ['Jackets', 'Shirts', 'Suits', 'Trousers']
    }
  }
}
</script>
