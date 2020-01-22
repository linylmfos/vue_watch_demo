<template>
    <div id="roots">
        <div :class="isActive ? 'active' : '' +  'normal'">数组绑定多个class</div>
        <div :class="['active', 'normal']">数组绑定多个class</div>
        <div :class="[{'active': isActive}, 'normal']">数组包含对象 绑定class</div>
        <div :class="[showWarning(), 'normal']">数组包含方法 绑定class</div>
        <div :style="[warning, bold]">数组绑定多个style</div>
        <div :style="[warning, mix()]">数组包含方法绑定style</div>
        <div :style="{ display: ['-webkit-box', '-ms-flexbox', 'flex'] }">style多重值</div>
    </div>
</template> 

<script>
    export default {
        data() {
            return {
                isActive: true,
                warning: {
                    color: 'orange'
                },
                bold: {
                    fontWeight: 'bold'
                }
            }
        },
        methods: {
            showWarning() {
                return 'warning'
            },
            mix() {
                return {
                    ...this.bold,
                    fontSize: 20
                }
            }
        }
    }
</script>  
<style scoped>

</style>   
