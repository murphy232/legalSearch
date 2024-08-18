

<template>
    <div class="root">
        <div class="searchBox">

            <div class="searchItem">
                <div class="s-logic"></div>
                <div class="s-title">标题</div>
                <div class="selective">
                    <el-input v-model="input" placeholder="最多3个词语，用空格分词" />
                    <el-select v-model="textLogic" placeholder="并且" size="medium">
                        <el-option v-for="item in options"
                            :key="item.value"
                            :label="item.label"
                            :value="item.value"
                        />
                    </el-select>
                    <el-input v-model="input" placeholder="最多3个词语，用空格分词" />
                </div>
                <div class="add">
                    <el-button :icon="Plus" circle style="border-width: 0;" />
                </div>
                
            </div>
            <div class="searchItem">
                <div class="s-logic">
                    <el-select v-model="value" placeholder="并且" size="medium" ></el-select>
                </div>
                <div class="s-title">全文</div>
                <div class="selective">
                    <el-input v-model="input"  placeholder="最多3个词语，用空格分词" />
                    <el-select v-model="value" placeholder="并且" size="medium"></el-select>
                    <el-input v-model="input"  placeholder="最多3个词语，用空格分词" />
                    <el-select placeholder="同篇" size="medium" ></el-select>
                </div>
                <div class="add"><el-button :icon="Plus" circle style="border-width: 0;" @click="onClick" /></div>
            </div>

            <div class="searchItem">
                <div class="s-logic">
                    <el-select v-model="value" placeholder="并且" size="medium" ></el-select>
                </div>
                <div class="s-title">
                    制定机关
                </div>
                <div class="selective">
                    <el-input v-model="input" placeholder="最多5个词语，词语词之间使用 或 的关系" />
                    <el-button plain @click="">从列表选择</el-button>
                    
                </div>
                <div class="add"><el-button :icon="Plus" circle style="border-width: 0;" /></div>
            </div>

            <div class="searchItem">
                <div class="s-logic">
                    <el-select v-model="value" placeholder="并且" size="medium" ></el-select>
                </div>
                <div class="s-title">
                    公布日期
                </div>
                <div class="selective">
                    <el-date-picker
                        v-model="value2"
                        type="datetimerange"
                        start-placeholder="请选择开始日期"
                        end-placeholder="请选择结束日期"
                        format="YYYY-MM-DD HH:mm:ss"
                        date-format="YYYY/MM/DD ddd"
                        time-format="A hh:mm:ss"
                    />
                </div>
                <div class="add"><el-button :icon="Plus" circle style="border-width: 0;" /></div>
            </div>

            <div class="searchItem">
                <div class="s-logic">
                    <el-select v-model="value" placeholder="并且" size="medium" ></el-select>
                </div>
                <div class="s-title">
                    效力位阶
                </div>
                <div class="selective">
                    <el-input v-model="input" placeholder="最多5个词语，词语词之间使用 或 的关系" />
                    <el-button plain @click="">从列表选择</el-button>
                    </div>
                <div class="add"><el-button :icon="Plus" circle style="border-width: 0;" /></div>
            </div>
        </div>
        <div class="buttonGroup">
            <el-button>提交</el-button>
            <el-button>取消</el-button>
        </div>
    </div>
    
</template>


<script setup>
import { ref } from 'vue'
import { Plus } from '@element-plus/icons-vue'
const value2 = ref('')
const textLogic = ref('')
const options = [
    {
        value:'and',
        label:'并且'
    },
    {
        value:'or',
        label:'或者'
    },
    {
        value:'not',
        label:'不包含'
    }
]
function onClick(){
    console.log('clicked')
}

</script>

<style lang="less" scoped>
.root {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}



.searchBox {
    width: 80%;
    margin: 20px;
    border-width: 2px;
}

.searchItem {
    display: grid;
    grid-template-columns: 80px 80px 1fr 40px;
    .s-title, .add, .s-logic {
    display: flex;
    justify-content: center;
    align-items: center;
}
}


.selective {
    display: flex;
    border: 1px solid #DCDFE6;
    border-radius: 4px;
    .el-select {
        width: 240px;
    }
    margin-top: 5px;
    margin-bottom: 5px;
    
    
}


:deep(.el-select__wrapper){
  background-color: #218FC4;
  color: #ffffff;
  border: none;
  box-shadow: none;
  --el-text-color-placeholder:#ffffff;
  --el-input-text-color:#ffffff;
  --el-select-input-color:#ffffff
}

:deep(.el-select){
    --el-select-input-focus-border-color: #ffffff;
}

:deep(.el-input){
    --el-input-border-color: #ffffff;
    --el-input-hover-border-color:#ffffff;
    --el-input-focus-border-color: #ffffff;
}
:deep(.el-date-editor){
    --el-input-border-color: #ffffff;
    --el-input-hover-border-color:#ffffff;
    --el-input-focus-border-color: #ffffff;
}
</style>