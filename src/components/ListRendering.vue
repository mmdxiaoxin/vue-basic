<template>
    <div>
        <h1>列表渲染</h1>
        <ul>
            <li v-for="item in list" :key="item.id">{{ item.name }}</li>
        </ul>
    </div>
</template>

<script>
export default {
    setup() {
        const list = [
            { id: 1001, name: 'Vue' },
            { id: 1002, name: 'React' },
            { id: 1003, name: 'Angular' }
        ];
        return { list };
    }
};
</script>

<style lang="scss" scoped></style>
