<template>
    <div class="language-card" v-for="language in languages">
        <img class="language-card__img" v-bind:src="language.img">
        <div class="language-card__descr">
            <div class="language__text">{{language.name}}</div>
            <div class="language-card__level">{{language.level}}</div>
        </div>
    </div>
            
        

</template>

<script>
export default {
    props: {
        languages: {
        type: Array,
        required: true
       } 
    }
}

</script>

<style>
.language-card {
    width: 266px;
    height: 40px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.language-card__descr {
    width: 217px;
    height: 40px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}
.language__text {
    font-weight: 500;
    font-size: 14px;
    color: #47516b;
}
.language-card__level {
    font-weight: 400;
    font-size: 12px;
    color: #79819a;
}
</style>