<template>
  <view class="community-container" @click="navigateToSocial">
    <!-- Status Bar -->
    <view class="status-bar">
      <view class="time">9:41</view>
      <view class="status-icons">
        <view class="signal-bars">
          <view class="bar bar-1"></view>
          <view class="bar bar-2"></view>
          <view class="bar bar-3"></view>
          <view class="bar bar-4"></view>
        </view>
        <view class="wifi-icon">
          <svg width="17" height="12" viewBox="0 0 17 12" fill="none">
            <path d="M16.4289 3.27C11.6935 -1.08957 4.40632 -1.08957 -0.329074 3.27C-0.413575 3.34856 -0.462323 3.45822 -0.464022 3.57358C-0.465721 3.68894 -0.420225 3.79999 -0.338074 3.881L0.572926 4.781C0.7376 4.94536 1.00287 4.94978 1.17293 4.791C5.07088 1.23337 11.038 1.23337 14.9359 4.791C15.106 4.94978 15.3713 4.94536 15.5359 4.781L16.4469 3.881C16.5279 3.79878 16.5718 3.68703 16.5684 3.57166C16.565 3.45628 16.5146 3.34731 16.4289 3.27Z" fill="#1C2340"/>
          </svg>
        </view>
        <view class="battery-icon">
          <svg width="22" height="11" viewBox="0 0 22 11" fill="none">
            <path d="M19.892 0H1.98904C1.0623 0 0.311035 0.751266 0.311035 1.678V9.51C0.311035 9.95503 0.487824 10.3818 0.80251 10.6965C1.1172 11.0112 1.544 11.188 1.98904 11.188H19.889C20.8158 11.188 21.567 10.4367 21.567 9.51V8.95H21.847C22.3104 8.95 22.686 8.57437 22.686 8.111V3.077C22.686 2.85448 22.5976 2.64108 22.4403 2.48374C22.283 2.32639 22.0696 2.238 21.847 2.238H21.567V1.678C21.567 0.752436 20.8176 0.00165476 19.892 0Z" fill="#1C2340"/>
          </svg>
        </view>
      </view>
    </view>

    <!-- Main Content -->
    <view class="main-content">
      <!-- Illustration Area -->
      <view class="illustration-container">
        <image 
          class="community-illustration" 
          src="https://cdn.builder.io/api/v1/image/assets%2F03bdf8e0f8b54edba10203afff5ff46f%2F3a7d76c053054c53aa119dddd3148a68?format=webp&width=800"
          mode="aspectFit"
        />
      </view>

      <!-- Content Section -->
      <view class="content-section">
        <!-- Gradient Background -->
        <view class="gradient-background">
          <!-- Main Headline -->
          <view class="headline-container">
            <text class="main-title">Find Community</text>
            <text class="sub-title">Friends</text>
          </view>

          <!-- Description -->
          <view class="description-container">
            <text class="description-line">Find People and opportunities</text>
            <text class="description-line">Everyone and Everywhere</text>
          </view>

          <!-- Pagination Dots -->
          <view class="pagination-dots">
            <view class="dot dot-inactive"></view>
            <view class="dot dot-active"></view>
            <view class="dot dot-inactive"></view>
          </view>
        </view>
      </view>
    </view>

    <!-- Home Indicator -->
    <view class="home-indicator">
      <view class="indicator-bar"></view>
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
    navigateToSocial() {
      // Use direct window navigation for H5 platform
      if (typeof window !== 'undefined') {
        window.location.href = '#/pages/social/social'
      } else {
        // Fallback for other platforms
        try {
          uni.navigateTo({
            url: '/pages/social/social'
          })
        } catch (e) {
          console.log('Navigation error:', e)
        }
      }
    }
  }
}
</script>

<style scoped>
.community-container {
  width: 100vw;
  height: 100vh;
  background: #fff;
  display: flex;
  flex-direction: column;
  position: relative;
  overflow: hidden;
}

.status-bar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20rpx 30rpx 0;
  height: 58rpx;
  z-index: 10;
}

.time {
  font-family: 'Roboto', sans-serif;
  font-weight: 700;
  font-size: 32rpx;
  color: #1c2340;
}

.status-icons {
  display: flex;
  align-items: center;
  gap: 12rpx;
}

.signal-bars {
  display: flex;
  align-items: flex-end;
  gap: 4rpx;
  height: 22rpx;
}

.bar {
  background: #1c2340;
  border-radius: 3rpx;
  width: 6rpx;
}

.bar-1 { height: 8rpx; }
.bar-2 { height: 12rpx; }
.bar-3 { height: 18rpx; }
.bar-4 { height: 22rpx; }

.wifi-icon,
.battery-icon {
  width: 34rpx;
  height: 22rpx;
  display: flex;
  align-items: center;
  justify-content: center;
}

.main-content {
  flex: 1;
  display: flex;
  flex-direction: column;
  position: relative;
}

.illustration-container {
  flex: 1;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #f8f8f8;
  padding: 40rpx 0;
}

.community-illustration {
  width: 100%;
  max-width: 600rpx;
  height: auto;
}

.content-section {
  position: relative;
  height: 710rpx;
  overflow: hidden;
}

.gradient-background {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 710rpx;
  background: linear-gradient(180deg, #FE6587 0%, #F52D6A 100%);
  border-top-left-radius: 40rpx;
  border-top-right-radius: 40rpx;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 60rpx 40rpx 120rpx;
  color: white;
}

.headline-container {
  text-align: center;
  margin-bottom: 40rpx;
}

.main-title {
  display: block;
  font-family: 'Roboto', sans-serif;
  font-weight: 700;
  font-size: 56rpx;
  line-height: 66rpx;
  color: white;
  margin-bottom: 8rpx;
}

.sub-title {
  display: block;
  font-family: 'Roboto', sans-serif;
  font-weight: 700;
  font-size: 56rpx;
  line-height: 66rpx;
  color: white;
  text-align: center;
}

.description-container {
  text-align: center;
  margin-bottom: 80rpx;
}

.description-line {
  display: block;
  font-family: 'Roboto', sans-serif;
  font-weight: 400;
  font-size: 26rpx;
  line-height: 30rpx;
  color: white;
  margin-bottom: 6rpx;
}

.pagination-dots {
  display: flex;
  gap: 20rpx;
  align-items: center;
}

.dot {
  width: 30rpx;
  height: 30rpx;
  border-radius: 50%;
  transition: all 0.3s ease;
}

.dot-active {
  background: white;
}

.dot-inactive {
  background: rgba(255, 255, 255, 0.2);
}

.home-indicator {
  position: absolute;
  bottom: 40rpx;
  left: 50%;
  transform: translateX(-50%);
  z-index: 10;
}

.indicator-bar {
  width: 268rpx;
  height: 10rpx;
  background: white;
  border-radius: 5rpx;
}

/* Responsive adjustments */
@media (max-width: 750rpx) {
  .main-title,
  .sub-title {
    font-size: 48rpx;
    line-height: 56rpx;
  }
  
  .description-line {
    font-size: 24rpx;
  }
  
  .content-section {
    height: 650rpx;
  }
  
  .gradient-background {
    height: 650rpx;
    padding: 50rpx 30rpx 100rpx;
  }
}

@media (max-width: 600rpx) {
  .main-title,
  .sub-title {
    font-size: 42rpx;
    line-height: 48rpx;
  }
  
  .description-line {
    font-size: 22rpx;
  }
  
  .content-section {
    height: 600rpx;
  }
  
  .gradient-background {
    height: 600rpx;
    padding: 40rpx 20rpx 80rpx;
  }
}
</style>
