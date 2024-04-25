<script>
import { ref } from 'vue';

export default {
    name: 'CounterComponent',
    setup() {
        const count = ref(0);
        const inputValue = ref('');

        const increment = () => {
            count.value++;
        };

        const decrement = () => {
            count.value--;
        };

        return {
            count,
            inputValue,
            increment,
            decrement
        };
    }
};
</script>

<template>
    <div>
        <h1>计数器</h1>
        <button @click="decrement">-</button>
        <span>目标count:{{ count }}</span>
        <button @click="increment">+</button>
        <input type="number" :value="inputValue" @change="(e) => (inputValue = e.target.value)" />
        <button @click="count = inputValue">设置</button>
        <span>等效简写：</span>
        <input type="number" v-model="inputValue" />
    </div>
</template>

<style></style>
