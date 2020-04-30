<template>
    <div>
        <ol>
            <li v-for="person in list">
                {{person.name}} {{person.surname}}
            </li>
        </ol>
    </div>
</template>

<script>
    export default {
        props: ['list']
    };
</script>