<script setup lang="ts"></script>

<template>
    <div class="container">
        <span class="icon">
            <Asterisk></Asterisk>
        </span>
        <slot></slot>
    </div>
</template>

<style scoped>
.container {
    display: flex;
    justify-content: center;
    align-items: center;
    color: var(--ind-accent);
    font-size: 0.9rem;
}
.icon {
    margin-right: 10px;
    color: var(--ind-accent-2);
}
</style>
