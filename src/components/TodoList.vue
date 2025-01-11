<script setup lang="ts">
    import ListItem from './ListItem.vue';
    type Item = {
        title: string;
        checked?: boolean;
    }
    const GroupsItems: Item[] = [
        { title: 'Visitar a la abuela', checked: false },
        { title: 'Hacer la compra', checked: false },
        { title: 'Estudiar Vue 3', checked: false },
    ];
</script>

<template>
    <ul>
        <li :key="index" v-for="(item, index) in GroupsItems">
            <ListItem :isChecked="item.checked">
                {{ item.title }}
            </ListItem>
        </li> 
    </ul>
</template>

<style scoped>
    ul {
        list-style: none;
        padding: 0;
    }
</style>