<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/download.png">
    <h1>Hi Dunia</h1>
  <p>Mari fokus, biar nggak kena sihir hocus pocus 👻</p>


    <!-- <p>{{praxis}}</p>
    <p>ada merk {{mobil.merk}} berjumlah {{mobil.jumlah}}</p>
    
    <h2>Daftar Gadget</h2>
    <ol>
      <li v-for="gadget in gadgets" :key="gadget">{{gadget}}</li>
    </ol>
    <h3>{{motor}}</h3>
    <button v-on:click="display">Ubah</button>
    <h4>{{angka}}</h4>
    <button v-on:click="tambahnilai">+</button>
    <button v-on:click="kurangnilai">-</button> -->
    
    <Anggrek/>
    <lifecycle/>
    <Model/>
    <CRUD/>
    <ToDo/>
    <h2></h2>
  </div>
</template>

<script>


import Lifecycle from '@/Lifecycle.vue';
import Model from '@/Model.vue';
import CRUD from '@/CRUD.vue';
import ToDo from '@/ToDO.vue';
export default {
name: 'App',
components: {
  Lifecycle, Model, CRUD, ToDo,
},
  // data:function(){
  //   return{
  //     motor: 'ini motor beat',
  //     praxis: 'sebuah boot camp',
  //     mobil: {
  //       merk: 'cap buaya',
  //       jumlah: 20
  //     },
  //     gadgets: ['Laptop', 'Mobile', 'Camera'],
  //     angka:0
  //   }
  // },
  // methods: {
  //    display: function(){
  //       this.motor = 'ini motor triger';
  //       console.log(this.motor);
  //   },
  //   tambahnilai: function(){
  //     this.angka = this.angka+5;
  //   },
  //   kurangnilai: function(){
  //     this.angka = this.angka-5;

  //   },
    
  // }
  
}
</script>

<style>

#app{
text-align: center; 
font-family: 'Roboto', sans-serif;
}
h1{
  border: 20px;
}
p{
 font-family: 'Josefin Slab', serif;
 font-size: 12pt;
}
</style>
