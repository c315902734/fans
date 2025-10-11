<template>
  <view class="onboarding-container" @click="navigateToNextStep">
    <view class="content-wrapper">
      <view class="logo-container">
        <view class="logo-circle">
          <view class="family-icon">
            <!-- Family icon SVG -->
            <svg width="120" height="120" viewBox="0 0 120 120" fill="none" xmlns="http://www.w3.org/2000/svg">
              <g stroke="#FF6B9D" stroke-width="3" fill="none" stroke-linecap="round" stroke-linejoin="round">
                <!-- Man (left) -->
                <circle cx="35" cy="35" r="8"/>
                <path d="M25 75 V65 C25 58 30 53 35 53 C40 53 45 58 45 65 V75"/>
                <path d="M35 45 V53"/>

                <!-- Woman (right) -->
                <circle cx="85" cy="35" r="8"/>
                <path d="M75 75 V65 C75 58 80 53 85 53 C90 53 95 58 95 65 V75"/>
                <path d="M85 45 V53"/>
                <path d="M80 45 L90 45"/>

                <!-- Child (center bottom) -->
                <circle cx="60" cy="55" r="6"/>
                <path d="M52 85 V78 C52 73 56 69 60 69 C64 69 68 73 68 78 V85"/>
                <path d="M60 63 V69"/>
              </g>
            </svg>
          </view>
          <text class="app-name">poxy</text>
        </view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {}
  },
  onLoad() {},
  methods: {
    navigateToNextStep() {
      // Navigate to second onboarding step
      try {
        uni.navigateTo({
          url: '/pages/onboarding/onboarding-step2'
        })
      } catch (e) {
        console.log('Navigation error:', e)
        // Fallback to community if step 2 fails
        uni.navigateTo({
          url: '/pages/community/community'
        })
      }
    }
  }
}
</script>

<style scoped>
.onboarding-container {
  width: 100vw;
  height: 100vh;
  background: linear-gradient(135deg, #ff6b9d 0%, #ff8a9b 100%);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.content-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
}

.logo-container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.logo-circle {
  width: 280rpx;
  height: 280rpx;
  background: white;
  border-radius: 50%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  box-shadow: 0 8rpx 32rpx rgba(0, 0, 0, 0.1);
}

.family-icon {
  margin-bottom: 16rpx;
}

.app-name {
  font-size: 48rpx;
  font-weight: bold;
  color: #ff6b9d;
  letter-spacing: 2rpx;
}

/* Responsive adjustments */
@media (max-width: 750rpx) {
  .logo-circle {
    width: 240rpx;
    height: 240rpx;
  }
  
  .app-name {
    font-size: 40rpx;
  }
}

@media (max-width: 600rpx) {
  .logo-circle {
    width: 200rpx;
    height: 200rpx;
  }
  
  .app-name {
    font-size: 36rpx;
  }
}
</style>
