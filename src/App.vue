<script setup>
import { reactive } from 'vue';

//import HelloWorld from './components/HelloWorld.vue'

const data = reactive({
    invoiceNumber:'',
    sender:'',
    billTo:'',
    shipTo:'',
    date:'',
    dueDate:'',
    poNumber:'',
    items:[{
        name:'',
        quantity:'',
        rate:'',
        amount:''
    }],
    notes:'',
    subTotal:'',
    tax:'',
    total:''
})

function addMoreItem(){
    data.items.push(
        {
            name:'',
            quantity:'',
            rate:'',
            amount:''
        }
    )
}
</script>

<template>
    <div id="invoice">
        <div class="grid grid-cols-2 gap-2">
            <div>
                <img src="./assets/logo.png" alt="">
            </div>
            <div class="text-right">
                <h2 class="text-2xl">Invoice Number</h2>
                <input v-model="data.invoiceNumber" type="text" name="" id="">
            </div>
            <div>
                <textarea v-model="data.sender" name="" id="" placeholder="Who This Voucher From (Required)" class="p-5 text-black">

                </textarea>
                <div class="grid grid-cols-2 gap-2">
                    <div>
                        Bill To <br>
                        <textarea v-model="data.billTo" name="" id="" placeholder="Who is this voucher to? (required)" class="p-5 text-black"></textarea>
                    </div>
                    <div>
                        Ship To <br>
                        <textarea v-model="data.shipTo" name="" id="" placeholder="(optional)" class="p-5 text-black"></textarea>
                    </div>
                </div>
            </div>
            <div  class="text-right">
                Date <input v-model="data.date" type="date" name="" id=""> <br>
                Due Date <input v-model="data.dueDate" type="date" name="" id=""><br>
                PO Number <input v-model="data.poNumber" type="text" name="" id="">
            </div>
        </div>
        <div class="grid grid-cols-4 gap-4">
            <div class="bg-white text-black p-2 text-center">Item</div>
            <div class="bg-white text-black p-2 text-center">Quantity</div>
            <div class="bg-white text-black p-2 text-center">Rate</div>
            <div class="bg-white text-black p-2 text-center">Amount</div>
        </div>
        <div v-for="(item,index) in data.items" :key="index" class="grid grid-cols-4 gap-4">
            <div><input v-model="item.name" type="text" name="" id="" class="w-full"></div>
            <div><input v-model="item.quantity" type="number" name="" id="" class="w-full"></div>
            <div><input v-model="item.rate" type="text" class="w-full"></div>
            <div class="text-right">$0.0</div>
        </div>
        <div>
            <button @click="addMoreItem()" type="submit" class="bg-green-600">+ ADD New</button>
        </div>
        <div>
            {{ data }}
        </div>
        <div class="grid grid-cols-2 gap-2 my-5">
            <div>
                Notes <br>
                <textarea v-model="data.notes" name="" id="" class="w-full min-h-[100px] text-black">

                </textarea>
            </div>
            <div class="text-right">
                Sub Total <input type="text" name="" id=""><br>
                Tax <input v-model="data.tax" type="text" name="" id=""><br>
                <strong>Total: $0.0</strong>
            </div>
        </div>
    </div>
</template>

<style scoped>

</style>
