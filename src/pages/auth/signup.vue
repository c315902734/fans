<template>
  <view class="signup-page">
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
        <text class="page-title">Sign up</text>
      </view>
    </view>

    <!-- Main Content -->
    <view class="content-area">
      <!-- Signup card -->
      <view class="signup-card">
        <!-- Profile photo upload -->
        <view class="profile-photo-section" @click="uploadPhoto">
          <view class="photo-circle">
            <svg width="99" height="99" viewBox="0 0 99 99" fill="none" xmlns="http://www.w3.org/2000/svg">
              <circle opacity="0.28" cx="49.5" cy="49.5" r="49.5" fill="#D6D6D6"/>
              <path fill-rule="evenodd" clip-rule="evenodd" d="M68 62.125C67.9994 63.9887 66.4887 65.4994 64.625 65.5H35.375C33.5113 65.4994 32.0006 63.9887 32 62.125V41.875C32.0006 40.0113 33.5113 38.5006 35.375 38.5H41.563L42.428 36.187C42.9212 34.8714 44.179 33.9998 45.584 34H54.408C55.8134 33.9994 57.0716 34.871 57.565 36.187L58.437 38.5H64.625C66.4887 38.5006 67.9994 40.0113 68 41.875V62.125ZM58.438 52C58.438 47.3398 54.6602 43.562 50 43.562C45.3398 43.562 41.562 47.3398 41.562 52C41.562 56.6602 45.3398 60.438 50 60.438C54.6588 60.4347 58.4347 56.6588 58.438 52ZM52.3687 57.7177C54.681 56.7596 56.1884 54.5029 56.188 52C56.1808 48.5856 53.4144 45.8196 50 45.813C47.4971 45.813 45.2407 47.3208 44.2829 49.6332C43.3252 51.9456 43.8548 54.6073 45.6248 56.3769C47.3947 58.1466 50.0565 58.6758 52.3687 57.7177Z" fill="#4A4A4A"/>
            </svg>
          </view>
        </view>

        <!-- Form fields -->
        <view class="form-fields">
          <!-- Full Name -->
          <view class="input-field">
            <input 
              class="input-text" 
              type="text" 
              v-model="fullName"
              placeholder="Full Name"
            />
          </view>

          <!-- Phone Number -->
          <view class="input-field">
            <input 
              class="input-text" 
              type="tel" 
              v-model="phoneNumber"
              placeholder="Phone Number"
            />
          </view>

          <!-- Email -->
          <view class="input-field">
            <input 
              class="input-text" 
              type="email" 
              v-model="email"
              placeholder="Email"
            />
          </view>

          <!-- Password -->
          <view class="input-field">
            <input 
              class="input-text" 
              type="password" 
              v-model="password"
              placeholder="Password"
            />
          </view>

          <!-- Confirm Password -->
          <view class="input-field">
            <input 
              class="input-text" 
              type="password" 
              v-model="confirmPassword"
              placeholder="Confirm Password"
            />
          </view>
        </view>

        <!-- Terms agreement -->
        <view class="terms-section">
          <view class="checkbox-container" @click="toggleTerms">
            <view class="checkbox" :class="{ checked: agreeToTerms }">
              <svg v-if="agreeToTerms" width="7" height="5" viewBox="0 0 7 5" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M4.83101 0.324025C5.13449 -0.0304828 5.65435 -0.103769 6.04401 0.153025C6.22538 0.265484 6.34982 0.450324 6.38577 0.660681C6.42172 0.871038 6.36574 1.08671 6.23201 1.25303L3.54501 4.60003C3.4003 4.77326 3.19141 4.88025 2.96627 4.89647C2.74112 4.91269 2.51906 4.83673 2.35101 4.68603L0.254011 2.77103C0.0926239 2.6303 0 2.42665 0 2.21253C0 1.9984 0.0926239 1.79475 0.254011 1.65403C0.605155 1.34536 1.13087 1.34536 1.48201 1.65403L2.80001 2.85303L4.83101 0.324025Z" fill="white"/>
              </svg>
            </view>
          </view>
          <view class="terms-text">
            <text class="terms-line">By creating an account you agree to</text>
            <text class="terms-line">our Terms of Service and Privacy Policy</text>
          </view>
        </view>

        <!-- Sign up button -->
        <view class="signup-button" @click="handleSignUp">
          <text class="button-text">Sign up</text>
        </view>
      </view>

      <!-- Sign in link -->
      <view class="signin-link">
        <text class="link-text">Already have an account?</text>
        <text class="link-action" @click="goToSignIn">Sign In</text>
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
  name: 'SignUp',
  data() {
    return {
      fullName: '',
      phoneNumber: '',
      email: '',
      password: '',
      confirmPassword: '',
      agreeToTerms: true
    }
  },
  methods: {
    goBack() {
      uni.navigateBack()
    },
    uploadPhoto() {
      // Handle photo upload
      uni.chooseImage({
        count: 1,
        sizeType: ['compressed'],
        sourceType: ['album', 'camera'],
        success: (res) => {
          console.log('Photo selected:', res.tempFilePaths)
          // Handle photo upload logic here
        }
      })
    },
    toggleTerms() {
      this.agreeToTerms = !this.agreeToTerms
    },
    handleSignUp() {
      if (!this.agreeToTerms) {
        uni.showToast({
          title: 'Please accept terms',
          icon: 'none'
        })
        return
      }
      
      if (this.password !== this.confirmPassword) {
        uni.showToast({
          title: 'Passwords do not match',
          icon: 'none'
        })
        return
      }

      // Navigate to main app after sign up
      uni.reLaunch({
        url: '/pages/community/community'
      })
    },
    goToSignIn() {
      uni.navigateTo({
        url: '/pages/auth/signin'
      })
    }
  }
}
</script>

