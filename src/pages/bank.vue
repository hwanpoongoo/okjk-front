<script setup lang="ts">
import trophy from '@images/misc/trophy.png'
function sendMoney() {
  console.log('돈을 보냈어요!')
}
</script>

<template>
  <VCard>
    <VRow no-gutters>
      <VCol
        cols="12"
        sm="8"
        md="12"
        lg="7"
        order="2"
        order-lg="1"
      >
        <VCardItem>
          <VCardTitle>축하해요! A등급 달성!!! 🎉</VCardTitle>
        </VCardItem>

        <VCardText>
          <VDivider />
        </VCardText>

        <VCardText class="d-flex justify-center">
          <div class="me-auto pe-4">
            <p class="d-flex align-center mb-6">
              <VIcon
                color="primary"
                icon="ri-funds-box-line"
              />
              <span class="ms-3">이자율</span>
              <span class="ms-3">10%</span>
            </p>
            <p class="d-flex align-center mb-6">
              <VIcon
                color="primary"
                icon="ri-calendar-schedule-line"
              />
              <span class="ms-3">예금기간</span>
              <span class="ms-3">5일 </span>
            </p>
            <VImg
              :src="trophy"
              class="trophy"
            />
          </div>
        </VCardText>
      </VCol>

      <VCol
        cols="12"
        sm="4"
        md="12"
        lg="5"
        order="1"
        order-lg="2"
        class="member-pricing-bg text-center"
      >
        <div class="membership-pricing d-flex flex-column align-center py-14 h-100 justify-center">
          <p class="text-sm">
            나의 신용 등급
          </p>
          <p style="font-size: 5rem; color: black">
            A
          </p>

          <p>
            <a
              color="error"
              class="send-money-button"
              target="_blank"
              rel="noopener noreferrer"
              @click="sendMoney"
            >
              예금 하기😎
            </a>
          </p>
        </div>
      </VCol>
    </VRow>
  </VCard>
</template>

<style lang="scss" scoped>
.v-card .trophy {
  position: absolute;
  inline-size: 5.188rem;
  inset-block-end: 1.25rem;
  inset-inline-end: 1.25rem;
}

.member-pricing-bg {
  position: relative;
  background-color: rgba(var(--v-theme-on-surface), var(--v-hover-opacity));
}

.send-money-button,
.button-inner {
  display: inline-flex;
  box-sizing: border-box;
  align-items: center;
  justify-content: center;
  border: 0;
  border-radius: 6px;
  margin: 0;
  animation: anime 12s linear infinite;
  appearance: none;
  background: linear-gradient(-45deg, #ffa63d, #ff3d77, #338aff, #3cf0c5);
  background-size: 600%;
  color: rgba(255, 255, 255, 90%);
  cursor: pointer;
  font-size: 0.9375rem;
  font-weight: 500;
  letter-spacing: 0.43px;
  line-height: 1.2;
  min-inline-size: 50px;
  outline: 0;
  padding-block: 0.625rem;
  padding-inline: 1.25rem;
  text-decoration: none;
  text-transform: none;
  vertical-align: middle;
}

.send-money-button {
  z-index: 999;

  &:hover {
    color: white;
    text-decoration: none;
  }

  &:not(:hover) .button-inner {
    opacity: 0.8;
  }
}

@keyframes anime {
  0% {
    background-position: 0% 50%;
  }

  50% {
    background-position: 100% 50%;
  }

  100% {
    background-position: 0% 50%;
  }
}
</style>
