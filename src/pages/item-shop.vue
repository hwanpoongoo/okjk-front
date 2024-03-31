<script setup lang="ts">
const workHardCoupons = [
  {
    id: '1',
    contents: '급식 1등으로 먹기',
    price: 20,
    inventoryCount: 0,
  },
  {
    id: '2',
    contents: '선생님 물건 빌리기',
    price: 20,
    inventoryCount: 0,
  },
  {
    id: '3',
    contents: '보드게임 이용권',
    price: 30,
    inventoryCount: 0,
  },
  {
    id: '4',
    contents: '칠판 낙서 쿠폰',
    price: 40,
    inventoryCount: 0,
  },
]

const ourClassCoupons = [
  {
    id: '1',
    contents: '나들이 쿠폰',
    price: 20,
    inventoryCount: 0,
  },
  {
    id: '2',
    contents: 'VR체험실 가기',
    price: 20,
    inventoryCount: 0,
  },
  {
    id: '3',
    contents: '컴퓨터실 이용',
    price: 30,
    inventoryCount: 0,
  },
  {
    id: '4',
    contents: '체육 자유시간',
    price: 40,
    inventoryCount: 0,
  },
]
</script>

<template>
  <VRow>
    <!-- 👉 열심이 쿠폰 -->
    <VCol
      md="6"
      lg="12"
      cols="12"
    >
      <VCard title="열심이 쿠폰">
        <VTable density="compact">
          <thead>
          <tr>
            <th class="text-uppercase">
              쿠폰 이름
            </th>
            <th class="text-uppercase text-center">
              가격
            </th>
            <th class="text-uppercase text-center">
              내 수량
            </th>
          </tr>
          </thead>

          <tbody>
          <tr
            v-for="item in workHardCoupons"
            :key="item.id"
          >
            <td>
              {{ item.contents }}
            </td>
            <td class="text-center">
              {{ item.price }}
            </td>
            <td class="text-center">
              {{ item.inventoryCount }}
            </td>
          </tr>
          </tbody>
        </VTable>
      </VCard>
    </VCol>
  </VRow>
  <VRow>
    <!-- 👉 우리반 쿠폰 -->
    <VCol
      md="6"
      lg="12"
      cols="12"
    >
      <VCard title="우리반 쿠폰">
        <VTable density="compact">
          <thead>
          <tr>
            <th class="text-uppercase">
              쿠폰 이름
            </th>
            <th class="text-uppercase text-center">
              가격
            </th>
            <th class="text-uppercase text-center">
              내 수량
            </th>
          </tr>
          </thead>

          <tbody>
          <tr
            v-for="item in ourClassCoupons"
            :key="item.id"
          >
            <td>
              {{ item.contents }}
            </td>
            <td class="text-center">
              {{ item.price }}
            </td>
            <td class="text-center">
              {{ item.inventoryCount }}
            </td>
          </tr>
          </tbody>
        </VTable>
      </VCard>
    </VCol>
  </VRow>
</template>

<style lang="scss" scoped>

</style>
