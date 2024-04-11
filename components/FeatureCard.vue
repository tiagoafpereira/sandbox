<script setup lang="ts"></script>

<template>
    <div class="container">
        <div class="header-image">
            <slot name="header-image"></slot>
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
    width: 100%;
    padding: 20px;
    background: linear-gradient(
        to top,
        var(--ind-dark) 0%,
        var(--ind-full-black) 100%
    );
    border-radius: 16px;
}

.title {
    font-size: 1.2rem;
    color: var(--ind-accent);
}

.description {
    font-size: 0.8rem;
}

.header-image {
    font-size: 3rem;
    display: flex;
    margin-bottom: 30px;
    justify-content: flex-start;
}
</style>
