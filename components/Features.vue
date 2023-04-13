<template>
    <div class="flex justify-center bg-cyan-950">

        <div class="flex flex-col justify-center items-center  pb-16 xl:max-w-[1280px] w-full">


        <div class="p-8 mb-16 w-full backdrop-blur bg-cyan-950/50 font-bold text-white text-center space-y-4 pt-32">
            <h1 class="text-4xl md:text-5xl lg:text-6xl leading-tight sm:leading-tight md:leading-tight">What we offer</h1>
            <p class="text-2xl sm:text-3xl">We provide workshops, events and seasonal how-tos for members. They're packed with ideas to enhance the office you have and help you work the way you want; plus below you can find some of our additional benefits!</p>
        </div>


        <ul class="flex md:flex-row flex-col justify-between sm:w-11/12 w-full">
            <li v-for="item in featuresList" :key="item.id" class="flex flex-col items-start m-4  flex-1 backdrop-blur bg-white/10 rounded-lg drop-shadow-lg overflow-hidden"> 

                <div class="w-full h-[250px]">
                    <img :src="item.featureImg" :alt="item.featureName" class="w-full h-full object-cover rounded-t-lg  hover:scale-105">
                </div>
                <Icon :name="item.featureIcon" size="40" class="m-2"/>
                <h4 class="m-2 text-2xl sm:text-3xl md:text-4xl leading-tight sm:leading-tight md:leading-tight ">{{ item.featureName }}</h4>
                <p class="m-2 text-white">{{ item.featureDescription }}</p>

                
            </li>
        </ul>
    </div>
</div>
</template>

<script>
// ES6 module syntax to import the images directly; @ refers to root directory
import img1 from "@/assets/images/6.jpg";
import img2 from "@/assets/images/2.webp";
import img3 from "@/assets/images/4.jpeg";
    export default {
        name: "features-list",
        data(){
            return {
                featuresList: [
                    {
                        id: 1,
                        featureName: "Our Locations",
                        featureDescription: "Discover our nearest showroom - with 10+ locations across the UK.",
                        featureIcon: "fa-map-marker",
                        featureImg: img1,
                    },
                    {
                        id: 2,
                        featureName: "Free Samples",
                        featureDescription: "Choose from over 100 fab fabrics and we'll pop them in the post with a little surprise.",
                        featureIcon: "fa-envelope",
                        featureImg: img2,
                    },
                    {
                        id: 3,
                        featureName: "Free Brochures",
                        featureDescription: "Kick back, put your feet up and sample some tasty morsels from our brochure.",
                        featureIcon: "fa-book",
                        featureImg: img3,
                    }
                ]

            }

        }
        
    }
</script>

<style lang="scss" scoped>

</style>