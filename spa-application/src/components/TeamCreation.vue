<script setup>
import Vue from 'vue'
const VueFormulate = require('@braid/vue-formulate')
Vue.use(VueFormulate.default)


</script>
<template>
    <FormulateForm
        class="login-form"
        v-model = "formValues"
    >
        <h2 class="form-title">Create</h2>
        <p>
            Here it is possible to create a new Team
        </p>
        <FormulateInput
            name="name"
            type="text"
            label="Team Name"
        />
        <FormulateInput
            type="submit"
            label="Create"
        />
        <pre
            class="code"
            v-text="formValues"
        />
    </FormulateForm>
</template>

<script>
export default {
    data() {
        return {
            formValues: {}
        }
    },
}
</script>