<template>
  <div id="app">
    <!-- <h1>MyTodoApp</h1>
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
    <draggable>
      <ul v-for="(item, i) in lists" :key="i">
        <li>
          id: {{ i }}, title: {{ item.title }}
          <button @click="deleteList(i)">削除</button>
        </li>
      </ul>
    </draggable>
    <pre>{{ $data }}</pre> -->
    <draggable tag="ul">
      <li v-for="item in items" :key="item.no">{{ item.name }}</li>
    </draggable>
  </div>
</template>

<script>
import draggable from "vuedraggable";
export default {
  components: {
    draggable: draggable,
  },
  data() {
    return {
      items: [
        { no: 1, name: "キャベツ", categoryNo: "1" },
        { no: 2, name: "ステーキ", categoryNo: "2" },
        { no: 3, name: "リンゴ", categoryNo: "3" },
      ],
    };
  },
};
// export default {
//   name: "Draggable",
//   components: { draggable },
//   data: () => ({
//     lists: [{ title: "mytodo", body: "content" }],
//     title: "",
//     body: "",
//     options: {
//       animation: 200,
//     },
//   }),
//   methods: {
//     addList: function () {
//       if (this.title == "" || this.body === "") return;
//       this.lists.push({ title: this.title, body: this.body });
//       this.title = "";
//       this.body = "";
//     },
//     deleteList: function (i) {
//       this.lists.splice(i, 1);
//     },
//   },
// };
</script>
