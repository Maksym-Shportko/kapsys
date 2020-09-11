<template>
  <section class="login-page">
    <div class="decoration"></div>
    <div class="container d-flex justify-content-center align-items-center">
      <div class="row">
        <div class="col text-center">
          <img src="../../assets/logo_white.svg" class="login-page__title" alt="">
          <form @submit.prevent="emailValidation" class="d-flex justify-content-center">
            <div class="login-form p-4">
              <h2 class="login-form__title">Log In</h2>
              <div class="text-left pb-4">
                <label class="d-block font-weight-bold" for="email">Email</label>
                <input
                  class="login-form__input"
                  placeholder="Enter your Email"
                  type="text"
                  id="email"
                  v-model.trim="email"
                  :class="{invalid:($v.email.$dirty && !$v.email.required)||($v.email.$dirty && !$v.email.email)}"
                />
              </div>
              <div class="text-left pb-4 position-relative">
                <div class="d-flex justify-content-between">
                  <label class="d-block font-weight-bold" for="password">Password</label>
                  <router-link class="d-block text-secondary" to="/">Forgot Password?</router-link>
                </div>
                <span @click="isShowPwd = !isShowPwd" class="password-eye" id="eye"></span>
                <input
                  class="login-form__input"
                  placeholder="Enter Password"
                  :type="isShowPwd ? 'text' : 'password'"
                  id="password"
                  v-model.trim="password"
                  :class="{invalid:($v.password.$dirty && !$v.password.required)||($v.password.$dirty && !$v.password.minLength)}"
                />
              </div>
              <button
                class="w-100 rounded border-0 mb-4 p-2 text-white login-form__submit"
                type="submit"
              >Log In</button>
              <p>
                <span class="text-secondary">Don't have an account?</span>
                <router-link to="/">Sign Up</router-link>
              </p>
            </div>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { email, required, minLength } from "vuelidate/lib/validators";

export default {
  name: "LoginModal",
  data: () => ({
    email: "",
    password: "",
    isShowPwd: false,
  }),
  validations: {
    email: { email, required },
    password: { required, minLength: minLength(6) },
  },
  methods: {
    emailValidation() {
      if(this.$v.$invalid) {
        this.$v.$touch()
        return
      }
      this.$router.push("/adminpanel");
    },
  },
};
</script>

<style lang="scss" >
.decoration {
  background: url("../../assets/logo-symbol-white.svg");
  background-size: 100px;
  width: 1046px;
  position: absolute;
  background-position: center;
  height: 950px;
  background-repeat: round;
  transform: rotateZ(30deg) scale(2);
}
.login-page {
  // background: url("../../assets/logo-symbol-white.svg");
  height: 100vh;
  position: relative;
  & .container {
    padding-top: 100px;
  }
  &__title {
    margin-bottom: 70px;
    height: 50px;
  }
  .login-form {
    background: #ffffff;
    width: 400px;
    box-shadow: 1px 1px 9px 0px black;
    border-radius: 8px;
    &__title {
      padding: 20px;
      font-weight: 700;
    }
    &__input {
      width: 100%;
      padding: 5px 15px;
      border-radius: 3px;
      border: 1px solid gray;
    }
    &__submit {
      background-color: #79d4f1;
    }
  }
  .password-eye {
    background: url("../../assets/vision.png") no-repeat;
    display: block;
    height: 15px;
    width: 18px;
    position: absolute;
    bottom: 35px;
    right: 20px;
    cursor: pointer;
  }
  .alert {
    display: none;
    position: absolute;
    top: 0;
    right: 0;
    left: 0;
    text-align: center;
  }
}
.invalid {
  border-bottom: 2px solid red!important;
}
</style>
