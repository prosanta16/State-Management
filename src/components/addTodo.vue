<template>
<div>
    <h3>Add Todo</h3>
    <div class="add">
        <form @submit="onsubmit">
            <input type="text" v-model="title" placeholder="Add todo.....">
            <input type="submit" value="submit">
        </form>
    </div>
</div>
    
</template>

<script>
import {mapActions} from 'vuex';
export default{
    name:"addTodo",
    data(){
        return {
            title:''
        }
    },
    methods:{
        ...mapActions(['addTodo']),
        onsubmit(e){
            e.preventDefault();
            this.addTodo(this.title);
        }
    }
    
}
</script>

<style scoped>
form {
  display: flex;
}
input[type="text"] {
  flex: 10;
  padding: 10px;
  border: 1px solid #41b883;
  outline: 0;
}
input[type="submit"] {
  flex: 2;
  background:#0080ff;
  color: #fff;
  border: 1px #41b883 solid;
  cursor: pointer;
}

</style>