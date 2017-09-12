<style>
    .ivu-progress-outer {
        padding-left: 35px;
    }
</style>
<template>
<div>
    <Button @click="modal2 = true">自定义页头和页脚</Button>
    <Modal v-model="modal2" width="360">
        <p slot="header" style="text-align:center">
            <span>{{progress<100?'正在生成数据...':'生成数据完成'}}</span>
        </p>
        <Progress :percent="100"></Progress>
        <div slot="footer">
            <Button type="primary" size="small" @click="del">确定</Button>
        </div>
    </Modal>
    </div>
</template>
<script>
    export default {
        data () {
            return {
                modal2: false,
                progress: 0
            }
        },
        methods: {
            del () {
                this.modal2 = false
            }
        }
    }
</script>
