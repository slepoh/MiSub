<script setup>
import { useI18n } from '../../i18n/index.js';

const { t } = useI18n();

defineProps({
  href: {
    type: String,
    default: 'https://web.yormb.cn'
  },
  className: {
    type: [String, Array, Object],
    default: ''
  }
});
</script>

<template>
  <a
    :href="href"
    target="_blank"
    rel="noopener noreferrer"
    :class="className"
    title="查看主页"
    :aria-label="t('nav.githubRepo')"
  >
    <svg class="h-5 w-5" viewBox="0 0 1024 1024" xmlns="http://www.w3.org/2000/svg" width="20" height="20">
      <path d="M1024 590.4384l-512-397.43488-512 397.43488 0-162.03776 512-397.43488 512 397.43488zM896 576l0 384-256 0 0-256-256 0 0 256-256 0 0-384 384-288.01024z" p-id="5127" fill="#8a8a8a"></path>
    </svg>
  </a>
</template>
