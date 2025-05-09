<template>
       <div class="certificates-card" v-for="certificate in certificates">
            <img v-bind:src="certificate.img">
            <div class="certificates-card__text">
                <div class="certificates-card__company">{{certificate.company}}</div>
                <div class="certificates-card__name">{{certificate.name}}</div>

            </div>
            <div class="certificates-card__time">{{certificate.time}}</div>
        </div>
            
        

</template>

<script>
export default {
    props: {
       certificates: {
        type: Array,
        required: true
       } 
    }
}

</script>

<style>
.certificates-card {
    border-radius: 8px 8px 0 0;
    padding: 15px 23px;
    width: 641px;
    height: 74px;
    background: #f7f9fc;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
}
.certificates-card__text {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 412px;
}
.certificates-card__company {
    font-weight: 400;
    font-size: 13px;
    letter-spacing: 0.01em;
    color: #79819a;
}
.certificates-card__name {
    font-weight: 500;
    font-size: 15px;
    color: #2e2e48;
}
.certificates-card__time {
    font-weight: 400;
    font-size: 11px;
    color: #47516b;
}
</style>