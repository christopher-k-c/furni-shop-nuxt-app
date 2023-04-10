<template>
    <div class="flex flex-col justify-center items-center bg-white py-8">
        <h1 class="font-poppins text-2xl sm:text-4xl md:text-5xl lg:text-6xl leading-tight sm:leading-tight md:leading-tight ">Our Pricing</h1>

        <ul class="flex md:flex-row flex-col justify-between w-3/4 ">
            <li v-for="item in featuresList" :key="item.id" class="flex flex-col items-start m-4 bg-slate-400/30 flex-1"> 

                <div class="w-full h-1/2">
                    <img :src="item.featureImg" :alt="item.featureName" class="w-full h-full object-cover">
                </div>
                <Icon :name="item.featureIcon" size="40" class="m-2"/>
                <h4 class="m-2 text-2xl sm:text-3xl md:text-4xl leading-tight sm:leading-tight md:leading-tight ">{{ item.featureName }}</h4>
                <p class="m-2">{{ item.featureDescription }}</p>

                
            </li>
        </ul>
    </div>
</template>

<script>
// ES6 module syntax to import the images directly; @ refers to root directory
import img1 from "@/assets/images/2.webp";
import img2 from "@/assets/images/3.jpeg";
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