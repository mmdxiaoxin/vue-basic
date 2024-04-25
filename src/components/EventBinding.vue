<template>
    <div className="EventBinding">
        <h1>事件绑定</h1>
        <button @click="handleClick">点击事件</button>
    </div>
</template>

<script>
export default {
    setup() {
        const handleClick = () => {
            alert('点击事件');
        };
        return { handleClick };
    }
};
</script>

<style lang="scss" scoped></style>
