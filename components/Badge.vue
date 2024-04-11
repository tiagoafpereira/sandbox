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
    width: fit-content;
    background-color: var(--ind-dark-int);
    border-radius: 8px;
    padding: 10px;
    font-size: 0.8rem;
}

.icon {
    margin-right: 10px;
    color: var(--ind-accent-2);
}
</style>
