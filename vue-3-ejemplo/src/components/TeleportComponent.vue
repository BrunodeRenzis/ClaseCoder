<template>
    <teleport to="body">  // Indicamos dónde queremos "teletransportarlo"
        <div class="modal" v-if="modalOpen">
            <h2>Modal title</h2>
            ...
            <button @click="modalOpen = false">Close modal</button>
        </div>
    </teleport>
</template>

<script>
export default {

}
</script>

<style>

</style>
