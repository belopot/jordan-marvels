<template>
    <b-container class="testimonials">
    <b-row class="flex-nowrap">
        <b-col cols="6">
            <b-row class="bubble-up">
                <p>"It didn't take too long to find the right experience for me and buy it instantly online. I had a couple of questions regarding the difficulty level of the hike and was right away taken care of by the customer care support. Amazing hike with so much to discover and share.</p>
            </b-row>
        </b-col>
        <b-col cols="6">
            <b-row class="bubble-up">
                <p>"It didn't take too long to find the right experience for me and buy it instantly online. I had a couple of questions regarding the difficulty level of the hike and was right away taken care of by the customer care support. Amazing hike with so much to discover and share.</p>
            </b-row>
        </b-col>
        <b-col cols="6">
            <b-row class="bubble-up">
                <p>"It didn't take too long to find the right experience for me and buy it instantly online. I had a couple of questions regarding the difficulty level of the hike and was right away taken care of by the customer care support. Amazing hike with so much to discover and share.</p>
            </b-row>
        </b-col>
    </b-row>
    <b-row>
        <b-col cols="6">
            <b-row align-v="center">
                <b-col cols="6">
                    <div class="d-flex align-items-center">
                        <b-img rounded="circle" class="mr-3" :src="require(`../../assets/svg/laura.svg`)"/>

                        <div class="info">
                            <b>Laura (27)</b>
                            January, 2020
                        </div>
                    </div>
                </b-col>
                <b-col cols="6">
                    <div class="d-flex align-items-center">
                        <b-img rounded="circle" class="mr-3" :src="require(`../../assets/svg/rene.svg`)"/>

                        <div class="info">
                            <b>Rene (39)</b>
                            Octobor, 2019
                        </div>
                    </div>
                </b-col>
            </b-row>
        </b-col>

        <b-col cols="6">
            <b-row align-v="center" class="flex-nowrap">
                <b-col cols="6">
                    <div class="d-flex align-items-center">
                        <b-img rounded="circle" class="mr-3" :src="require(`../../assets/svg/laura.svg`)"/>

                        <div class="info">
                            <b>Laura (27)</b>
                            January, 2020
                        </div>
                    </div>
                </b-col>
                <b-col cols="6">
                    <div class="d-flex align-items-center">
                        <b-img rounded="circle" class="mr-3" :src="require(`../../assets/svg/rene.svg`)"/>

                        <div class="info">
                            <b>Rene (39)</b>
                            Octobor, 2019
                        </div>
                    </div>
                </b-col>
                
                <b-col cols="6">
                    <div class="d-flex align-items-center">
                        <b-img rounded="circle" class="mr-3" :src="require(`../../assets/svg/laura.svg`)"/>

                        <div class="info">
                            <b>Laura (27)</b>
                            January, 2020
                        </div>
                    </div>
                </b-col>
            </b-row>
        </b-col>
    </b-row>
    <b-row class="flex-nowrap">
        <b-col cols="6" offset="3">
            <b-row class="bubble-down" align-v="end">
                <p>"It didn't take too long to find the right experience for me and buy it instantly online. I had a couple of questions regarding the difficulty level of the hike and was right away taken care of by the customer care support. Amazing hike with so much to discover and share.</p>
            </b-row>
        </b-col>
        <b-col cols="6">
            <b-row class="bubble-down" align-v="end">
                <p>"It didn't take too long to find the right experience for me and buy it instantly online. I had a couple of questions regarding the difficulty level of the hike and was right away taken care of by the customer care support. Amazing hike with so much to discover and share.</p>
            </b-row>
        </b-col>
    </b-row>
    </b-container>
</template>
<script>

export default {
    name: "Profile",
    props: {
        svg_photo_img: String, 
        svg_name_img: String,
        png_bubble_img: String,
        png_text_img: String
    }  
}
</script>
<style lang="scss">
.testimonials{

    .bubble-up,
    .bubble-down{
        position: relative;
        width: 569px;
        height: 304px;
        background: url("../../assets/images/bubble-up.svg");
        background-size: 100%;
        background-repeat: no-repeat;
        background-position: center;
        padding: 45px;
        overflow: hidden;

        p{
            font-size: 16px;
            line-height: 1.8;
        }
    }
    .bubble-down{
        background: url("../../assets/images/bubble-down.svg");
    }
    .info{
        font-weight: 300;
        font-size: 14px;

        b{ 
            display: block;
            font-weight: bold;
            font-size: 22px;
        }
    }
} 

</style>