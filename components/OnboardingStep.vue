<script setup lang="ts"></script>

<template>
    <div class="container">
        <div class="icon">
            <slot name="icon"></slot>
        </div>
        <div class="title">
            <slot name="title"></slot>
        </div>
        <div class="description">
            <slot></slot>
        </div>
    </div>
</template>

<style scoped>
.container {
    display: flex;
    flex-direction: column;
    height: 100%;
    padding: 20px;
    background-color: var(--ind-dark-int);
    border-color: var(--ind-dark-int);
    border-radius: 16px;
}

.title {
    font-size: 1.2rem;
}

.description {
    font-size: 0.8rem;
}

.icon {
    font-size: 3rem;
    display: flex;
    margin-bottom: 30px;
    justify-content: flex-start;
}
</style>
