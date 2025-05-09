<template>
           
     <div class="card" v-for="university in universities">
        <div class="card__title-wrap">
            <img v-bind:src="university.img">
            <div class="card__title">{{university.title}}</div>
        </div>
        <div class="card__level-wrap">
            <div class="card__level">{{university.level}}</div>
            <div class="card__time">{{university.time}}</div>
            <div class="card__completion"> <span>Percentage</span> {{university.completion}}</div>
        </div>
            
    </div>
    

</template>

<script>
export default {
    props: {
       universities: {
        type: Array,
        required: true
       } 
    }
}

</script>

<style scoped>
.card {
    border-radius: 8px 0 0 8px;
    padding: 16px 24px;
    width: 227px;
    height: 158px;
    background: #f7f9fc;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}
.card__title-wrap {
    width: 178px;
    height: 48px;
    display: flex;
    justify-content: flex-start;
}
.card__title {
    font-weight: 500;
    font-size: 12px;
    color: #2e2e48;
    margin-left: 16.13px;
    align-content: center;
}
.card__level-wrap {
    width: 178px;
    height: 70px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}
.card__level {
    font-weight: 500;
    font-size: 14px;
    color: #2e2e48;
}
.card__time {
    font-weight: 400;
    font-size: 10px;
    color: #79819a;
}
.card__completion {
    font-weight: 400;
    font-size: 12px;
    color: #79819a;
}
.card__completion span {
    font-weight: 400;
    font-size: 12px;
    color: #5d5fef;
}
</style>