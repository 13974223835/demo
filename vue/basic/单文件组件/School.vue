<template>
                <div class="demo">
                    <h2>学校名称：{{schoolName}}</h2>
                    <h2>学校地址：{{address}}</h2>    
                    <button @click="showName">点我提示学校</button>
                </div>
</template>

<script>
// 组件交互相关的代码（数据，方法等等）
// 简写export default {}
export default Vue.extend({
            name:'School',
            data(){
                return {
                    schoolName:'一中',
                    address:'北京',
                }
            },
            methods:{
                showName(){
                    alert(this.schoolName)
                }
            }
        })

    //  交互需要暴露出去：
    //     1：export const school = Vue.extend({})叫分别暴露  写法import {??} from ??
    //     2:export{school}叫统一暴露  写法import {??} from ??
    //     3：export default school 叫默认暴露，写法import ?? from ??

</script>

<style>
/* 组件的样式 */
    .demo{
        background-color: brown;
    }
</style>