<template>
  <view class="signin-page">
    <!-- Header -->
    <view class="header">
      <!-- Status bar -->
      <view class="status-bar">
        <view class="status-time">9:41</view>
        <view class="status-icons">
          <view class="network-signal">
            <view class="signal-bar bar1"></view>
            <view class="signal-bar bar2"></view>
            <view class="signal-bar bar3"></view>
            <view class="signal-bar bar4"></view>
          </view>
          <view class="wifi-icon">
            <svg width="17" height="12" viewBox="0 0 18 12" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path fill-rule="evenodd" clip-rule="evenodd" d="M17.4289 3.27C12.6935 -1.08957 5.40632 -1.08957 0.670926 3.27C0.586425 3.34856 0.537677 3.45822 0.535978 3.57358C0.534279 3.68894 0.579775 3.79999 0.661926 3.881L1.57293 4.781C1.7376 4.94536 2.00287 4.94978 2.17293 4.791C6.07088 1.23337 12.038 1.23337 15.9359 4.791C16.106 4.94978 16.3713 4.94536 16.5359 4.781L17.4469 3.881C17.5279 3.79878 17.5718 3.68703 17.5684 3.57166C17.565 3.45628 17.5146 3.34731 17.4289 3.27ZM9.04993 8.514C8.36234 8.514 7.74246 8.92819 7.47933 9.56344C7.2162 10.1987 7.36165 10.9299 7.84784 11.4161C8.33404 11.9023 9.06524 12.0477 9.70049 11.7846C10.3357 11.5215 10.7499 10.9016 10.7499 10.214C10.7499 9.27512 9.98881 8.514 9.04993 8.514ZM3.65793 6.29C6.74192 3.57922 11.3589 3.57922 14.4429 6.29C14.5304 6.36753 14.5816 6.47792 14.5845 6.59474C14.5873 6.71156 14.5415 6.82431 14.4579 6.906L13.5419 7.806C13.3814 7.96446 13.1263 7.97359 12.9549 7.827C10.7092 5.89837 7.39168 5.89837 5.14593 7.827C4.97452 7.97359 4.71941 7.96446 4.55893 7.806L3.64293 6.906C3.55937 6.82431 3.51354 6.71156 3.51638 6.59474C3.51923 6.47792 3.5705 6.36753 3.65793 6.29Z" fill="#1C2340"/>
            </svg>
          </view>
          <view class="battery-icon">
            <svg width="22" height="11" viewBox="0 0 23 12" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path fill-rule="evenodd" clip-rule="evenodd" d="M19.892 0H1.98904C1.0623 0 0.311035 0.751266 0.311035 1.678V9.51C0.311035 9.95503 0.487824 10.3818 0.80251 10.6965C1.1172 11.0112 1.544 11.188 1.98904 11.188H19.889C20.8158 11.188 21.567 10.4367 21.567 9.51V8.95H21.847C22.3104 8.95 22.686 8.57437 22.686 8.111V3.077C22.686 2.85448 22.5976 2.64108 22.4403 2.48374C22.283 2.32639 22.0696 2.238 21.847 2.238H21.567V1.678C21.567 0.752436 20.8176 0.00165476 19.892 0ZM19.333 2.238V4.476H20.452V6.714H19.333V8.95H2.54904V2.238H19.333ZM3.66804 3.357H14.857V7.833H3.66804V3.357Z" fill="#1C2340"/>
            </svg>
          </view>
        </view>
      </view>

      <!-- Navigation -->
      <view class="nav-header">
        <view class="back-button" @click="goBack">
          <svg width="27" height="18" viewBox="0 0 27 18" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M27 7.5H5.745L11.115 2.115L9 0L0 9L9 18L11.115 15.885L5.745 10.5H27V7.5Z" fill="#1C2340"/>
          </svg>
        </view>
        <text class="page-title">Sign in</text>
      </view>
    </view>

    <!-- Main Content -->
    <view class="content-area">
      <!-- Illustration -->
      <view class="illustration-section">
        <image 
          src="https://api.builder.io/api/v1/image/assets/TEMP/a0dc38c0d050da5db336fd6acac27e8fdb4764cd?width=672"
          class="signin-illustration"
          mode="aspectFit"
        />
      </view>

      <!-- Sign up card -->
      <view class="signup-card">
        <view class="card-header">
          <text class="card-title">Sign up with</text>
          <text class="card-subtitle">email and phone number</text>
        </view>

        <!-- Email input -->
        <view class="input-field email-field">
          <view class="input-icon">
            <svg width="16" height="12" viewBox="0 0 16 12" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path fill-rule="evenodd" clip-rule="evenodd" d="M2 0C0.896798 0.0032948 0.0032948 0.896798 0 2V10C0.0032948 11.1032 0.896798 11.9967 2 12H14C15.1032 11.9967 15.9967 11.1032 16 10V2C15.9967 0.896798 15.1032 0.0032948 14 0H2ZM8 7L2 2H14L8 7Z" fill="#242A37"/>
            </svg>
          </view>
          <input 
            class="input-text" 
            type="email" 
            v-model="email"
            placeholder="johndoe@mail.com"
          />
        </view>

        <!-- OR divider -->
        <view class="or-divider">
          <view class="divider-line"></view>
          <text class="or-text">OR</text>
          <view class="divider-line"></view>
        </view>

        <!-- Phone input -->
        <view class="input-field phone-field">
          <view class="country-selector">
            <view class="flag-circle">
              <svg width="26" height="26" viewBox="0 0 26 26" fill="none" xmlns="http://www.w3.org/2000/svg">
                <circle cx="13" cy="13" r="12.922" fill="white"/>
                <path d="M25.024 11.531V11.52C23.334 6.763 19.031 3.425 14.004 2.97C15.982 4.054 16.559 7.49 17.066 11.531C17.412 14.376 17.414 17.252 17.073 20.097C16.573 24.16 15.991 27.62 14.005 28.709C19.041 28.253 23.35 24.903 25.033 20.134C25.033 20.122 25.041 20.109 25.045 20.097C26.013 17.323 26.007 14.302 25.028 11.531H25.024Z" fill="#258F44"/>
                <path d="M17.727 11.531C17.217 7.49 15.979 4.054 14.001 2.97C13.617 2.936 13.231 2.917 12.84 2.917C7.369 2.917 2.491 6.361 0.66 11.517V11.528C-0.319 14.299 -0.325 17.32 0.643 20.094L0.655 20.131C2.478 25.301 7.363 28.758 12.844 28.759C13.235 28.759 13.622 28.74 14.005 28.706C15.991 27.617 17.237 24.158 17.738 20.094C18.078 17.25 18.074 14.375 17.727 11.531Z" fill="#359846"/>
                <circle cx="12.841" cy="13.841" r="4.761" fill="#EC1C24"/>
              </svg>
            </view>
            <svg width="12" height="8" viewBox="0 0 12 8" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M6 8L11.32 2.68L0.68 2.68L6 8Z" fill="#333333"/>
            </svg>
          </view>
          <input 
            class="input-text phone-text" 
            type="tel" 
            v-model="phone"
            placeholder="+880 111 222 333"
          />
          <view class="verified-icon">
            <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
              <circle cx="8" cy="8" r="8" fill="url(#paint0_linear)"/>
              <path d="M6.061 10.953L11.203 5.788H11.199C11.228 5.758 11.243 5.718 11.242 5.677C11.241 5.636 11.223 5.597 11.192 5.569L10.519 4.869C10.492 4.839 10.452 4.822 10.411 4.823C10.37 4.823 10.331 4.84 10.303 4.869L5.611 9.596L3.903 7.888C3.875 7.859 3.836 7.842 3.796 7.842C3.755 7.842 3.716 7.859 3.688 7.888L3.003 8.573C2.974 8.602 2.957 8.641 2.957 8.683C2.957 8.724 2.974 8.763 3.003 8.792L5.165 10.946C5.281 11.074 5.442 11.153 5.615 11.165C5.785 11.151 5.943 11.076 6.061 10.953Z" fill="white"/>
              <defs>
                <linearGradient id="paint0_linear" x1="0" y1="0" x2="0" y2="16" gradientUnits="userSpaceOnUse">
                  <stop stop-color="#A7E05F"/>
                  <stop offset="1" stop-color="#12AB97"/>
                </linearGradient>
              </defs>
            </svg>
          </view>
        </view>

        <!-- Sign in button -->
        <view class="signin-button" @click="handleSignIn">
          <text class="button-text">SIGN IN</text>
        </view>

        <!-- Sign up link -->
        <view class="signup-link">
          <text class="link-text">Already have an account?</text>
          <text class="link-action" @click="goToSignUp">Sign up</text>
        </view>
      </view>
    </view>

    <!-- Home indicator -->
    <view class="home-indicator">
      <view class="indicator-bar"></view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'SignIn',
  data() {
    return {
      email: 'johndoe@mail.com',
      phone: '+880 111 222 333'
    }
  },
  methods: {
    goBack() {
      uni.navigateBack()
    },
    handleSignIn() {
      // Navigate to main app after sign in
      uni.reLaunch({
        url: '/pages/community/community'
      })
    },
    goToSignUp() {
      // Navigate to sign up page
      uni.navigateTo({
        url: '/pages/auth/signup'
      })
    }
  }
}
</script>

