<template>
    <div>
        <form @submit.prevent="addNewParticipant()">
            <label>Firstname</label>
            <input type="text" v-model="newParticipant.name">
            <label>Lastname</label>
            <input type="text" v-model="newParticipant.surname">
            <button>Add new participant</button>
        </form>
    </div>
</template>

<script>
    export default {
        data() {
            return {newParticipant: {}};
        },
        methods: {
            addNewParticipant() {
                this.$emit('added', this.newParticipant);
                this.newParticipant = {};
            }
        }
    };
</script>