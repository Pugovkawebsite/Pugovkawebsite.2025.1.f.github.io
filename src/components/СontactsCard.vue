<template>
       <div class="contact-card" v-for="contact in contacts">
            <div class="contact-card__img">
                <img v-bind:src="contact.img">
            </div>
           <div class="contact-card__text">
            <div class="contact-card__name">{{contact.name}}</div>
            <div class="contact-card__address">{{contact.address}}</div>
           </div>
        </div>
            
        

</template>

<script>
export default {
    props: {
        contacts: {
        type: Array,
        required: true
       } 
    }
}

</script>

<style>
.contact-card {
    width: 266px;
    height: 40px;
    display: flex;
    justify-content: space-between;
}
.contact-card__img {
    border-radius: 202px;
    width: 32px;
    height: 32px;
    background: #e2e6ee;
    display: flex;
    justify-content: center;
    align-items: center;
}
.contact-card__text {
    width: 217px;
    height: 40px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}
.contact-card__name {
    font-weight: 400;
    font-size: 12px;
    color: #79819a;
}
.contact-card__address{
    font-weight: 500;
    font-size: 14px;
    color: #47516b;
}
</style>