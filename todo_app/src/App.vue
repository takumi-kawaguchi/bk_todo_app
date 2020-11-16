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
    <div>
      <input type="submit" value="追加" @click="addList" />
    </div>
    <ul v-for="(item, i) in lists" :key="i">
      <li>
        id: {{ i }}, title: {{ item.title }}
        <button @click="deleteList(i)">削除</button>
      </li>
    </ul>
    <pre>{{ $data }}</pre>
  </div>
</template>

<script>
export default {
  data: () => ({
    lists: [{ title: "mytodo", body: "content" }],
    title: "",
    body: "",
  }),
  methods: {
    addList: function () {
      if (this.title == "" || this.body === "") return;
      this.lists.push({ title: this.title, body: this.body });
      this.title = "";
      this.body = "";
    },
    deleteList: function (i) {
      this.lists.splice(i, 1);
    },
  },
};
</script>
