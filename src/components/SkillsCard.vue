<template>
       <div class="skills-card" v-for="skill in skills">
            
            <img v-bind:src="skill.img">
            <div class="skills-card__wraper">
                <div class="skills-card__name"> {{skill.name}} </div>
                <div class="skills-card__function"> {{skill.function}} </div>
            </div>
        </div>
            
        

</template>

<script>
export default {
    props: {
        skills: {
        type: Array,
        required: true
       } 
    }
}

</script>

<style>
.skills-card {
    border-radius: 8px 0 0 0;
    padding: 16px;
    width: 227px;
    height: 129px;
    background: #f7f9fc;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
}
.skills-card__name {
    font-weight: 500;
    font-size: 14px;
    color: #2e2e48;
    text-align: center;
}
.skills-card__function {
    font-weight: 400;
    font-size: 10px;
    text-align: center;
    color: #79819a;
}
</style>