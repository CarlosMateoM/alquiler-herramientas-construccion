<script setup>

import { onMounted, ref } from 'vue';
import Layaout from '../components/Layaout.vue';
import ItemCarrito from '../components/ItemCarrito.vue';
import useCarrito from '../service/CarritoService';

const {errors, carrito, showCarrito} = useCarrito();

onMounted(() => showCarrito());

</script>

<template>
	<Layaout>

	<template v-slot:main>

    <div class="h-screen bg-white">
	<div class="py-12">
		
    <div class="max-w-md mx-auto bg-white-500 shadow-lg rounded-lg  md:max-w-5xl">
        <div class="md:flex ">
            <div class="w-full p-4 px-5 py-5">

            	<div class="md:grid md:grid-cols-3 gap-2 ">

            		<div class="col-span-2 p-5">

            			<h1 class="text-xl text-yellow-300 font-medium ">Herramientas</h1>
						


						<ItemCarrito v-for="item in carrito.herramientas" :data="item" />
	

            			<div class="flex justify-between items-center mt-6 pt-6 border-t"> 
            				<div class="flex items-center">
            					
            				</div>

            				<div class="flex justify-center items-end">
            					
            				</div>
            				
            			</div>
            			
            		</div>

            		<div class=" p-5 bg-gray-800 rounded overflow-visible">

            			<span class="text-xl font-medium text-gray-100 block pb-3">Card Details</span>

            			<span class="text-xs text-gray-400 ">Card Type</span>

            			<div class="overflow-visible flex justify-between items-center mt-2">

            			


            				<div class="rounded w-52 h-28 bg-gray-500 py-2 px-4 relative right-10">

            					<span class="italic text-lg font-medium text-gray-200 underline">VISA</span>

            					<div class="flex justify-between items-center pt-4 ">
            						
            						<span class="text-xs text-gray-200 font-medium">****</span>
            						<span class="text-xs text-gray-200 font-medium">****</span>
            						<span class="text-xs text-gray-200 font-medium">****</span>
            						<span class="text-xs text-gray-200 font-medium">****</span>

            					</div>

            					<div class="flex justify-between items-center mt-3">
             						
            						<span class="text-xs  text-gray-200">Giga Tamarashvili</span>
            						<span class="text-xs  text-gray-200">12/18</span>
            					</div>


            					
            				</div>






            				<div class="flex justify-center  items-center flex-col">

            					<img src="https://img.icons8.com/color/96/000000/mastercard-logo.png" width="40" class="relative right-5" />
            					<span class="text-xs font-medium text-gray-200 bottom-2 relative right-5">mastercard.</span>
            					
            				</div>
            				
            			</div>




            			<div class="flex justify-center flex-col pt-3">
            				<label class="text-xs text-gray-400 ">Name on Card</label>
            				<input type="text" class="focus:outline-none w-full h-6 bg-gray-800 text-white placeholder-gray-300 text-sm border-b border-gray-600 py-4" placeholder="Giga Tamarashvili">
            			</div>


            			<div class="flex justify-center flex-col pt-3">
            				<label class="text-xs text-gray-400 ">Card Number</label>
            				<input type="text" class="focus:outline-none w-full h-6 bg-gray-800 text-white placeholder-gray-300 text-sm border-b border-gray-600 py-4" placeholder="****     ****      ****      ****">
            			</div>




            			<div class="grid grid-cols-3 gap-2 pt-2 mb-3">

            				<div class="col-span-2 ">

            					<label class="text-xs text-gray-400">Expiration Date</label>
            					<div class="grid grid-cols-2 gap-2">

            						<input type="text" class="focus:outline-none w-full h-6 bg-gray-800 text-white placeholder-gray-300 text-sm border-b border-gray-600 py-4" placeholder="mm">
            						<input type="text" class="focus:outline-none w-full h-6 bg-gray-800 text-white placeholder-gray-300 text-sm border-b border-gray-600 py-4" placeholder="yyyy">
            						
            					</div>


            					
            				</div>

            				<div class="">
            					<label class="text-xs text-gray-400">CVV</label>
            					<input type="text" class="focus:outline-none w-full h-6 bg-gray-800 text-white placeholder-gray-300 text-sm border-b border-gray-600 py-4" placeholder="XXX">
            					
            				</div>
            				
            			</div>

            			<button class="h-12 w-full bg-blue-500 rounded focus:outline-none text-white hover:bg-blue-600">Check Out</button>

            		</div>

            		
            	</div>
            	
               
           </div>
        </div>
    </div>
    </div>
</div>
</template>
	</Layaout>
    
</template>