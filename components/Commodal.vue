<template>
<div style="text-align:right">
  <b-button v-b-modal.modal-1 class="btn-circlelg" style="background-color:#cddc39; border:none; margin-right:16px">＋</b-button>

  <b-modal id="modal-1" title="コミュニティ新規作成">
    <div class = "creater">
        <form action="" method="post">
        <label for="ComunityName">作成するコミュニティの名前を記入してください</label>
        <input class="form-control" type="text" name="ComunityName" id="ComunityName">
        </form>
        <br>
        <form action="" method="post">
        <label for="ComunityDescription">説明</label>
        <br>
        <input class="form-control" type="text" name="ComunityDescription" id="ComunityDescription" placeholder="任意">
        </form>
        <br>
        <form action="" method="post">
            <div class="row d-inline-block" style="padding:0px 16px;">
            <div class="col-xs-8">   
                <label for="Invitation">メンバー招待</label>
                <br>
                <input class="form-control" type="text" name="Invitation" id="Invitation" placeholder="ユーザーID" v-model="memberID">
            </div>
            </div>
            <!-- type = button　にすると閉じない -->
            <button type="button" class="btn btn-danger btn-circle btn-circle-sm m-1 d-inline-block" @click="AddInvite">＋</button>
        </form>
        <li class="d-inline-block" style="width:50%" v-for="member in members" :key="member">
            {{member}}
        <b-button variant="outline-secondary" type="button" @click="Remove(member)">削除</b-button>
        </li>
    </div>
  </b-modal>
</div>
</template>

<script>
export default{
   
   data(){
       return{
       members: [],
       memberID : ""
   }
   },
    methods:{
        AddInvite(){
            this.members.push(
                this.memberID
            );
        },
        Remove(target){
            var index = this.members.indexOf(target)
            this.members.splice(index,1)
            // splice(始まり,消去数)
        }
    }
   
};
</script>

<style scoped>
.btn-circle {
  width: 30px;
  height: 30px;
  line-height: 30px;
  text-align: center;
  vertical-align: center;
  padding: 0px;
  font-weight:bold;
  font-size: 20px;
  border-radius: 50%;
}
.btn-circlelg {
  width: 40px;
  height: 40px;
  line-height: 40px;
  text-align: center;
  vertical-align: center;
  padding: 0px;
  font-weight:bold;
  font-size: 27px;
  border-radius: 50%;
}


</style>