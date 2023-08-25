<script setup lang='ts'>
</script>
<template>
    <button>
        <slot></slot>
    </button>
</template>
<style scoped>
    button{
        display: flex;
        gap: 8px;
        height: 48px;
        justify-content: center;
        align-items: center;
        padding: 0 2rem;
        background-color: var(--color-primary);
        border-radius: 40px;
        white-space: nowrap;
        border: none;
        outline: none;
        color: white;
        box-shadow: 0px 13px 25px -4px rgba(44, 171, 223, 0.20);
    }
</style>