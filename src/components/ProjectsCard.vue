<template>
       <div class="project-card" v-for="project in projects">
            <div class="project-card__wrap__1">
                <img class="project-card__img" v-bind:src="project.img">
                <div class="project-card__text"> 
                    <div class="project-card__text__name">{{project.name}}</div>
                    <div class="project-card__text__role">{{project.role}}</div>
                </div>
            </div>
            <div class="project-card__wrap__2">
                <img class="project-card__icon" v-bind:src="project.img2">
                <div class="project-card__link">{{project.link}}</div>
            </div>
           
        </div>
            
        

</template>

<script>
export default {
    props: {
        projects: {
        type: Array,
        required: true
       } 
    }
}

</script>

<style>
.project-card {
    border-radius: 8px 0 0 8px;
    padding: 24px;
    width: 342px;
    height: 150px;
    background: #f7f9fc;
}
.project-card__wrap__1 {
    height: 82px;
    width: 100%;
}
.project-card__text__name {
    font-weight: 500;
    font-size: 16px;
    color: #2e2e48;
}
.project-card__text__role {
    font-weight: 400;
    font-size: 14px;
    color: #79819a;
}
.project-card__text {
    width: 229px;
    height: 82px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}
.project-card__wrap__1 {
    display: flex;
    justify-content: space-between;
}
.project-card__link {
    margin-left: 12.1px;
    padding-top: 3px;
    font-weight: 500;
    font-size: 16px;
    text-decoration: underline;
    color: #516cf7;
}
.project-card__wrap__2 {
    display: flex;
    justify-content: start;
}
.project-card__img {
    width: 48px;
    height: 48px;
}
</style>