<style scoped>
.signin-page {
  width: 100vw;
  height: 100vh;
  background: #F9F9F9;
  display: flex;
  flex-direction: column;
  overflow: hidden;
}

/* Header styles */
.header {
  background: #fff;
  padding-bottom: 10px;
}

.status-bar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 11px 15px 0;
  height: 30px;
}

.status-time {
  font-family: 'Roboto', -apple-system, sans-serif;
  font-weight: 700;
  font-size: 16px;
  color: #1C2340;
}

.status-icons {
  display: flex;
  align-items: center;
  gap: 5px;
}

.network-signal {
  display: flex;
  align-items: flex-end;
  gap: 1px;
  height: 11px;
}

.signal-bar {
  width: 3px;
  background: #1C2340;
  border-radius: 1.5px;
}

.bar1 { height: 4px; }
.bar2 { height: 6px; }
.bar3 { height: 9px; }
.bar4 { height: 11px; }

.nav-header {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 15px;
  position: relative;
  height: 60px;
}

.back-button {
  position: absolute;
  left: 15px;
  top: 50%;
  transform: translateY(-50%);
  padding: 5px;
  cursor: pointer;
}

.page-title {
  font-family: 'Roboto', -apple-system, sans-serif;
  font-weight: 700;
  font-size: 22px;
  color: #1C2340;
}

