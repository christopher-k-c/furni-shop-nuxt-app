<template>

    <div class="flex flex-col sm:flex-row sm:justify-around justify-center items-center sm:items-start w-full h-auto bg-black/90 pt-4 pb-4">
        <!-- List -->
        <ul class="space-y-4 sm:text-none text-center pb-4">
            <h4 class="font-bold text-xl text-cyan-100/90">About</h4>
            <hr>
            <li v-for="item in contact" :key="item" class="flex flex-col text-slate-300">  
                <a :href="`#${item}`">
                    {{ item }}   
                </a>
            </li>
        </ul>

        <!-- Social -->
        <div class="flex flex-col space-y-4 sm:text-none text-center pb-4">
            <h4 class="font-bold text-xl text-cyan-100/90">Social</h4>
            <hr>
            <div v-for="icon in social" :key="icon">
                <a :href="icon.htt" class="flex items-end">
                    <img :src="icon.url" class="w-[30px] h-auto">
                    <p class="ml-4 text-slate-300">{{ icon.text }}</p>
                </a>
            </div>
        </div>

                <!-- Email -->
        <div class="flex flex-col space-y-4 sm:text-none text-center pb-4">
            <h4 class="font-bold text-xl text-cyan-100/90">Contact Us</h4>
            <hr>
            <ul>
                <li class="flex flex-col text-slate-300">
                    Oxford Circus
                    <br>
                    London, 
                    <br>
                    WC1 3B4
                </li>
                <li class="flex flex-col text-slate-300">
                    Email: furni@shop.com
                </li>
                <li class="flex flex-col text-slate-300">
                    Phone: 01928739322893
                </li>
            </ul>
        </div>
    </div>

    <!-- Map spans width of footer, blue border is hidden by border-0 -->
    <div class="w-full aspect-w-16 aspect-h-9">
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3336.0411177223555!2d-0.1292968540820232!3d51.502230267555554!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x487604ce37bbdb95%3A0x5120415568fd2d8b!2sCentral%20London%2C%20London%20SW1A%202DR!5e0!3m2!1sen!2suk!4v1681203206864!5m2!1sen!2suk" 
            class="w-full h-full border-0" 
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