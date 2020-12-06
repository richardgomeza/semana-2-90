<template>
    <div id="Team-Card">
        
            <div class="card text-white bg-danger">
                <div class="d-flex justify-content-center p-2">
                    <img v-bind:src="member.imagen" alt="Fotografia del equipo" width="200px" height="200px">
                </div>
                <div class="card-body">
                    <h5 class="card-title">{{ member.Nombre }}</h5>
                    <p class="card-text">{{"Codigo"}} - {{member.codigo}}</p>
                    <p class="card-text">{{member.descripcion}}</p>
                    <p class="card-text">{{member.rol}}</p>
                </div>
                <div class="card-footer bg-white">
                    <small class="text-muted">Activo hace 5 minutos.</small>
                </div>
            </div>
        
    </div>
</template>

<script>
    export default {
        name: "TeamCard",
        props: ['member']
    }
</script>

<style scoped>

</style>
