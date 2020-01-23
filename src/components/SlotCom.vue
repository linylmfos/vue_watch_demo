<template>
  <div id="root_slot">
    <div>
        <h4>案例1： slot基本用法--v-slot可简写为#</h4>
      <Test>
        <template #header="{user}">
          <div>自定义header {{user.a}}</div>
        </template>
        <template v-slot="{user}">
          <div>自定义body {{user.b}}</div>
        </template>
      </Test>
    </div>

    <div>
        <div>案例2： Vue2.6新特性 --动态slot</div>
        <Test>
            <template v-slot:[section]="{section}">
                <div>this is {{section}}</div>
            </template>
        </Test>
        <button @click="change">switch header and body</button>
    </div>

  </div>
</template>

<script>
import Test from "./Test";
export default {
    components: {
        Test
    },
    data() {
        return {section: 'header'}
    },
    methods: {
        change() {
            this.section === 'header' ? this.section = 'default' :
            this.section = 'header'
        }
    }
};
</script>  