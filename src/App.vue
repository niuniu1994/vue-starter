<template>
  <div>
    <h1>Participants list ({{participants.length}})</h1>
    <participants-list :list="participants"></participants-list>

    <h3>New participant</h3>
      <new-participant-form @added="addNewParticipant($event)"> </new-participant-form>
    
  </div>
</template>

<script>
    import NewParticipantForm from "./NewParticipantForm";
    import ParticipantsList from "./ParticipantsList";
  export default {
    components:{NewParticipantForm,ParticipantsList},
    data() {
      return {
        participants:[],
      };
    },
    methods: {
      addNewParticipant(newParticipant) {
          this.participants.push(newParticipant);
      }
    }
  };
</script>