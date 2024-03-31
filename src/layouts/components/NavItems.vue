<script lang="ts" setup>
import VerticalNavSectionTitle from '@/@layouts/components/VerticalNavSectionTitle.vue'
import VerticalNavGroup from '@layouts/components/VerticalNavGroup.vue'
import VerticalNavLink from '@layouts/components/VerticalNavLink.vue'
</script>

<template>
  <!-- 👉 Dashboards -->
  <VerticalNavGroup
    :item="{
      title: 'Dashboards',
      badgeContent: '5',
      badgeClass: 'bg-error',
      icon: 'ri-home-smile-line',
    }"
  >
    <VerticalNavLink
      :item="{
        title: 'Analytics',
        to: '/dashboard',
      }"
    />
  </VerticalNavGroup>

  <!-- 옹기종기 알파 -->
  <VerticalNavSectionTitle
    :item="{
      heading: '옹기종기 알파',
    }"
  />
  <VerticalNavLink
    :item="{
      title: '내 자산',
      icon: 'ri-user-line',
      to: '/my-assets',
    }"
  />

  <VerticalNavLink
    :item="{
      title: '내 아이템',
      icon: 'ri-shopping-bag-line',
      to: '/my-items',
    }"
  />
  <VerticalNavLink
    :item="{
      title: '아이템 상점',
      icon: 'ri-shopping-cart-2-line',
      to: '/item-shop',
    }"
  />
  <VerticalNavLink
    :item="{
      title: '은행',
      icon: 'ri-money-dollar-circle-line',
      to: '/bank',
    }"
  />
  <VerticalNavLink
    :item="{
      title: '증권 거래소',
      icon: 'ri-p2p-line',
      to: '/stock-exchange',
    }"
  />

<!--  &lt;!&ndash; 👉 Apps & Pages &ndash;&gt;-->
<!--  <VerticalNavSectionTitle-->
<!--    :item="{-->
<!--      heading: 'Apps & Pages',-->
<!--    }"-->
<!--  />-->
<!--  <VerticalNavLink-->
<!--    :item="{-->
<!--      title: 'Account Settings',-->
<!--      icon: 'ri-user-settings-line',-->
<!--      to: '/account-settings',-->
<!--    }"-->
<!--  />-->

<!--  <VerticalNavLink-->
<!--    :item="{-->
<!--      title: 'Login',-->
<!--      icon: 'ri-login-box-line',-->
<!--      to: '/login',-->
<!--    }"-->
<!--  />-->
<!--  <VerticalNavLink-->
<!--    :item="{-->
<!--      title: 'Register',-->
<!--      icon: 'ri-user-add-line',-->
<!--      to: '/register',-->
<!--    }"-->
<!--  />-->
<!--  <VerticalNavLink-->
<!--    :item="{-->
<!--      title: 'Error',-->
<!--      icon: 'ri-information-line',-->
<!--      to: '/no-existence',-->
<!--    }"-->
<!--  />-->

<!--  &lt;!&ndash; 👉 User Interface &ndash;&gt;-->
<!--  <VerticalNavSectionTitle-->
<!--    :item="{-->
<!--      heading: 'User Interface',-->
<!--    }"-->
<!--  />-->
<!--  <VerticalNavLink-->
<!--    :item="{-->
<!--      title: 'Typography',-->
<!--      icon: 'ri-text',-->
<!--      to: '/typography',-->
<!--    }"-->
<!--  />-->
<!--  <VerticalNavLink-->
<!--    :item="{-->
<!--      title: 'Icons',-->
<!--      icon: 'ri-remixicon-line',-->
<!--      to: '/icons',-->
<!--    }"-->
<!--  />-->
<!--  <VerticalNavLink-->
<!--    :item="{-->
<!--      title: 'Cards',-->
<!--      icon: 'ri-bar-chart-box-line',-->
<!--      to: '/cards',-->
<!--    }"-->
<!--  />-->

<!--  &lt;!&ndash; 👉 Forms & Tables &ndash;&gt;-->
<!--  <VerticalNavSectionTitle-->
<!--    :item="{-->
<!--      heading: 'Forms & Tables',-->
<!--    }"-->
<!--  />-->
<!--  <VerticalNavLink-->
<!--    :item="{-->
<!--      title: 'Form Layouts',-->
<!--      icon: 'ri-layout-4-line',-->
<!--      to: '/form-layouts',-->
<!--    }"-->
<!--  />-->
<!--  <VerticalNavLink-->
<!--    :item="{-->
<!--      title: 'Tables',-->
<!--      icon: 'ri-table-alt-line',-->
<!--      to: '/tables',-->
<!--    }"-->
<!--  />-->
</template>
