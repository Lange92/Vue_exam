<template>
  <div class="register">
    <div class="landing-page">
      <img
        src="../assets/imgs/register-landing-pic.png"
        alt="Landing page picutre"
        class="img-landing-page"
      />
    </div>
    <div class="width-container">
      <form id="app" @submit="checkForm" action="/something" method="post">
        <div class="RegContainer">
          <div>
            <h2>Sign in</h2>
            <input
              type="text"
              name="email"
              id="email"
              v-model="email"
              placeholder="Your Email..."
            />
          </div>
          <div>
            <input
              type="text"
              name="password"
              id="password"
              v-model="password"
              placeholder="Your Password..."
            />
          </div>
          <div class="RegContainer__input--button">
            <button type="submit" v-on:click="checkForm()">Sign in</button>
          </div>
          <div>
            <h2>Register</h2>
            <input
              type="text"
              name="emailReg"
              id="emailReg"
              v-model="emailReg"
              placeholder="Your Email.."
            />
          </div>
          <div>
            <input
              type="text"
              name="passwordReg"
              id="passwordReg"
              v-model="passwordReg"
              placeholder="Your Password.."
            />
          </div>
          <div>
            <input
              type="text"
              name="confirmPasswordReg"
              id="confirmPasswordReg"
              v-model="confirmPasswordReg"
              placeholder="Confirm Password.."
            />
          </div>
          <div class="RegContainer__input--align">
            <form action="/action_page.php">
              <input type="checkbox" name="vehicle1" value="Bike" />
              <h4>
                Sign up for exlusive updates, discounts new arrivals, contests
                and more!
              </h4>
            </form>
          </div>
          <div class="RegContainer__input--buttonTwo">
            <button type="submit" v-on:click="checkForm2()">
              Create Account
            </button>
          </div>
          <div class="RegContainer__input--p">
            <p>
              Forgot your password
              <i class="fas fa-long-arrow-alt-right"></i>
            </p>
          </div>
          <div>
            <p>
              By clicking ‘Create Account’, you agree to our
              <span>
                Privacy Policy
                <i class="fas fa-long-arrow-alt-right"></i>
              </span>
            </p>
          </div>
          <div v-if="errors.length" class="RegContainer__error">
            <b>Please correct the following error(s):</b>
            <ul>
              <li v-for="error in errors" :key="error">{{ error }}</li>
              <li v-for="error in errorsTwo" :key="error">{{ error }}</li>
            </ul>
          </div>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      errors: [],
      email: null,
      password: null,
      emailReg: null,
      passwordReg: null,
      confirmPasswordReg: null
    }
  },
  methods: {
    checkForm: function(e) {
      if (this.email && this.password) return true
      this.errors = []
      if (!this.email) this.errors.push('Email required.')
      if (!this.password) this.errors.push('Password Required')
      e.preventDefault()
    },
    checkForm2: function(e) {
      if (this.emailReg && this.passwordReg && this.confirmPasswordReg)
        return true
      this.errorsTwo = []
      if (!this.emailReg) this.errorsTwo.push('Email required.')
      if (!this.passwordReg) this.errorsTwo.push('Password Required')
      if (!this.confirmPasswordReg) this.errorsTwo.push('Confirmation needed')
      e.preventDefault()
    }
  }
}
</script>
