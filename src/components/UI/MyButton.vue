<script>
export default {

}
</script>

<template>
    <button>
        <slot></slot>
    </button>
</template>

<style scoped>
button {
    color: #21E6C1;
    border: 1px solid #21E6C1;
    padding: 12px;
    background: transparent;
    font-weight: 500;
    cursor: pointer;
    transition: 0.4s ease;
}
button:hover {
    background: #21E6C1;
    color: #071E3D;
}
</style>