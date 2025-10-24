<script>
    export default { 
        // Add code in appropriate places
        data() {
            return {
                items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter']
            }
            
        },
        methods: {
            addItem(newItem) {
                this.items.push(newItem);
            },
            removeItem(index) {
                this.items.splice(index, 1);
            }
        }
    }
</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
    <ul>
        <li v-for="(item, index) in items" :key="item">
            {{ item }}
            <button type="button" @click="removeItem(index)">Delete</button>
        </li>
    </ul>
    <input type="text" v-model="newItem" placeholder="Add new item">
    <button type="button" @click="addItem(newItem); newItem=''">Add Item</button>
</template>
