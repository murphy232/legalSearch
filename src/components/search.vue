<script setup>
import { ref } from 'vue'
import { Plus } from '@element-plus/icons-vue'
const value2 = ref('')
</script>

<template>
    <div class="root">
        <div class="searchBox">

            <div class="searchItem">
                <div class="s-logic">
                    <el-select v-model="value" placeholder="并且" size="medium" style="width: 80px;"></el-select>
                </div>
                <div class="s-title">
                    标题
                </div>
                <div class="selectvie">
                    <el-input v-model="input" style="width: 200px" placeholder="Please input" />
                    <el-select v-model="value" placeholder="并且" size="medium" style="width: 80px; color: blue;"></el-select>
                    <el-input v-model="input" style="width: 200px" placeholder="Please input" />
                    <el-button :icon="Plus" circle style="border-width: 0;" />
                </div>
            </div>
            <div class="searchItem">
                <div class="s-logic">
                    <el-select v-model="value" placeholder="并且" size="medium" style="width: 80px;"></el-select>
                </div>
                <div class="s-title">
                    全文
                </div>
                <div class="selectvie">
                    <el-input v-model="input" style="width: 200px" placeholder="Please input" />
                    <el-select v-model="value" placeholder="并且" size="medium" style="width: 80px; color: blue;"></el-select>
                    <el-input v-model="input" style="width: 200px" placeholder="Please input" />
                    <el-select placeholder="同篇" size="medium" style="width: 80px;"></el-select>
                    <el-button :icon="Plus" circle style="border-width: 0;" />
                </div>
            </div>

            <div class="searchItem">
                <div class="s-logic">
                    <el-select v-model="value" placeholder="并且" size="medium" style="width: 80px;"></el-select>
                </div>
                <div class="s-title">
                    制定机关
                </div>
                <div class="selectvie">
                    <el-input v-model="input" style="width: 200px" placeholder="Please input" />
                    <el-button plain @click="">从列表选择</el-button>
                    <el-button :icon="Plus" circle style="border-width: 0;" />
                </div>
            </div>

            <div class="searchItem">
                <div class="s-logic">
                    <el-select v-model="value" placeholder="并且" size="medium" style="width: 80px;"></el-select>
                </div>
                <div class="s-title">
                    公布日期
                </div>
                <div class="selectvie">
                    <el-date-picker
                        v-model="value2"
                        type="datetimerange"
                        start-placeholder="Start date"
                        end-placeholder="End date"
                        format="YYYY-MM-DD HH:mm:ss"
                        date-format="YYYY/MM/DD ddd"
                        time-format="A hh:mm:ss"
                    />
                    <el-button :icon="Plus" circle style="border-width: 0;" />
                </div>
            </div>

            <div class="searchItem">
                <div class="s-logic">
                    <el-select v-model="value" placeholder="并且" size="medium" style="width: 80px;"></el-select>
                </div>
                <div class="s-title">
                    效力位阶
                </div>
                <div class="selectvie">
                    <el-input v-model="input" style="width: 200px" placeholder="Please input" />
                    <el-button plain @click="">从列表选择</el-button>
                    <el-button :icon="Plus" circle style="border-width: 0;" />
                </div>
            </div>
        </div>
        <div class="buttonGroup">
            <el-button>提交</el-button>
            <el-button>取消</el-button>
        </div>
    </div>
    
</template>

<style scoped>
.root {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.searchBox {
    width: 100%;
    margin: 20px;
    border-width: 2px;
    border-color: black;
}


.searchItem {
display: grid;
grid-template-columns: 80px 80px 1fr;
}

</style>