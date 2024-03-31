<script setup lang="ts">
const desserts = [
  {
    date: '2024/03/29',
    contents: '아침활동면제권 1개 환불',
    assets: '5000',
  },
  {
    date: '2024/03/29',
    contents: '아침활동면제권 1개 구매',
    assets: '4950',
  },
  {
    date: '2024/03/29',
    contents: '예금 이자율: 10%',
    assets: '',
  },
]

function sendMoney() {
  alert('돈을 보냅니다!')
}
</script>

<template>
  <VRow>
    <!-- 👉 Lifetime Membership -->
    <VCol
      md="6"
      lg="12"
      cols="12"
    >
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
              <VCardTitle>열심히 모아보아요! 화이팅! 💪</VCardTitle>
            </VCardItem>

            <VCardText>
              <VDivider />
            </VCardText>

            <VCardText class="d-flex justify-center">
              <div class="me-auto pe-4">
                <p class="d-flex align-center mb-6">
                  <VIcon
                    color="primary"
                    icon="ri-currency-line"
                  />
                  <span class="ms-3">현금</span>
                  <span class="ms-3">10,000</span>
                </p>
                <p class="d-flex align-center mb-6">
                  <VIcon
                    color="primary"
                    icon="ri-bank-line"
                  />
                  <span class="ms-3">예금</span>
                  <span class="ms-3">20,000</span>
                </p>
                <p class="d-flex align-center mb-6">
                  <VIcon
                    color="primary"
                    icon="ri-funds-line"
                  />
                  <span class="ms-3">증권</span>
                  <span class="ms-3">30,000</span>
                </p>
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
                내 현재 자산
              </p>
              <p class="mb-5">
                <sup class="text-h1 font-weight-medium">60,000</sup>
              </p>
              <p>
                <a
                  color="error"
                  class="send-money-button"
                  target="_blank"
                  rel="noopener noreferrer"
                  @click=sendMoney
                >
                  송금 하기😎
                </a>
              </p>

            </div>
          </VCol>
        </VRow>
      </VCard>
    </VCol>
  </VRow>
  <VRow>
    <VCol cols="12">
      <VCard title="자산 내역">
        <VTable>
          <thead>
          <tr>
            <th class="text-uppercase text-left">
              날짜
            </th>
            <th class="text-uppercase text-left">
              내용
            </th>
            <th class="text-uppercase text-right">
              자산
            </th>
          </tr>
          </thead>

          <tbody>
          <tr
            v-for="item in desserts"
            :key="item.dessert"
          >
            <td class="text-left">
              {{ item.date }}
            </td>
            <td class="text-left">
              {{ item.contents }}
            </td>
            <td class="text-right">
              {{ item.assets }}
            </td>
          </tr>
          </tbody>
        </VTable>
      </VCard>
    </VCol>
  </VRow>
</template>

<style lang="scss" scoped>
// membership pricing
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
