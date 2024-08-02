<script setup>
import { Plus } from '@element-plus/icons-vue'
</script>
<template>
    <div class="searchBox">
        <div class="searchItem">
            <div class="s-title">
                标题
            </div>
            <div class="selectvie">
                <el-input v-model="input" style="width: 200px" placeholder="Please input" />
                <el-select v-model="value" placeholder="并且" size="large" style="width: 100px; color: blue;"></el-select>
                <el-input v-model="input" style="width: 200px" placeholder="Please input" />
                <el-button :icon="Plus" circle style="border-width: 0;" />
            </div>
        </div>
        <div class="searchItem">
            er
        </div>
    </div>
</template>

<style scoped>
.searchBox {
    display: grid;
    margin: 20px;
    border-width: 2px;
    border-color: black;
}


.searchItem {
display: flex;
justify-content: center;
align-items: center;
}

</style>