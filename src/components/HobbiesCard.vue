<template>
       <div class="hobbies-card" v-for="hobbi in hobbies">
            <img v-bind:src="hobbi.img">
            <div class="hobbies-card__text">{{hobbi.name}}</div>
        </div>
            
        

</template>

<script>
export default {
    props: {
        hobbies: {
        type: Array,
        required: true
       } 
    }
}

</script>

<style>
.hobbies-card {
    width: 266px;
    height: 34px;
    display: flex;
    justify-content: space-between;
}
.hobbies-card__text {
    font-weight: 500;
    font-size: 14px;
    color: #47516b;
    width: 215px;
    height: 19px;
    padding-top: 8px;
}

</style>