<template>
    <div id="app">
  <button v-on:click="show" class="button">show!</button>
  <modal name="hello-world" :draggable="true" :resizable="true">
    <!-- <div class="modal-header">
      <h2>Modal title</h2>
    </div> -->
    <div class="modal-body">
      <div>画像選択</div>
      <div><input type="text">名前</div>
      <div><input type="text">説明</div>
      <div><input type="text">パスワード</div>
      <div href="#">メンバーを招待</div>
      <button v-on:click="hide">閉じる</button>
    </div>  
  </modal>
</div>
</template>

<script>
Vue.use(VModal);
new Vue({
  el: '#app',
  methods: {
    show : function() {
      this.$modal.show('hello-world');
    },
    hide : function () {
      this.$modal.hide('hello-world');
    },
  }
})
</script>