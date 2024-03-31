<script setup lang="ts">
import { useTheme } from 'vuetify'
import AuthProvider from '@/views/pages/authentication/AuthProvider.vue'
import logo from '@images/logo.svg?raw'
import authV1MaskDark from '@images/pages/auth-v1-mask-dark.png'
import authV1MaskLight from '@images/pages/auth-v1-mask-light.png'
// import authV1Tree2 from '@images/pages/auth-v1-tree-2.png'
// import authV1Tree from '@images/pages/auth-v1-tree.png'

const form = ref({
  email: '',
  password: '',
  remember: false,
})

const vuetifyTheme = useTheme()

const authThemeMask = computed(() => {
  return vuetifyTheme.global.name.value === 'light'
    ? authV1MaskLight
    : authV1MaskDark
})

const isPasswordVisible = ref(false)
</script>

<template>
  <!-- eslint-disable vue/no-v-html -->

  <div class="auth-wrapper d-flex align-center justify-center pa-4">
    <VCard
      class="auth-card pa-4 pt-7"
      max-width="448"
    >
      <VCardItem class="justify-center">
        <template #prepend>
          <div class="d-flex">
            <div v-html="logo" />
          </div>
        </template>

        <VCardTitle class="font-weight-semibold text-2xl text-uppercase">
          옹기종기
        </VCardTitle>
      </VCardItem>

      <VCardText class="pt-2">
        <h5 class="text-h5 font-weight-semibold mb-1">
          환영해요! 👋🏻
        </h5>
        <p class="mb-0">
          계정에 로그인하여 시작해주세요 :D
        </p>
      </VCardText>

      <VCardText>
        <VForm @submit.prevent="() => {}">
          <VRow>
            <!-- email -->
            <VCol cols="12">
              <VTextField
                v-model="form.email"
                label="이메일"
                type="email"
              />
            </VCol>

            <!-- password -->
            <VCol cols="12">
              <VTextField
                v-model="form.password"
                label="비밀번호"
                placeholder="············"
                :type="isPasswordVisible ? 'text' : 'password'"
                :append-inner-icon="isPasswordVisible ? 'ri-eye-off-line' : 'ri-eye-line'"
                @click:append-inner="isPasswordVisible = !isPasswordVisible"
              />

              <!-- remember me checkbox -->
              <div class="d-flex align-center justify-space-between flex-wrap mt-1 mb-4">
                <VCheckbox
                  v-model="form.remember"
                  label="계정 기억하기"
                />

                <a
                  class="ms-2 mb-1"
                  href="javascript:void(0)"
                >
                  비밀번호를 잊어버렸나요?
                </a>
              </div>

              <!-- login button -->
              <VBtn
                block
                type="submit"
                to="/my-assets"
              >
                로그인
              </VBtn>
            </VCol>

            <!-- create account -->
            <VCol
              cols="12"
              class="text-center text-base"
            >
              <span>처음 이신가요?</span>
              <RouterLink
                class="text-primary ms-2"
                to="/register"
              >
                계정 만들기
              </RouterLink>
            </VCol>

            <VCol
              cols="12"
              class="d-flex align-center"
            >
              <VDivider />
              <span class="mx-4">or</span>
              <VDivider />
            </VCol>

            <!-- auth providers -->
            <VCol
              cols="12"
              class="text-center"
            >
              <AuthProvider />
            </VCol>
          </VRow>
        </VForm>
      </VCardText>
    </VCard>

<!--    <VImg-->
<!--      class="auth-footer-start-tree d-none d-md-block"-->
<!--      :src="authV1Tree"-->
<!--      :width="250"-->
<!--    />-->

<!--    <VImg-->
<!--      :src="authV1Tree2"-->
<!--      class="auth-footer-end-tree d-none d-md-block"-->
<!--      :width="350"-->
<!--    />-->

<!--    &lt;!&ndash; bg img &ndash;&gt;-->
<!--    <VImg-->
<!--      class="auth-footer-mask d-none d-md-block"-->
<!--      :src="authThemeMask"-->
<!--    />-->
  </div>
</template>

<style lang="scss">
@use "@core/scss/pages/page-auth.scss";
</style>
