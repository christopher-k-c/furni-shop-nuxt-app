<template>

    <!-- <div class="flex flex-col sm:flex-row justify-around items-start h-auto bg-black/90 w-full space-x-4 p-4"> -->

        <!-- <div class="flex flex-row justify-around w-full"> -->
            <!-- List -->
            <!-- <ul class="space-y-4">
                <h4 class="font-bold">About</h4>
                <li v-for="item in contact" :key="item" class="flex flex-col text-slate-300">  
                    {{ item }}   

                </li>
            </ul> -->

            <!-- Social -->
            <!-- <div class="flex flex-col space-y-4">
                <h4 class="font-bold">Social</h4>
                <div v-for="icon in social" :key="icon">
                    <a :href="icon.htt" class="flex items-end">
                        <img :src="icon.url" class="w-[30px] h-auto">
                        <p class="ml-4 text-slate-300">{{ icon.text }}</p>
                    </a>
                </div>
            </div>
        </div> -->
        <!-- Map -->
        <!-- <div class="flex justify-center items-center"> -->

        <div class="flex flex-col sm:flex-row sm:justify-around items-start w-full h-auto bg-black/90">
            <!-- List -->
            <ul class="space-y-4">
                <h4 class="font-bold">About</h4>
                <li v-for="item in contact" :key="item" class="flex flex-col text-slate-300">  
                    {{ item }}   
                </li>
            </ul>

            <!-- Social -->
            <div class="flex flex-col space-y-4">
                <h4 class="font-bold">Social</h4>
                <div v-for="icon in social" :key="icon">
                    <a :href="icon.htt" class="flex items-end">
                        <img :src="icon.url" class="w-[30px] h-auto">
                        <p class="ml-4 text-slate-300">{{ icon.text }}</p>
                    </a>
                </div>
            </div>



        <!-- </div> -->
    </div>



        <div class="w-full aspect-w-16 aspect-h-9">
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3336.0411177223555!2d-0.1292968540820232!3d51.502230267555554!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x487604ce37bbdb95%3A0x5120415568fd2d8b!2sCentral%20London%2C%20London%20SW1A%202DR!5e0!3m2!1sen!2suk!4v1681203206864!5m2!1sen!2suk" 
                class="w-full h-full" 
                style="border:0;" 
                allowfullscreen="" 
                loading="lazy" 
                referrerpolicy="no-referrer-when-downgrade">
            </iframe>
        </div>

</template>

<script>


    export default {
        data(){
            return {
                contact:[
                "Home",
                "Features",
                "Pricing",
                "Registration",
                "Contact"
                ],
                social: [
                {url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/facebook/facebook-original.svg", htt: "https://www.facebook.com", text: "Facebook"},
                {url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/twitter/twitter-original.svg", htt: "https://twitter.com", text: "Twitter"},
                {url: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/slack/slack-original.svg", htt: "https://slack.com/", text: "Slack"},
                
            ]
            }
        }
        
    }
</script>

<style lang="scss" scoped>

</style>