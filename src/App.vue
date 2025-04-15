<script setup>
import  { ref }  from 'vue';
const now = new Date();

const timeStrRef = ref(new Date().toLocaleTimeString());

function changeTime() {
    const newTimeStr = new Date().toLocaleTimeString();
    timeStrRef.value = newTimeStr;
}
setInterval(changeTime, 1000);
</script>
<template>
    <p>現在時刻: {{ now }}</p>
    <p>現在時刻(ref):{{ timeStrRef }}</p>
</template>