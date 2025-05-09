<template>
    <div class="achievements-card" v-for="achievement in achievements">
         <div class="grafic">
            <div class="grafic__wrap-point">
                <div class="grafic__point"> </div> 
                <div class="grafic__line"> </div>
            </div>             
          </div> 
         <div class="achievements-content"> 
            <div class="achievements-content__main"> 
                <div class="achievements-content__time__wrap"> 
                    <div class="achievements-content__time"> {{achievement.time}} </div>
                    <img class="achievements-content__img" src="../img/achievements/Icon_location.svg">
                    <div class="achievements-content__place"> {{achievement.place}} </div>
                </div>
                <div class="achievements-content__company__wrap">
                    <img v-bind:src="achievement.img" class="achievements-content__company__img">
                    <div class="achievements-content__company__block">
                        <div class="achievements-content__company__role">{{achievement.role}}</div>
                        <div class="achievements-content__company__title">{{achievement.company}}</div>                        
                    </div>
                </div>
            </div>
            <div class="achievements-content__descr"> 
                <div class="achievements-content__descr__text"> {{achievement.descr}}</div>
            </div>
         </div>
    </div>
            
        

</template>

<script>
export default {
    props: {
       achievements: {
        type: Array,
        required: true
       } 
    }
}

</script>

<style>
.achievements-card {
    width: 697px;
    min-height: 86px;
    display: flex;
    justify-content: space-between;
}
.grafic {
    width: 24px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}
.grafic__wrap-point {
    width: 24px;
    height: 24px;
    display: flex;
    justify-content: center;
    align-items: center;
}
.grafic__point {
    color: #2e2e48;
    width: 8px;
    height: 7px;
    border-radius: 100%;

}
.grafic__line {
    border: 2.02px solid #f7f9fc;
    width: 1px;
    height: 100%;
}
.achievements-content {
    padding: 6px 0px 16px 0px;
    width: 657px;
    height: 100%;
    display: flex;
    justify-content: space-between;
}
.achievements-content__main {
    width: 242px;
    min-height: 65px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}
.achievements-content__time__wrap {
    width: 242px;
    height: 16px;
    display: flex;
    justify-content: start;
}
.achievements-content__company__wrap {
    width: 242px;
    min-height: 44px;
    display: flex;
    justify-content: start;
}
.achievements-content__time {
    font-weight: 400;
    font-size: 10px;
    color: #47516b;
    padding-top: 3.5px;
}
.achievements-content__img {
    margin-left: 4.03px;
    margin-right: 4.03px;
}
.achievements-content__place {
    font-weight: 400;
    font-size: 10px;
    color: #79819a;
    padding-top: 3.5px;
}
.achievements-content__descr {
    display: block;
    width: 407.4px;
}
.achievements-content__descr__text {
    font-weight: 400;
    font-size: 12px;
    color: #79819a;
}
.achievements-content__company__title {
    color: #2E2E48; 
    font-size: 14.12px;
    font-weight: 500;
}
.achievements-content__company__role {
    color: #79819A; 
    font-size: 12.10px;
    font-weight: 400;
    margin-bottom: 4.3px;
}
.achievements-content__company__img {
    margin-right: 16.13px;
}
</style>