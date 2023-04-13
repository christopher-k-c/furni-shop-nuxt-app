<template >
    <div class="flex flex-col justify-center items-center py-16 relative " name="Pricing" id="Pricing">
        
        <div class="p-8 mb-16 rounded-lg backdrop-blur bg-cyan-950/50 font-bold text-white">
            <h1 class="font-poppins text-2xl sm:text-4xl md:text-5xl lg:text-6xl leading-tight sm:leading-tight md:leading-tight">Our Pricing</h1>
        </div>
       <!-- flex-shrink-0 flex-grow w-full  -->
        <div class="flex lg:flex-row flex-col justify-center items-center w-11/12 space-y-4 sm:space-y-0">
            <div v-for="(des, indx) in priceList" :key="indx" class=" rounded-lg backdrop-blur bg-white/50 text-slate-900 text-center p-8 space-y-4 w-full h-auto sm:w-[400px] sm:h-[700px] sm:m-4 m-4" >
                <h1 class="text-3xl sm:text-4xl">{{ des.priceName }}</h1>
                
                <h3 class="text-slate-400">{{ des.subDescription }}</h3>

                <h1 class="">£ {{ des.priceType }}</h1>
                
                <ul class="space-y-4 text-left">
                    <li v-for="(content, index) in des.contents" :key="index">
                        <div v-if="content.boo" class="flex items-start space-x-1">
                            <img src="https://img.icons8.com/color/48/null/checkmark--v1.png" alt="tick" :style="{ width: '20px', height:'20px' }">
                            <p>{{ content.txt }}: <span>{{ content.info }}</span></p>
                        </div>
                        <div v-else="content.boo" class="flex items-start space-x-1">
                            <img src="https://img.icons8.com/color/48/null/delete-sign--v1.png" alt="cross" :style="{ width: '20px', height:'20px'}" class="mt-1"/>
                            <p class="text-slate-500">{{ content.txt }}: <span>{{ content.info }}</span></p>
                        </div>
                    </li>
                </ul>
                <button class="bg-cyan-950 text-white p-2 mt-4"> Get Started </button>

            </div>
        </div>

        <img src="../assets/images/1.jpeg" alt="Hero Image" class="absolute object-cover h-full w-full -z-10 " />

    </div>
   
</template>

<script>

    export default {
        name: "price-list",
        data(){
            return {
                priceList: [
                    {
                        id: 1,
                        priceName: "Buy",
                        subDescription: "Best option for one time purchase",
                        priceType: "Fixed",
                        contents:[
                            {id: 2, boo: true, txt: "shipping", info: "Free Shipping"},
                            {id: 3, boo: false, txt: "design", info: "Custom Designs"},
                            {id: 4, boo: false, txt: "flexibility", info: "Flexible Schedules"},
                            {id: 5, boo: false, txt: "setup", info: "Professional Installation"},
                            {id: 6, boo: false, txt: "replacements", info: "12 Month Warranty"},
                            {id: 7, boo: false, txt: "sustainable", info: "Circular ecosystem"},
                        ]

                    },
                    {
                        id: 2,
                        priceName: "Lease",
                        subDescription: "Relevant for short term tenants",
                        priceType: "Variable",
                        contents:[
                            {id: 2, boo: true, txt: "shipping", info: "Free Shipping"},
                            {id: 3, boo: true, txt: "design", info: "Custom Designs"},
                            {id: 4, boo: true, txt: "flexibility", info: "Flexible Schedules"},
                            {id: 5, boo: false, txt: "setup", info: "Professional Installation"},
                            {id: 6, boo: false, txt: "replacements", info: "24 Month Warranty"},
                            {id: 7, boo: false, txt: "sustainable", info: "Circular ecosystem"},
                        ]
                    },
                    {
                        id: 3,
                        priceName: "Subscription",
                        subDescription: "Essential for long term rentals",
                        priceType: "Variable",
                        contents:[
                            {id: 2, boo: true, txt: "shipping", info: "Free Shipping"},
                            {id: 3, boo: true, txt: "design", info: "Custom Designs"},
                            {id: 4, boo: true, txt: "flexibility", info: "Flexible Schedules"},
                            {id: 5, boo: true, txt: "setup", info: "Professional Installation"},
                            {id: 6, boo: true, txt: "replacements", info: "24 Month Warranty"},
                            {id: 7, boo: true, txt: "sustainable", info: "Circular ecosystem"},
                        ]
                    },
                ]

            }

        }
        
    }
</script>

<style lang="scss" scoped>

</style>