<style scoped>
.signup-page {
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
  padding: 20px;
}

/* Signup card */
.signup-card {
  background: #fff;
  border-radius: 10px;
  padding: 25px 20px;
  display: flex;
  flex-direction: column;
  gap: 15px;
  margin-bottom: 15px;
}

/* Profile photo section */
.profile-photo-section {
  display: flex;
  justify-content: center;
  margin-bottom: 5px;
  cursor: pointer;
}

.photo-circle {
  width: 99px;
  height: 99px;
  display: flex;
  align-items: center;
  justify-content: center;
}

/* Form fields */
.form-fields {
  display: flex;
  flex-direction: column;
  gap: 13px;
}

.input-field {
  background: #F3F3F3;
  border-radius: 25px;
  height: 50px;
  display: flex;
  align-items: center;
  padding: 0 20px;
}

.input-text {
  flex: 1;
  border: none;
  background: transparent;
  font-family: 'Roboto', -apple-system, sans-serif;
  font-weight: 400;
  font-size: 16px;
  color: #1B242D;
  outline: none;
}

.input-text::placeholder {
  color: #1B242D;
  opacity: 1;
}

/* Terms section */
.terms-section {
  display: flex;
  align-items: flex-start;
  gap: 12px;
  margin-top: 3px;
}

.checkbox-container {
  flex-shrink: 0;
  cursor: pointer;
  padding-top: 2px;
}

.checkbox {
  width: 16px;
  height: 16px;
  border-radius: 3px;
  background: linear-gradient(180deg, #FE6587 0%, #F52D6A 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.2s ease;
}

.checkbox:not(.checked) {
  background: #E0E0E0;
}

.terms-text {
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 5px;
}

.terms-line {
  font-family: 'Roboto', -apple-system, sans-serif;
  font-weight: 400;
  font-size: 16px;
  color: #1B242D;
  line-height: 1.2;
  display: block;
}

/* Sign up button */
.signup-button {
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
  font-weight: 700;
  font-size: 16px;
  color: #fff;
}

/* Signin link */
.signin-link {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 6px;
  padding: 10px 0;
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
  .signup-card {
    padding: 20px 15px;
  }
  
  .terms-line {
    font-size: 15px;
  }
}

@media (max-width: 600rpx) {
  .signup-card {
    padding: 18px 15px;
    gap: 12px;
  }
  
  .form-fields {
    gap: 11px;
  }
  
  .terms-line {
    font-size: 14px;
  }
}

/* Tablet and larger screens */
@media (min-width: 768px) {
  .signup-page {
    max-width: 375px;
    margin: 0 auto;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
  }
}
</style>
