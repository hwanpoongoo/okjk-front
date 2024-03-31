<script setup lang="ts">
const myItem = [
  {
    id: '1',
    contents: '급식 1등으로 먹기',
    price: 20,
    inventoryCount: 3,
  },
  {
    id: '1',
    contents: '나들이 쿠폰',
    price: 20,
    inventoryCount: 5,
  },
]
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
      </VCard>
    </VCol>
  </VRow>
  <VRow>
    <VCol cols="12">
      <VCard title="내 아이템">
        <VTable>
          <thead>
          <tr>
            <th class="text-uppercase text-left">
              아이템 이름
            </th>
            <th class="text-uppercase text-left">
              보유 수량
            </th>
          </tr>
          </thead>

          <tbody>
          <tr
            v-for="item in myItem"
            :key="item.id"
          >
            <td class="text-left">
              {{ item.contents }}
            </td>
            <td class="text-left">
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