/* Content area */
.content-area {
  flex: 1;
  display: flex;
  flex-direction: column;
  overflow-y: auto;
  padding: 0 20px 20px;
}

.illustration-section {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px 0;
}

.signin-illustration {
  width: 100%;
  max-width: 336px;
  height: auto;
}

/* Signup card */
.signup-card {
  background: #fff;
  border-radius: 10px;
  padding: 23px 20px 25px;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.card-header {
  text-align: center;
  margin-bottom: 10px;
}

.card-title {
  font-family: 'Roboto', -apple-system, sans-serif;
  font-weight: 700;
  font-size: 24px;
  color: #1C2340;
  display: block;
  margin-bottom: 4px;
}

.card-subtitle {
  font-family: 'Roboto', -apple-system, sans-serif;
  font-weight: 400;
  font-size: 20px;
  color: #1C2340;
  display: block;
}

/* Input fields */
.input-field {
  background: #F4F5F7;
  border-radius: 25px;
  height: 50px;
  display: flex;
  align-items: center;
  padding: 0 15px;
  gap: 12px;
}

.input-icon {
  flex-shrink: 0;
  display: flex;
  align-items: center;
}

.input-text {
  flex: 1;
  border: none;
  background: transparent;
  font-family: 'Roboto', -apple-system, sans-serif;
  font-weight: 700;
  font-size: 16px;
  color: #242A37;
  outline: none;
}

.phone-field {
  padding: 0 12px 0 8px;
}

.country-selector {
  display: flex;
  align-items: center;
  gap: 8px;
  flex-shrink: 0;
  padding-right: 8px;
  border-right: 1px solid rgba(36, 42, 55, 0.1);
}

.flag-circle {
  width: 26px;
  height: 26px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.phone-text {
  padding-left: 8px;
}

.verified-icon {
  flex-shrink: 0;
  display: flex;
  align-items: center;
}

/* OR divider */
.or-divider {
  display: flex;
  align-items: center;
  gap: 15px;
  padding: 0 5px;
}

.divider-line {
  flex: 1;
  height: 1px;
  background: rgba(36, 42, 55, 0.14);
}

.or-text {
  font-family: 'Roboto', -apple-system, sans-serif;
  font-weight: 700;
  font-size: 16px;
  color: #1C2340;
  flex-shrink: 0;
}

/* Sign in button */
.signin-button {
  background: linear-gradient(180deg, #FE6587 0%, #F52D6A 100%);
  border-radius: 25px;
  height: 50px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  margin-top: 10px;
}

.button-text {
  font-family: 'Roboto', -apple-system, sans-serif;
  font-weight: 500;
  font-size: 16px;
  color: #fff;
  letter-spacing: 0.5px;
}

/* Signup link */
.signup-link {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 8px;
  margin-top: 5px;
}

.link-text {
  font-family: 'Roboto', -apple-system, sans-serif;
  font-weight: 400;
  font-size: 16px;
  color: #1C2340;
}

.link-action {
  font-family: 'Roboto', -apple-system, sans-serif;
  font-weight: 700;
  font-size: 16px;
  color: #F52E6B;
  cursor: pointer;
}

/* Home indicator */
.home-indicator {
  display: flex;
  justify-content: center;
  padding: 20px 0 8px;
  background: #F9F9F9;
}

.indicator-bar {
  width: 134px;
  height: 5px;
  background: #F52E6B;
  border-radius: 2.5px;
}

/* Responsive design */
@media (max-width: 750rpx) {
  .card-title {
    font-size: 22px;
  }
  
  .card-subtitle {
    font-size: 18px;
  }
}

@media (max-width: 600rpx) {
  .card-title {
    font-size: 20px;
  }
  
  .card-subtitle {
    font-size: 16px;
  }
  
  .signup-card {
    padding: 20px 15px;
  }
}

/* Tablet and larger screens */
@media (min-width: 768px) {
  .signin-page {
    max-width: 375px;
    margin: 0 auto;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
  }
}
</style>
