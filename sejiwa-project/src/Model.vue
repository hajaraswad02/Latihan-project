<template>
    <div>
        <input v-model="pesan" placeholder="edit">
        <p> Output : {{pesan}}</p>
        <input v-model="Message" placeholder="ubah">
        <p>{{Message}}</p>
    </div>
</template>

<script>
export default {
    data: function() {
        return{
            pesan: "pesan"
        }
    },
    apaGitu: function() {
        return{
            message: "ok"
        }
    }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Josefin+Slab:ital,wght@1,700&display=swap');
input{
    text-align: center;
    color: forestgreen;
    font-size: 10pt;
    font-style: bold;
    
    
}
</style>