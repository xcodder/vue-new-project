<template lang="html">
  <div class="msg">
    <span class='chat-title'>{{title}}</span>
    <p class='chat-content'>{{content}}</p>
  </div>
</template>

<script>
export default {
  props: {
    title: {},
    content: {}
  }
}
</script>

<style lang="css" scoped>
.msg {
  padding: 6px 7px;
  background: #fbfbfb;
  margin-bottom: 12px;
  border: 1px solid #e8e8e8;
  display: flex;
  flex-direction: column;
}
.chat-title {
  font-weight: bold;
  margin-bottom: 4px;
}

.chat-content {
  white-space: pre-wrap;
}
</style>
