<script lang="ts" setup>
import type { GlobalThemeOverrides } from 'naive-ui';
import { zhCN, dateZhCN } from 'naive-ui';

// 自定义主题样式
const themeOverrides: GlobalThemeOverrides = {
  // 通用
  common: {
    primaryColor: '#4D96FFFF',
    primaryColorHover: '#90BDFFFF',
    primaryColorPressed: '#608ECFFF',
    primaryColorSuppl: '#90BDFFFF',
    infoColor: '#4D96FFFF',
    infoColorHover: '#90BDFFFF',
    infoColorPressed: '#608ECFFF',
    infoColorSuppl: '#90BDFFFF',
    successColor: '#6BCB77FF',
    successColorPressed: '#73AF7AFF',
    successColorHover: '#A3DFAAFF',
    successColorSuppl: '#A3DFAAFF',
    warningColor: '#FFD93DFF',
    warningColorHover: '#FFE786FF',
    warningColorSuppl: '#FFE786FF',
    warningColorPressed: '#CFB756FF',
    errorColor: '#FF6B6BFF',
    errorColorPressed: '#CF7373FF',
    errorColorHover: '#FFA3A3FF',
    errorColorSuppl: '#FFA3A3FF',
    textColorBase: '#333333FF',
  },
};
</script>

<template>
  <!-- naive-ui提供的配置器 -->
  <n-config-provider
    :theme-overrides="themeOverrides"
    :locale="zhCN"
    :date-locale="dateZhCN"
    :inline-theme-disabled="true"
    :abstract="true"
  >
    <!-- 主页面 -->
    <router-view />
  </n-config-provider>
</template>

<style scoped></style>
