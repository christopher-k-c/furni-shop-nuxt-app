<template>
    <nav id="TopNav" :class="isToggled ? 'flex justify-start' : ' flex justify-between'" class= "w-full py-6 items-center px-2 relative">
        
        <!-- Logo / Title -->
        <h4 class="font-poppins font-bold uppercase text-cyan-950 px-4 z-10 text-2xl sm:text-3xl md:text-4xl leading-tight sm:leading-tight md:leading-tight flex justify-start">
            furni.store
        </h4>

        <!-- Render Desktop Navigation List -->
        <ul class="list-none md:flex hidden justify-end items-center flex-1">
            <li  v-for="item in NaviagtionList"  :key="item" 
            class="font-poppins font-normal cursor-pointer text-[16px] text-cyan-950 px-4">
                {{ item }}
            </li>
        </ul>
        <!-- Icon -->
        <div class="md:hidden px-4" :class="isToggled ? 'hidden' : 'flex'">
            <Icon name="fa-bars" size="20" @click="toggle" />
        </div>

        <!-- Render Mobile Navigation List -->
        <div :class="isToggled ? 'flex' : 'hidden'" class="fixed top-0 left-0 right-0 bottom-0 bg-slate-400 ">
            <Icon name="fa-times" size="20" @click="toggle" class="fixed top-7 right-6"/>
            <ul class="flex flex-col justify-center items-center h-full w-full">
                <li v-for="item in NaviagtionList" :key="item" class="text-[25px] py-4">
                    {{ item }}
                </li>
            </ul>
        </div>


    </nav>
</template>

<script>
    
    export default {
        name: "nav-list",
        data() {
            return {
                NaviagtionList: [
                    
                    "Home",
                    "Features",
                    "Pricing",
                    "Registration",
                    "Contact"
                    
                ],
                isToggled: false
            }
        },
        methods: {
            toggle(){
                this.isToggled = !this.isToggled // Make the toggle var the opposite eof it's current boolean val
            }
        }
    }
</script>

