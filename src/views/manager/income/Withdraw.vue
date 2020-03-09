<template>
    <div class="withdraw">
        <briup-fulllayout title="提现申请" @back="backHandler">

        </briup-fulllayout>
    </div>
</template>

<script>
export default {
    data() {
        return {

        }
    },
    computed: {

    },
    created() {

    },
    methods: {
        // 返回到我的页面
        backHandler(){
            this.$router.push({path:'./income_list'})
        }
    }
}
</script>