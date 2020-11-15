<template>
  <div id="app">
    <h1>MyTodoApp</h1>
    <div>
      <label for="title">タイトル：</label>
      <input type="text" v-model="title" placeholder="タイトル" />
    </div>
    <div>
      <label for="body">内容：</label>
      <textarea v-model="body" placeholder="内容"></textarea>
    </div>
    <pre>{{ $data }}</pre>
  </div>
</template>

<script>
export default {
  data: () => ({
    title: "",
    body: "",
  }),
};
</script>
