<script setup>
</script>

<template>
    <div>
        <form @submit.prevent="">
            <div class="input-wrapper">
                <label for="name-input">Create a new team</label>
                <input
                id="name-input"
                type="text"
                placeholder="Enter the Team Name"
                ref="teamInput"
                />
                <input 
                type="submit"
                class="submit"
                value="Submit Team"
                @click="inputShout"
                >
            </div>
        </form>
    </div>

    <b>{{teamName}}</b>
</template>

<script>
export default{
    props: {

    },
    data() {
        return{
            teamName: "",
            formSubmitted: false           
        };
    },
    methods: {
        submitForm: function () {
            this.formSubmitted = false
        },
        inputShout: function () {
            const message = this.$refs.teamInput.value;
            this.teamName = `${message}`; 
        }
    }
}
</script>