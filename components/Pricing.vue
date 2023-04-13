<template>

    <div class="flex justify-center bg-cyan-950/50 relative">
    
    <div class="xl:max-w-[1280px] w-full relative flex flex-col justify-center items-center font-poppins ">


        <div class="p-8 mb-8 w-full backdrop-blur font-bold text-white text-center space-y-4 pt-32">
            <h1 class="text-4xl md:text-5xl lg:text-6xl leading-tight sm:leading-tight md:leading-tight">Our Pricing</h1>
            <p class="text-2xl sm:text-3xl">We deliver a workspace furnishing service for a subscription fee that keeps things simple and affordable.</p>
        </div>




        <!-- Cards Container -->
        <div class="flex flex-col lg:flex-row justify-center items-center w-full h-full p-4 mb-10 ">



            <!-- Individual Cards rendered in container - plus initial for loop to access price name, description and type -->
            <div v-for="(des, indx) in priceList" :key="indx" class=" flex flex-col bg-slate-100 rounded-lg drop-shadow-lg w-full m-6 overflow-hidden backdrop-blur bg-white/50" >

                <div class="font-bold text-center px-2 py-5 text-3xl sm:text-4xl ">{{ des.priceName }}</div>

                <h3 class="text-center px-2 py-5 text-white">{{ des.subDescription }}</h3>

                <h1 class="text-center px-2 pb-5 font-bold">£ {{ des.priceType }}</h1>

                <!-- Nest for to access the array of objects -->
                <ul v-for="(el, index) in des.contents" :key="index" class="m-4 " >

                    <!-- If true display tick -->
                    <li v-if="el.boo" class="flex items-start space-x-1 hover:scale-105">

                        <img src="https://img.icons8.com/color/48/null/checkmark--v1.png" alt="tick" :style="{ width: '20px', height:'20px' }">
                        <p>{{ el.txt }}: <span>{{ el.info }}</span></p>

                    </li>

                    <!-- If false display cross -->
                    <li v-else="el.boo" class="flex items-start space-x-1 hover:scale-105">

                        <img src="https://img.icons8.com/color/48/null/delete-sign--v1.png" alt="cross" :style="{ width: '20px', height:'20px'}" class="mt-1"/>
                        <p class="text-slate-500">{{ el.txt }}: <span>{{ el.info }}</span></p>
                    
                    </li>
            
                </ul>

                <button class="bg-cyan-950 text-white p-2 mt-4"> Get Started </button>

            </div>

        </div>
        

    </div>
    <img src="../assets/images/1.jpeg" alt="Hero Image" class="absolute left-0 right-0 top-0 bottom-0 object-cover h-full w-full -z-10 " />
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
                        priceType: "Fixed Price",
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
                        priceType: "Variable Price",
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
                        priceType: "Variable Price",
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
   