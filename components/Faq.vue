<script setup lang="ts">
const items = [
    {
        label: 'How much does the Inductiva Genesis Program cost?',
        defaultOpen: true,
        content:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.',
    },
    {
        label: 'What are the criteria for Inductiva Genesis Program eligibility?',
        content:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.',
    },
    {
        label: 'Why am I required to provide information about XXXXXX in the registration process?',
        content:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.',
    },
    {
        label: 'What if I can\'t disclose information about my partners/clients?',
        content:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.',
    },
    {
        label: 'What are the functionalities provided by the API within the Genesis Program?',
        content:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.',
    },
    {
        label: 'Do I control where the tasks will be run?',
        content:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.',
    },
    {
        label: 'What hardware is committed to the Inductiva Genesis Program?',
        content:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.',
    },
    {
        label: 'What is the purpose and structure of the “Application Demo” Repos?',
        content:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.',
    },
]
</script>

<template>
    <UAccordion :items="items" multiple color="gray" open-icon="">
        <template #default="{ item, index, open }">
            <div class="header" :class="open ? '' : 'closed'">
                {{ item.label }}
                <UIcon v-if="!open" name="i-heroicons-plus" class="icon" />
                <UIcon v-if="open" name="i-heroicons-x-mark" class="icon" />
            </div>
        </template>
        <template #item="{ item }">
            <div class="content">
                {{ item.content }}
            </div>
        </template>
    </UAccordion>
</template>

<style scoped>

.content {
    background-color: var(--ind-dark-int);
    border-radius: 0 0 16px 16px;
    padding: 0 16px 16px 16px;
}

.header {
    display: flex;
    cursor: pointer;
    justify-content: space-between;
    color: var(--light-text-color);
    background-color: var(--ind-dark-int);
    margin-bottom: -6px;
    padding: 16px;
    border-radius: 16px 16px 0 0;

    .icon {
        color: var(--light-text-color);
        font-size: 1.1rem;
    }
}

.closed {
    background-color: transparent;
    margin: 10px 0 10px 0;
    padding: 0 16px 0 16px;
}
</style>
