<template>
    <div>
        
        <p v-if="life === 'life cycle' ">{{life}}</p>
        
        <button @click="life = 'halo halo aja'">Update</button>
    </div>
</template>

<script>
export default {
   data: () => {
       return {
           life: "life cycle",
       };
   },
   beforeCreate() {
       alert(this.life + "before created");
   },
   created() {
       alert(this.life + "created");
   },
   beforeMount() {
       alert(this.life + "before mounted");
   },
    mounted() {
        alert(this.life + "mounted");
    },
    beforeUpadate() {
        alert(this.life + "before update");
    },
    updated() {
        alert(this.life + "updated");
    },
    beforeDestroy() {
        alert(this.life + "before destroy");
    },
    destroyed() {
        alert(this.life + "destroyed");
    },
}
</script>

<style>

</style>