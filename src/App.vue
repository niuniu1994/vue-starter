<template>
  <div>
    <h1>{{ title }}</h1>
    <button @click="iAmClicked()">Click me!</button>
  </div>
</template>

<script>
  let num = 0;
    export default {
        data() {
            return {title: 'Not clicked yet'}
        },
        methods: {
            iAmClicked() {
                this.onclick = num++;
                this.title = 'Clicked '+ num +' times';
            }
        }
    };
</script>
