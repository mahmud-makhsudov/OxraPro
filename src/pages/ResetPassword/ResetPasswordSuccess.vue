<template>
  <div>
    <div class="auth-page" v-if="isSend">
      <div
        class="auth-header d-flex justify-content-between align-items-center"
      >
        <img src="@/assets/logo-new.svg" />
        <div class="auth-header-actions">
          <a href="tel:+7888">+7 (800) 333-98-87</a>
          <a href="mailto:sale@oxrapro.ru">sale@oxrapro.ru</a>
        </div>
      </div>
      <b-container>
        <div class="auth-form">
          <form>
            <div class="auth-form-inner">
              <div class="form-group auth-title">Восстановить пароль</div>
              <div class="form-group auth-subtitle text-center">
                Придумайте и повторите новый пароль
              </div>
              <div class="form-group">
                <div class="input-group mb-2">
                  <div class="input-group-prepend">
                    <div class="input-group-text">
                      <svg
                        width="10"
                        height="11"
                        viewBox="0 0 10 11"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M4.92779 3.86144e-05C3.56364 -0.00648805 2.36589 0.814827 1.78725 2.09811C1.48963 2.81065 1.50733 3.7865 1.52113 4.63863H0V11H10V4.63863H8.34582V3.43216C8.34582 2.95917 8.24884 2.52259 8.06767 2.09811C7.53801 0.879433 6.29194 0.00656528 4.92779 3.86144e-05ZM4.92779 2.02561C5.72467 2.04684 6.30592 2.64852 6.3406 3.42008V4.63863H3.52635V3.43216C3.60156 2.59227 4.1309 2.00437 4.92779 2.02561Z"
                          fill="#4A5056"
                        />
                      </svg>
                    </div>
                  </div>
                  <input
                    type="password"
                    class="form-control"
                    id="inlineFormInputGroup"
                    placeholder="password"
                  />
                </div>
              </div>
              <div class="form-group">
                <div class="input-group mb-2">
                  <div class="input-group-prepend">
                    <div class="input-group-text">
                      <svg
                        width="10"
                        height="11"
                        viewBox="0 0 10 11"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M4.92779 3.86144e-05C3.56364 -0.00648805 2.36589 0.814827 1.78725 2.09811C1.48963 2.81065 1.50733 3.7865 1.52113 4.63863H0V11H10V4.63863H8.34582V3.43216C8.34582 2.95917 8.24884 2.52259 8.06767 2.09811C7.53801 0.879433 6.29194 0.00656528 4.92779 3.86144e-05ZM4.92779 2.02561C5.72467 2.04684 6.30592 2.64852 6.3406 3.42008V4.63863H3.52635V3.43216C3.60156 2.59227 4.1309 2.00437 4.92779 2.02561Z"
                          fill="#4A5056"
                        />
                      </svg>
                    </div>
                  </div>
                  <input
                    type="password"
                    class="form-control"
                    id="inlineFormInputGroup"
                    placeholder="password"
                  />
                </div>
              </div>
              <div class="form-group text-center auth-submit">
                <button
                  type="submit"
                  class="btn btn-primary mb-2"
                  @click="resetSend"
                >
                  Восстановить
                </button>
              </div>
            </div>
          </form>
        </div>
      </b-container>
    </div>
    <div class="auth-page" v-else>
      <div
        class="auth-header d-flex justify-content-between align-items-center"
      >
        <img src="@/assets/logo-new.svg" />
        <div class="auth-header-actions">
          <a href="tel:+7888">+7 (800) 333-98-87</a>
          <a href="mailto:sale@oxrapro.ru">sale@oxrapro.ru</a>
        </div>
      </div>
      <b-container>
        <div class="auth-form">
          <form>
            <div class="auth-form-inner">
              <div class="form-group auth-subtitle text-center">
                Ваш пароль успешно изменен!
              </div>
              <div class="form-group text-center auth-submit">
                <button
                  type="submit"
                  class="btn btn-primary mb-2"
                  @click="resetSend"
                >
                  Войти в личный кабинет
                </button>
              </div>
            </div>
          </form>
        </div>
      </b-container>
    </div>
  </div>
</template>

<script>
import Widget from "@/components/Widget/Widget";
import { mapState, mapActions } from "vuex";

import config from "../../config";

export default {
  name: "LoginPage",
  components: { Widget },
  data() {
    return {
      isSend: true,
    };
  },
  computed: {
    ...mapState("auth", {
      isFetching: (state) => state.isFetching,
      errorMessage: (state) => state.errorMessage,
    }),
  },
  methods: {
    resetSend() {
      this.isSend = false;
    },
    ...mapActions("auth", ["loginUser", "receiveToken", "receiveLogin"]),
    login() {
      const email = this.$refs.email.value;
      const password = this.$refs.password.value;

      if (email.length !== 0 && password.length !== 0) {
        this.loginUser({ email, password });
      }
    },
    googleLogin() {
      this.loginUser({ social: "google" });
    },
    microsoftLogin() {
      this.loginUser({ social: "microsoft" });
    },
  },
  created() {
    const token = this.$route.query.token;
    if (token) {
      this.receiveToken(token);
    } else if (this.isAuthenticated(localStorage.getItem("token"))) {
      this.receiveLogin();
    }
  },
  mounted() {
    const creds = config.auth;
    this.$refs.email.value = creds.email;
    this.$refs.password.value = creds.password;
  },
};
</script>
<style lang="scss" scoped>
</style>
