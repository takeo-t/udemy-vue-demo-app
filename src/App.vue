<script setup>
import { ref } from 'vue';
import FoodCard from './components/FoodCard.vue';
const foods = ref([
    { name: '寿司', emoji: '🍣' },
    { name: 'ハンバーガー', emoji: '🍔' },
    { name: 'ラーメン', emoji: '🍜' },
    { name: 'カレー', emoji: '🍛' },
    { name: 'ピザ', emoji: '🍕' },
    { name: 'サンドイッチ', emoji: '🥪' },
    { name: 'タコス', emoji: '🌮' },
    { name: 'フライドチキン', emoji: '🍗' },
    { name: 'アイスクリーム', emoji: '🍦' },
    { name: 'ケーキ', emoji: '🍰' },
    { name: 'ドーナツ', emoji: '🍩' },
    { name: 'チョコレート', emoji: '🍫' },
    { name: 'クッキー', emoji: '🍪' },
    { name: 'フルーツ', emoji: '🍉' },
    { name: 'サラダ', emoji: '🥗' },
    { name: 'スープ', emoji: '🍲' },
    { name: 'おにぎり', emoji: '🍙' },
    { name: '焼き鳥', emoji: '🍢' },
    { name: '餃子', emoji: '🥟' },
    ]);
const pickedFoodIndex = ref(0)
</script>

<template>
    <main>
        <h1 class="title">今日何食べる？</h1>
        <FoodCard :name="foods[0].name" :emoji="foods[0].emoji" />
        <p>VS</p>
        <FoodCard :name="foods[1].name" :emoji="foods[1].emoji" />
    </main>
</template>

<style scoped>
main {
    width: 350px;
    margin: 100px auto;
    text-align: center;
}
.title {
    margin-bottom: 60px;
}
</style>
