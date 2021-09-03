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
                Введите свой email, мы отправим вам ссылку <br />
                для изменения пароля.
              </div>
              <div class="form-group">
                <div class="input-group mb-2">
                  <div class="input-group-prepend">
                    <div class="input-group-text">
                      <svg
                        width="12"
                        height="12"
                        viewBox="0 0 12 12"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M12 5.35338C12 5.81454 11.9448 6.27068 11.8344 6.7218C11.724 7.17293 11.5533 7.58396 11.3225 7.95489C11.1016 8.32581 10.8206 8.62155 10.4793 8.84211C10.138 9.05263 9.73651 9.15789 9.27478 9.15789C8.90339 9.15789 8.57716 9.07268 8.29611 8.90226C8.01506 8.7218 7.81932 8.49123 7.70891 8.21053H7.58846C7.3877 8.46115 7.11669 8.6817 6.77541 8.87218C6.44416 9.06266 6.04266 9.15789 5.57089 9.15789C4.67754 9.15789 3.98494 8.89223 3.4931 8.3609C3.01129 7.81955 2.77039 7.11278 2.77039 6.2406C2.77039 5.56892 2.91593 4.97744 3.20703 4.46617C3.49812 3.94486 3.90966 3.53885 4.44166 3.24812C4.97365 2.94737 5.601 2.79699 6.32371 2.79699C6.79548 2.79699 7.28231 2.84211 7.78419 2.93233C8.29611 3.01253 8.6926 3.10276 8.97365 3.20301L8.82309 6.28571C8.81305 6.38596 8.80803 6.49123 8.80803 6.6015C8.80803 6.70175 8.80803 6.76692 8.80803 6.79699C8.80803 7.20802 8.86324 7.48371 8.97365 7.62406C9.0941 7.75439 9.22459 7.81955 9.36512 7.81955C9.59598 7.81955 9.7867 7.70927 9.93726 7.48872C10.0878 7.25815 10.1982 6.95739 10.2685 6.58647C10.3488 6.20551 10.389 5.78947 10.389 5.33835C10.389 4.49624 10.2183 3.78446 9.87704 3.20301C9.53576 2.61153 9.06901 2.1604 8.47679 1.84962C7.8946 1.53885 7.2271 1.38346 6.47428 1.38346C5.42033 1.38346 4.532 1.60401 3.80928 2.04511C3.09661 2.47619 2.55458 3.06767 2.18319 3.81955C1.81179 4.57143 1.6261 5.43358 1.6261 6.40601C1.6261 7.7594 1.98745 8.79699 2.71016 9.5188C3.44291 10.2406 4.49184 10.6015 5.85696 10.6015C6.43915 10.6015 7.04642 10.5363 7.67879 10.406C8.31117 10.2757 8.88833 10.1153 9.41029 9.92481V11.3383C8.92848 11.5388 8.39147 11.6992 7.79925 11.8195C7.20703 11.9398 6.57967 12 5.91719 12C4.67252 12 3.60853 11.7794 2.72522 11.3383C1.84191 10.8972 1.16437 10.2657 0.692597 9.44361C0.230866 8.61153 0 7.61404 0 6.45113C0 5.53885 0.150565 4.69173 0.451694 3.90977C0.752823 3.12782 1.18444 2.44612 1.74655 1.86466C2.3187 1.27318 3.00125 0.817042 3.79423 0.49624C4.5872 0.165413 5.47553 0 6.45922 0C7.53325 0 8.48682 0.215539 9.31995 0.646617C10.1531 1.07769 10.8055 1.69424 11.2773 2.49624C11.7591 3.29825 12 4.25063 12 5.35338ZM4.47177 6.27068C4.47177 6.82206 4.5872 7.21805 4.81807 7.45865C5.04893 7.69925 5.35508 7.81955 5.73651 7.81955C6.23839 7.81955 6.58971 7.6391 6.79046 7.2782C7.00125 6.90727 7.12672 6.42606 7.16688 5.83459L7.25721 4.21053C7.1468 4.19048 7.02133 4.17544 6.8808 4.16541C6.74028 4.14536 6.58469 4.13534 6.41405 4.13534C5.94228 4.13534 5.56085 4.2406 5.26976 4.45113C4.98871 4.65163 4.78294 4.91729 4.65245 5.24812C4.53199 5.56892 4.47177 5.90977 4.47177 6.27068Z"
                          fill="#575E66"
                        />
                      </svg>
                    </div>
                  </div>
                  <input
                    type="text"
                    class="form-control"
                    id="inlineFormInputGroup"
                    placeholder="ivanov@mail.ru"
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
              <div class="form-group auth-subtitle">
                Мы отправили ссылку для восстановления пароля на ваш email
                <span>ivanov@mail.ru</span>
                <p>В письме будет указана дальнейшая инструкция.</p>
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
.auth-form-inner {
    max-width: 373px;
}
.auth-subtitle {
    text-align: center;
    span {
        font-weight: 700;
    }
    p{
        margin-top: 10px;
    }
}
</style>
