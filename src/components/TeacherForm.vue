<template>
  <section>
    <h3>Añadir Profesor</h3>
    <div><label>Nombre: </label><input tabindex="text" v-model="teacher.teacherName"/></div>
    <div><label>Apellidos: </label><input tabindex="text" v-model="teacher.surname"/></div>
    <div><label>DNI / NIF: </label><input tabindex="text" v-model="teacher.dni"/></div>
    <div><label>Materias: </label><input tabindex="text" v-model="subject"/><button>Agregar</button></div>
    <input type="checkbox" v-model="teacher.doc"> Documentación entregada
    
    <button>Agregar</button>
  </section>
  <section>
    <h3>Listado de profesores</h3>
  </section>
</template>

<script lang="ts" setup>
    import { Ref, ref } from 'vue'

    interface ITeacher {
        teacherName: string,
        surname: string,
        dni: string,
        subjects: Array<string>,
        doc: boolean
    }

    let teacher:Ref<ITeacher> = ref({
        teacherName: '',
        surname: '',
        dni: '',
        subjects: [],
        doc: false
    })

    let teachers:Ref<Array<ITeacher>> = ref([])

    let subject: Ref<string> = ref('')
</script>

<style scoped>
</style>