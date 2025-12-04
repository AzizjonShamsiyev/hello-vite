<template>
    <div>
        <p>Fruit Component</p>
        <ul>
            <li v-for="item in list" :key="item.id" style="margin-bottom: 12px; padding: 8px; border-left: 3px solid #42b983; background-color: #f5f5f5;">
                <strong>Fruit #{{ item.id }}:</strong> {{ item.name }} 
                <span style="color: #666;">({{ item.color }})</span>
                <br>
                <span style="font-size: 0.9em;">Price: ${{ item.price }}</span>
                <br>
                <span style="font-size: 0.85em; color: #888;">{{ item.info }}</span>
            </li>
        </ul>
    </div>
</template>
<script setup>
    import { reactive } from "vue";
    const list = reactive([
        { id: 1, name: "Apple", color: "Red", price: 3 , info: "Apples are nutritious fruits that come in various colors including red, green, and yellow. They are rich in fiber and vitamin C."},
        { id: 2, name: "Banana", color: "Yellow", price: 1 , info: "Bananas are elongated, yellow fruits known for their sweet taste and high potassium content. They are a popular snack and ingredient in smoothies."},
        { id: 3, name: "Grapes", color: "Purple", price: 2 , info: "Grapes are small, round fruits that grow in clusters on vines. They can be eaten fresh or used to make wine, juice, and raisins."},
        { id: 4, name: "Orange", color: "Orange", price: 2.5 , info: "Oranges are citrus fruits known for their bright orange color and tangy flavor. They are an excellent source of vitamin C and are often consumed as juice or eaten fresh."},
        { id: 5, name: "Strawberry", color: "Red", price: 4 , info: "Strawberries are small, red fruits with a sweet and slightly tart flavor. They are rich in antioxidants and vitamin C, making them a healthy treat."}
    ]);
</script>