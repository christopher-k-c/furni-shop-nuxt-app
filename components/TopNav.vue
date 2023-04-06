<template>
    <nav id="TopNav" class= "w-full flex py-6 justify-start items-center">
        <!-- Logo / Title -->
        <h4 class="font-poppins font-bold xs:text-[25px] text-[20px] xs:leading-[36.8px] leading-[26.8px] uppercase text-cyan-950">
            furni.store
        </h4>

        <!-- Render Navigation List -->
        <ul class="list-none sm:flex hidden justify-end items-center flex-1">
            <li  v-for="item in NaviagtionList"  :key="item" class="font-poppins font-normal cursor-pointer text-[16px] text-cyan-950">
                {{ item }}
            </li>
        </ul>

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
                    
                ]
            }
        }
    }
</script>

<!-- 
<template>
    <div>
      <h1>Navigation List</h1>
      <ul>
        <li v-for="item in navigationList" :key="item">
          {{ item }}
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    name: "nav-list",
    data() {
      return {
        navigationList: [
          "Home",
          "Features",
          "Pricing",
          "Registration",
          "Contact"
        ]
      };
    }
  };
  </script>
   -->