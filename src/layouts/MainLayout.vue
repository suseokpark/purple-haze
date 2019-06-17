<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          @click="leftDrawerOpen = !leftDrawerOpen"
          aria-label="Menu"
        >
          <q-icon name="menu" />
        </q-btn>

        <q-toolbar-title>
            {{ mainTitle }}
        </q-toolbar-title>

        <div class="todo">로그인 정보 입력 예정</div>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      bordered
      content-class="bg-grey-2"
    >
      <q-list>
        <q-item-label header>업무링크</q-item-label>
        <q-item clickable to="/">
          <q-item-section avatar>
            <q-icon name="home" />
          </q-item-section>
          <q-item-section>
            <q-item-label>홈</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable to="/coupon">
          <q-item-section avatar>
            <q-icon name="redeem" />
          </q-item-section>
          <q-item-section>
            <q-item-label>쿠폰</q-item-label>
            <q-item-label caption>쿠폰 관리자</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable to="/coupon-list">
          <q-item-section avatar>
            <q-icon name="list" />
          </q-item-section>
          <q-item-section>
            <q-item-label>쿠폰리스트</q-item-label>
            <q-item-label caption>발급된 쿠폰 조회</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { openURL } from 'quasar';

export default {
  name: 'MainLayout',
  data() {
    return {
      mainTitle: 'Kurly CMS',
      leftDrawerOpen: this.$q.platform.is.desktop,
    };
  },
  methods: {
    openURL,
  },
};
</script>

<style>
.todo {
  font-weight: bold;
  background :skyblue;
  color: black;
}
</style>
