<script>
import { ref } from 'vue';

export default {
    name: 'CounterComponent',
    setup() {
        const count = ref(0);

        const increment = () => {
            count.value++;
        };

        const decrement = () => {
            count.value--;
        };

        return {
            count,
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
        <input type="number" />
        <button>设置</button>
    </div>
</template>

<style></style>
