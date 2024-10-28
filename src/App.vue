<script setup>
//import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
    <div id="invoice">
        <div class="grid grid-cols-2 gap-2">
            <div>
                <input type="file" name="" id="" placeholder="Choose Your Company Logo">
            </div>
            <div class="text-right">
                <h2 class="text-2xl">Invoice Number</h2>
                <input type="text" name="" id="">
            </div>
            <div>
                <textarea name="" id="" placeholder="Who This Voucher From (Required)" class="p-5 text-black">

                </textarea>
                <div class="grid grid-cols-2 gap-2">
                    <div>
                        Bill To <br>
                        <textarea name="" id="" placeholder="Who is this voucher to? (required)" class="p-5 text-black"></textarea>
                    </div>
                    <div>
                        Ship To <br>
                        <textarea name="" id="" placeholder="(optional)" class="p-5 text-black"></textarea>
                    </div>
                </div>
            </div>
            <div  class="text-right">
                Date <input type="date" name="" id=""> <br>
                Due Date <input type="date" name="" id=""><br>
                PO Number <input type="text" name="" id="">
            </div>
        </div>
        <div class="grid grid-cols-4 gap-4">
            <div class="bg-white text-black p-2 text-center">Item</div>
            <div class="bg-white text-black p-2 text-center">Quantity</div>
            <div class="bg-white text-black p-2 text-center">Rate</div>
            <div class="bg-white text-black p-2 text-center">Amount</div>
            <div><input type="text" name="" id="" class="w-full"></div>
            <div><input type="number" name="" id="" class="w-full"></div>
            <div><input type="text" class="w-full"></div>
            <div class="text-right">$0.0</div>
        </div>
        <div><button type="submit" class="bg-green-600">+ ADD New</button></div>
        <div class="grid grid-cols-2 gap-2 my-5">
            <div>
                Notes <br>
                <textarea name="" id="" class="w-full min-h-[100px] text-black">

                </textarea>
            </div>
            <div class="text-right">
                Sub Total <input type="text" name="" id=""><br>
                Tax <input type="text" name="" id=""><br>
                <strong>Total: $0.0</strong>
            </div>
        </div>
    </div>
</template>

<style scoped>

</style>
