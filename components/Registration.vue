<template>

<div class="flex flex-col justify-center items-center w-full h-[900px] bg-cyan-950 space-y-4 relative">
    <div v-if="isLoading" class="absolute left-0 right-0 bottom-0 top-0 z-30 flex justify-center items-center">
        <h1 class="text-6xl">I am loading</h1>
    </div>

    <div class="p-8 mb-16 rounded-lg backdrop-blur bg-slate-100/50 font-bold text-white">
            <h1 class="font-poppins text-2xl sm:text-4xl md:text-5xl lg:text-6xl leading-tight sm:leading-tight md:leading-tight">Sign Up!</h1>
    </div>


    <form @submit.prevent="submitForm" class=" flex flex-col justify-center items-center w-11/12 space-y-4 bg-slate-500/10 rounded-lg p-4 drop-shadow-xl ">
        <label for="firstName" class="font-bold text-slate-200">
            First Name:
        </label>
        <!-- Define the input type, set id and bind input to the form object -->
        <input type="text" id="firstName" v-model="registration.first" class="rounded-sm w-1/2">

        <label for="lastName" class="font-bold text-slate-200">
            Last Name:
        </label>
        <!-- Define the input type, set id and bind input to the form object -->
        <input type="text" id="lastName" v-model="registration.last" class="rounded-sm w-1/2">

        <label for="email" class="font-bold text-slate-200">
            Email:
        </label>
        <!-- Define the input type, set id and bind input to the form object -->
        <input type="email" id="email" v-model="registration.email" class="rounded-sm w-1/2">

        <label for="password" class="font-bold text-slate-200">
            Password:
        </label>
        <!-- Define the input type, set id and bind input to the form object -->
        <input type="password" id="password" v-model="registration.password" class="rounded-sm w-1/2"/>

        <label for="confirmPassword" class="font-bold text-slate-200">
            Confirm Password:
        </label>
        <!-- Define the input type, set id and bind input to the form object -->
        <input type="password" id="confirmPassword" v-model="registration.confirm" class="rounded-sm w-1/2"/>

        <button type="submit" class="bg-black text-white p-4 m-2 drop-shadow-xl font-bold">Register</button>
    </form>
   
</div>



</template>

<script>


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
                isLoading: false,
            }
        },
        
        methods:{
            

            submitForm(event) {
            this.isLoading = true;
            setTimeout(() => {
                for (let key in this.registration) {
                    if (this.registration[key].length == 0) {
                        console.log(`The ${key} input is empty`);
                        event.preventDefault();
                        return;
                    }
                }

        if (this.registration.password === this.registration.confirm) {
            console.log("Form Submission Successful:", this.registration);
            event.preventDefault();
            return;
        } else {
            console.log("Passwords do not match!", this.registration);
        }
        this.isLoading = false; // Set isLoading to false after the delay
    }, 2000);
}

        }
        
    }
</script>

<style lang="scss" scoped>

</style>