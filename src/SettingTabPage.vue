<template>
    <div>
        <button @click="add_one">+1</button>
        <span class="sample-class">{{ count }}</span>
    </div>
    <br />
    <div>
        <n-button @click="add_one">naive-ui</n-button>
    </div>
</template>

<style scoped>
.sample-class {
    margin-left: 1em;
    color: #6C31E3;
}
</style>

<script lang="ts">
import { defineComponent } from "vue";
import { NButton } from "naive-ui";

export default defineComponent({
    name: "SampleSettingTabPage",
    data() {
        return {
            count: 0
        }
    },
    methods: {
        add_one() {
            this.count += 1;
        }
    },
    components: {
        NButton
    }
})
</script>