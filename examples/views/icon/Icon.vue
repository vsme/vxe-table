<template>
  <div>
    <h2>{{ $t('app.aside.nav.icon') }}</h2>
    <p class="tip">内置字体图标，可以通过 <router-link class="link" :to="{name: 'StartIcons'}">setup</router-link> 替换为 font 图标，例如第三方图标库：font-awesome、inconfont</p>

    <ul class="vxe-row icon-list" title="点击复制内容">
      <li class="vxe-col--4" v-for="name in iconList" :key="name">
        <i :class="`${prefixClass}${name}`"></i>
        <div class="title">{{ prefixClass }}{{ name }}</div>
      </li>
    </ul>

    <p class="demo-code">{{ $t('app.body.button.showCode') }}</p>

    <pre>
      <pre-code class="xml">{{ demoCodes[0] }}</pre-code>
    </pre>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  setup () {
    return {
      prefixClass: 'vxe-icon-',
      iconList: ['time', 'feedback', 'lightning', 'cloudy', 'heavy-rain', 'moon', 'sunny', 'location', 'location-fill', 'microphone-fill', 'microphone', 'share', 'share-fill', 'flag', 'flag-fill', 'platform', 'goods-fill', 'goods', 'funnel-clear', 'envelope', 'envelope-open-fill', 'envelope-open', 'envelope-fill', 'message-fill', 'chat', 'chat-fill', 'send', 'send-fill', 'user', 'user-fill', 'wechat', 'alipay', 'indicator', 'file-excel', 'file-pdf', 'file-image', 'file-markdown', 'file-ppt', 'file-word', 'file-zip', 'file-txt', 'refresh', 'checkbox-unchecked', 'information', 'info-circle-fill', 'info-circle', 'chart-radar', 'chart-bar-x', 'repeat', 'voice-fill', 'voice', 'flow-branch', 'comment', 'folder', 'folder-open', 'picture', 'picture-fill', 'bell', 'bell-fill', 'undo', 'home', 'home-fill', 'checkbox-checked', 'checkbox-indeterminate', 'fullscreen', 'minimize', 'print', 'upload', 'download', 'cloud-upload', 'cloud-download', 'spinner', 'close', 'custom-column', 'edit', 'zoom-in', 'caret-down', 'caret-up', 'caret-right', 'caret-left', 'square-checked-fill', 'square-close', 'square-down', 'square-left', 'square-caret-right', 'square-minus', 'square-plus', 'square-right', 'square-up', 'square-checked', 'square-down-fill', 'square-minus-fill', 'square-close-fill', 'square-left-fill', 'square-caret-right-fill', 'square-up-fill', 'square-right-fill', 'square-plus-fill', 'square-plus-square', 'square-fill', 'square-square', 'sort-alpha-desc', 'sort-alpha-asc', 'sort-numeric-asc', 'sort-numeric-desc', 'star-fill', 'star', 'star-half', 'lock-fill', 'unlock-fill', 'question', 'exclamation', 'ellipsis-h', 'ellipsis-v', 'save', 'setting', 'setting-fill', 'link', 'sort', 'chart-pie', 'chart-line', 'swap', 'num-list', 'copy', 'company', 'swap-right', 'swap-left', 'table', 'merge-cells', 'paste', 'cut', 'lock', 'unlock', 'chart-bar-y', 'fixed-left-fill', 'fixed-left', 'fixed-right-fill', 'fixed-right', 'swap-down', 'swap-up', 'square', 'check', 'question-circle-fill', 'error-circle-fill', 'delete', 'dot', 'success-circle', 'delete-fill', 'minus', 'maximize', 'question-circle', 'warning-circle', 'warnion-circle-fill', 'eye-fill', 'search', 'funnel', 'eye-fill-close', 'search-zoom-in', 'arrow-right', 'arrow-left', 'arrow-up', 'calendar', 'arrow-down', 'warning-triangle', 'add', 'arrow-double-left', 'arrow-double-right', 'menu', 'warning-triangle-fill', 'error-circle', 'zoom-out', 'success-circle-fill', 'radio-checked', 'radio-unchecked'],
      demoCodes: [
        `
        <i class="vxe-icon-delete"></i>
        `
      ]
    }
  }
})
</script>

<style lang="scss" scoped>
.icon-list {
  font-size: 26px;
  text-align: center;
  border-top: 1px solid #eee;
  border-left: 1px solid #eee;
  overflow: hidden;
  margin: 0;
  padding: 0;
  &:after {
    content: "";
    clear: both;
  }
  & > li {
    height: 100px;
    border-right: 1px solid #eee;
    border-bottom: 1px solid #eee;
    cursor: pointer;
    padding-top: 10px;
    & > i {
      color: #606266;
      border-color: #606266;
    }
    &:hover {
      & > i {
        color: #5CB6FF;
        border-color: #5CB6FF;
      }
    }
    .title {
      font-size: 14px;
      margin-top: 10px;
    }
  }
}
</style>
