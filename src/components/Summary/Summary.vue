<template>
    <div class="summary_container">
        <h3>Summary</h3>
        <ul class="summary_category_container">
            <li class="summary_category_item" v-for="item in jsonData" :key="item.category">
                <p><img :src=item.icon alt="Category icon">{{ item.category }}</p>
                <p><span>{{ item.score }}</span> / 100</p>
                
            </li>
        </ul>
        <button>Continue</button>
    </div>
</template>
  
<script>
import data from '../../json/data.json'
export default {
    name: 'YourSummary',
    data() {
        return {
            jsonData: data
        };
    }
}
</script>
  
<style scoped src="./Summary.scss" lang="scss"></style>
  