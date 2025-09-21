<template>
  <view class="onboarding-step3">
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

    <!-- Main content -->
    <view class="main-content">
      <!-- Illustration area -->
      <view class="illustration-container">
        <image 
          src="https://cdn.builder.io/api/v1/image/assets%2F03bdf8e0f8b54edba10203afff5ff46f%2Fd3c715c2bc4f4246a7d3bfb4b093a637?format=webp&width=800" 
          class="communication-illustration"
          mode="aspectFit"
        />
      </view>

      <!-- Content section with gradient background -->
      <view class="content-section">
        <view class="text-content">
          <view class="main-title">Like Comment and</view>
          <view class="main-title">Share</view>
          <view class="subtitle-container">
            <view class="subtitle-line">A simple way to text, video chat and plan</view>
            <view class="subtitle-line">things all in one place.</view>
          </view>
        </view>

        <!-- Page indicators -->
        <view class="page-indicators">
          <view class="indicator"></view>
          <view class="indicator"></view>
          <view class="indicator active"></view>
        </view>

        <!-- Home indicator -->
        <view class="home-indicator">
          <view class="home-bar"></view>
        </view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'OnboardingStep3',
  data() {
    return {}
  },
  methods: {
    goToApp() {
      // Navigate to main app (community page or main index)
      uni.redirectTo({
        url: '/pages/community/community'
      })
    }
  },
  mounted() {
    // Auto-advance after 4 seconds to complete onboarding
    setTimeout(() => {
      this.goToApp()
    }, 4000)
  }
}
</script>

<style scoped>
.onboarding-step3 {
  width: 100vw;
  height: 100vh;
  background: #fff;
  display: flex;
  flex-direction: column;
  overflow: hidden;
}

/* Status bar styles */
.status-bar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 15px;
  height: 44px;
  background: transparent;
  position: relative;
  z-index: 10;
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

/* Main content */
.main-content {
  flex: 1;
  display: flex;
  flex-direction: column;
}

.illustration-container {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
  background: #fff;
  min-height: 400px;
}

.communication-illustration {
  width: 100%;
  max-width: 320px;
  height: auto;
}

/* Content section with gradient */
.content-section {
  background: linear-gradient(180deg, #FE6587 0%, #F52D6A 100%);
  border-top-left-radius: 20px;
  border-top-right-radius: 20px;
  padding: 40px 20px 30px;
  display: flex;
  flex-direction: column;
  align-items: center;
  min-height: 355px;
  position: relative;
}

.text-content {
  text-align: center;
  margin-bottom: 40px;
}

.main-title {
  font-family: 'Roboto', -apple-system, sans-serif;
  font-weight: 700;
  font-size: 28px;
  color: #fff;
  line-height: 1.2;
  margin-bottom: 2px;
}

.subtitle-container {
  margin-top: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 3px;
}

.subtitle-line {
  font-family: 'Roboto', -apple-system, sans-serif;
  font-weight: 400;
  font-size: 13px;
  color: #fff;
  line-height: normal;
}

/* Page indicators */
.page-indicators {
  display: flex;
  gap: 12px;
  margin-top: auto;
  margin-bottom: 40px;
}

.indicator {
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background: rgba(255, 255, 255, 0.3);
  transition: all 0.3s ease;
}

.indicator.active {
  background: #fff;
}

/* Home indicator */
.home-indicator {
  display: flex;
  justify-content: center;
  padding-bottom: 8px;
}

.home-bar {
  width: 134px;
  height: 5px;
  background: #fff;
  border-radius: 2.5px;
}

/* Responsive design */
@media (max-width: 750rpx) {
  .main-title {
    font-size: 24px;
  }
  
  .subtitle-line {
    font-size: 12px;
  }
  
  .content-section {
    padding: 35px 15px 25px;
  }
  
  .illustration-container {
    min-height: 350px;
  }
}

@media (max-width: 600rpx) {
  .main-title {
    font-size: 22px;
  }
  
  .subtitle-line {
    font-size: 11px;
  }
  
  .content-section {
    padding: 30px 15px 20px;
  }
  
  .illustration-container {
    padding: 15px;
    min-height: 320px;
  }
}

/* Tablet and larger screens */
@media (min-width: 768px) {
  .onboarding-step3 {
    max-width: 375px;
    margin: 0 auto;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
  }
}
</style>
