<template>
    
<div class="flex justify-center bg-cyan-950 ">
<div class="flex flex-col justify-center items-center xl:max-w-[1280px] w-full space-y-4 relative pb-16" >

    <div class="p-8 mb-16 w-full backdrop-blur  font-bold text-white text-center space-y-4 pt-32">
            <h1 class="text-4xl md:text-5xl lg:text-6xl leading-tight sm:leading-tight md:leading-tight">Sign Up!</h1>
            <p class="text-2xl sm:text-3xl">Get all the wahooooos, benefits, rewards and more to bring your ideas to life. Whether you’re a newlywed or newly single, a pet parent or a family of 1 or 100, this is the club for everyone. Discover the benefits of being part of Furni.Shop Family.</p>
    </div>
    
    <!-- Display Loading Animation -->
    <div v-if="showSpinner" class="absolute left-0 right-0 bottom-0 top-0 z-10 flex justify-center items-center bg-slate-600/40">   
        <atom-spinner  :animation-duration="5000" :size="90" :color="'#ff1d5e'" class="z-30"/>
    </div> 


    <!-- <div class="p-8 mb-16 rounded-lg backdrop-blur bg-slate-100/50 font-bold text-white">
        <h1 class="font-poppins text-2xl sm:text-4xl md:text-5xl lg:text-6xl leading-tight sm:leading-tight md:leading-tight">Sign Up!</h1>
    </div> -->


<div class="w-11/12 flex flex-col md:flex-row md:justify-around justify-center items-center bg-slate-950/50 rounded-lg drop-shadow-xl px-16">
    <form @submit.prevent="submitForm" class=" flex flex-col justify-center items-start w-full space-y-4 p-4">

        <h1 class="text-4xl md:text-5xl lg:text-6xl leading-tight sm:leading-tight md:leading-tight text-white">Register An Account</h1>

        <label for="firstName" class="font-bold text-slate-200">
            First Name:
        </label>
        <!-- Define the input type, set id and bind input to the form object -->
        <input type="text" id="firstName" v-model="registration.first" class="rounded-sm sm:w-3/4 w-full" required>

        <label for="lastName" class="font-bold text-slate-200">
            Last Name:
        </label>
        <!-- Define the input type, set id and bind input to the form object -->
        <input type="text" id="lastName" v-model="registration.last" class="rounded-sm sm:w-3/4 w-full" required>

        <label for="email" class="font-bold text-slate-200">
            Email:
        </label>
        <!-- Define the input type, set id and bind input to the form object -->
        <input type="email" id="email" v-model="registration.email" class="rounded-sm sm:w-3/4 w-full" pattern="[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}" title="Please enter a valid email address" required>

        <label for="password" class="font-bold text-slate-200" name="Registration" id="Registration">
            Password:
        </label>
        <!-- Define the input type, set id and bind input to the form object -->
        <input type="password" id="password" v-model="registration.password" class="rounded-sm sm:w-3/4 w-full" required pattern=".{8,}" title="Password must be at least 8 characters"/>

        <label for="confirmPassword" class="font-bold text-slate-200">
            Confirm Password:
        </label>
        <!-- Define the input type, set id and bind input to the form object -->
        <input type="password" id="confirmPassword" v-model="registration.confirm" class="rounded-sm sm:w-3/4 w-full" required pattern=".{8,}" title="Password must be at least 8 characters"/>

        <a href="#" class="font-medium text-white hover:text-indigo-500">start your 14-day free trial</a>



        <button type="submit" class="bg-black text-white p-4 m-2 drop-shadow-xl font-bold">Register</button>



        
    </form>
    
    

    <img src="@/assets/images/undraw_completed_03xt.svg" alt="LogoSVG" class="w-[200px] h-auto m-8"/>
</div>



    <!-- <LogoSVG /> -->
   
</div>
</div>


</template>

<script>

import {AtomSpinner} from 'epic-spinners';


    export default {
        
        data(){
            
            return{
                registration: {
                    first: '',
                    last: '',
                    email: '',
                    password: '',
                    confirm: '',
                },
                showSpinner: false, // Add this boolean property
            }
        },  
        components: {
    AtomSpinner,

  },   
        
  methods: {
    async submitForm(event) {
      // Set showSpinner to true before the form submission
      this.showSpinner = true;

      for (let key in this.registration) {
        if (this.registration[key].length === 0) {
          console.log(`The ${key} input is empty`);
          event.preventDefault();
          // Set showSpinner back to false after form validation
          this.showSpinner = false;
          return;
        }
      }

      if (this.registration.password === this.registration.confirm) {
        // Delay the form submission for 2 seconds (for demonstration)
        await new Promise(resolve => setTimeout(resolve, 2000));

        console.log("Form Submission Successful:", this.registration);
        event.preventDefault();
        // Set showSpinner back to false after form submission
        this.showSpinner = false;
        alert("Registration Successful!")
        return;
      } else {
        console.log("Passwords do not match!", this.registration);

        alert("Passwords do not match!")
        // Set showSpinner back to false after form validation
        this.showSpinner = false;
      }
    },
  },
}
</script>

<style lang="scss" scoped>



</style>