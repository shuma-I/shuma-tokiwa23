<script lang="ts" setup>
import{ref} from 'vue'
const showMenu = ref(false)
const toggleMenu = () =>{
  console.log('clicked')
  showMenu.value = !showMenu.value
}
</script>

<template>
  <div class="navigation-menu-base">
    <div class="navigation-menu-button-title">
      <button @click="toggleMenu">MENU</button>
    </div>
    <div v-show="showMenu">
      <nav class="navigation-menu">
        <ul class="nav-list">
          <li>
            <NuxtLink to="/" @click="close">トップ</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/" @click="close">常盤祭紹介</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/" @click="close">学内マップ＆パンフレット</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/" @click="close">ご協賛企業・個人一覧</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/" @click="close">企画一覧</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/" @click="close">タイムテーブル</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/" @click="close">本部企画一覧</NuxtLink>
          </li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<style scoped lang="scss">
.navigation-menu-base {
  font-family: "Noto Sans JP", sans-serif;
  font-weight: 700;
  width: 90vw;
  height: 90px;
  margin: 0 auto;
  background-color: #DA8080;
  opacity: 1;
  outline: 1px solid #DA8080;
  outline-offset: -1px;
  border-radius: 20px;
}

.navigation-menu-button-title {
  z-index: 10;
  width: 90%;
  padding-left: 30px;
  height: 90px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  color: #ffffff;
}
</style>
