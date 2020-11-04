<template>
  <div class="about">
    <h1>My daily activity</h1>
    <h2>Tambah tugas</h2>
    <input v-model="newTask" type="text" placeholder="input some task"/>
    <button @click="addTask">add</button>

    <h3>Tugas Hari ini</h3>
    <ul v-for="(task, index) in tasks" :key="index">
      <li>
      {{editIndex !== index ? task : null }} <input v-if="editIndex === index" v-model="editInput" type="text"/>
      <button @click="delTask(index)">delete</button>
      <button @click="saveEdit(index)" v-if="editIndex === index" >Save</button>
      <button v-if="editIndex !== index" @click="editTask(index)">Edit</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      tasks: ["Diving", "Break dance", "Basket"],
      newTask: '',
      editInput: '',
      editIndex: true
    }
  },
  methods: {
    addTask: function() {
      this.tasks.push(this.newTask);
    },
    delTask: function (index){
      this.tasks.splice(index, 1);
    },
     editTask: function(index){
        this.editIndex = index;
        this.editInput = this.tasks[index];
        console.log(this.editInput);
        console.log(this.editIndex);
      },
      saveEdit: function(index){
        this.tasks[index] = this.editInput;
        console.log(this.tasks);
        this.editIndex = true;
      }
  }
}
</script>

<style scoped>
h1{
  font-family: 'Just Another Hand', cursive;
}
h2{
  font-style: bold;
}

h3{
  font-family: 'Josefin Slab', serif;
  font-size: 15pt;
  font-style: bold;
}

li{
  text-align: center;
  font-family: 'Josefin Slab', serif;
}
</style>
