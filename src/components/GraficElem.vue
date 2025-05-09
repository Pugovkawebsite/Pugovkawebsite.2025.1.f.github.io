<template>
    <div class="elem">
        <div class="elem__ball__wrap">
            <svg width="21" height="21" viewBox="0 0 21 21" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M10.3671 14.6266C8.0465 14.6266 6.16531 12.7454 6.16531 10.4249C6.16531 8.10433 8.0465 6.22314 10.3671 6.22314C12.6876 6.22314 14.5688 8.10433 14.5688 10.4249C14.5688 12.7454 12.6876 14.6266 10.3671 14.6266Z" fill="#5531A7" />
            </svg>
        </div>
        <div class="elem__line__wrap">
            <div class="elem__line"></div>
        </div>
    </div>
            
        

</template>

<script>
export default {
    props: {
        tools: {
        type: Array,
        required: true
       } 
    }
}

</script>

<style>
.elem__line {
  border: 2.02px solid #e2e6ee;
  width: 1px;
  height: 100%;
}
.elem {
  width: 96.81px;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
}
.elem__ball__wrap {
  width: 32px;
  height: 32px;
  border-radius: 202px;
  box-shadow: inset 0 2px 2px 0 rgba(0, 0, 0, 0.04), 0 12px 48px 0 rgba(0, 0, 0, 0.04), 0 2px 8px 0 rgba(0, 0, 0, 0.05);
  background: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
}
.elem__line__wrap {
  width: 32.27px;
  display: flex;
  justify-content: center;
  height: 100%;
}

</style>