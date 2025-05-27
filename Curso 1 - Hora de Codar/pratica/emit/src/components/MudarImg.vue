<template>
    <div>
        <button @click="$emit('trocarImg')">Trocar imagem de perfil</button>
    </div>
</template>

<script>
    export default {
        name: "MudarImg",
        emits: ["trocarImg"]
    }
</script>