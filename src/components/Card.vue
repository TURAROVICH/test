<template>
    <div class="card">
        <div class="title"><span v-for="(i,k) in name" :key="k">{{i}}</span></div>
        <div class="all-des">
            <div class="des">
          {{des}}
        </div>
        <div class="options">
            <div class="rooms"><span>rooms:</span>{{rooms}}</div> <div class="area"><span>area:</span>{{area}} {{unit}}</div>
        </div>
        </div>

        <div class="location">
            <div class="loc">
                <img src="../assets/loc.png" alt="">
                <div class="adress"><span v-for="(i,k ) in address" :key="k">{{i}}</span></div>
            </div>
            <img @click="isLike=!isLike"  v-if="!isLike" src="../assets/heart.svg" alt="">
            <img @click="isLike=!isLike"  :class="{active:!islike}"  v-else src="../assets/Vector.png" alt="">
        </div>
    </div>
</template>

<script>
export default {
    props:['name','des','rooms','area','unit','address'],
    data:()=>({
        isLike:false
    }),
    mounted(){
        console.log(this.name);
    }
}
</script>


<style scoped>

.active{
 transition: all .5s ease;
 animation: scl .5s 0s 1;
}
@keyframes scl{
    0%{
        transform: scale(1);
    }
    50%{
        transform: scale(1.5);
    }
    100%{
        transform: scale(1);
    }
}
*{
    font-family: Roboto;
}
.location{
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.loc{
    display: flex;
    gap: 10px;
    align-items: center;
    font-weight: 600;
    font-size: 14px;
    line-height: 13px;
    color: #5D6475;
}
.rooms span,.area span{
font-style: normal;
font-weight: normal;
font-size: 18px;
line-height: 27px;
/* identical to box height, or 148% */


color: #5D6475;

}
.rooms,.area{
    font-weight: 600;
font-size: 18px;
line-height: 27px;
/* identical to box height, or 148% */


color: #5D6475;
}
.options{
    display: flex;
    gap: 10px;
}
.title{
    font-family: Roboto;
font-style: normal;
font-weight: 600;
font-size: 24px;
line-height: 24px;
/* identical to box height, or 100% */


/* Black */

color: #292929;

display: flex;
gap: 10px;
}
.adress{
    display: flex;
    gap: 5px;
}
.des{
    font-style: normal;
font-weight: normal;
font-size: 18px;
line-height: 27px;
/* identical to box height, or 148% */


color: #5D6475;
}
.all-des{
        display: flex;
    flex-direction: column;
    gap: 5px;
}
.card{
    display: flex;
    flex-direction: column;
    gap: 10px;
    padding: 20px 30px;
    width: 80%;
    background: #FFFFFF;
box-shadow: 5px 5px 10px rgba(224, 224, 224, 0.2), -5px -5px 10px rgba(224, 224, 224, 0.2), 5px -5px 10px rgba(255, 255, 255, 0.9), -5px 5px 13px rgba(224, 224, 224, 0.9);
border-radius: 10px;
}

@media screen and (max-width:839px) {
.card{
    width: 80%;
}
}

@media screen and (max-width:454px) {
.title{
    flex-wrap: wrap;
}
}
</style>