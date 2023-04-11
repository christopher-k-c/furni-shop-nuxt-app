<template>
    <div class="flex justify-center items-start h-auto bg-cyan-950 w-full space-x-4 ">


        <!-- List -->
        <ul>
            <li v-for="item in contact" :key="item" class="flex flex-col ">  
                {{ item }}    
            </li>
        </ul>

        <!-- Map -->
        <div class="mb-4">
            Find us here!
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3336.0411177223555!2d-0.1292968540820232!3d51.502230267555554!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x487604ce37bbdb95%3A0x5120415568fd2d8b!2sCentral%20London%2C%20London%20SW1A%202DR!5e0!3m2!1sen!2suk!4v1681203206864!5m2!1sen!2suk" width="400" height="300" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
        </div>

        <!-- Social -->
        <div v-for="icon in social" :key="icon">

          <img :src="icon" class="w-[30px] h-auto">
          

        </div>
        


    
    </div>
</template>

<script>


    export default {
        data(){
            return {
                contact:[
                "About",
                "How it works",
                "Styles & brands",
                "Pricing",
                "Company",
                ],
                social: [
                "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/facebook/facebook-original.svg",
                "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/twitter/twitter-original.svg",
                "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/slack/slack-original.svg",
            ]
            }
        }
        
    }
</script>

<style lang="scss" scoped>

</style>