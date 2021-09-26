<template>
  <div id="app">
     <div class="text-center">
            <h1>Tabla de Usuarios</h1>
        </div>
        <table class="table table-hover">
            <thead>
              <tr>
                <th scope="col">#</th>
                <th scope="col">Nombre</th>
                <th scope="col">Apellido</th>
                <th scope="col">Run</th>
                <th scope="col">Nacimiento</th>
                <th scope="col">Edad</th>
              </tr>
            </thead>
            <tbody>
                <tr v-for="(user, index) in users" :key="index">
                    <th>{{index+1}}</th>
                    <td>{{user.nombre}}</td>
                    <td>{{user.apellido}}</td>
                    <td>{{user.run}}</td>
                    <td>{{user.fecha_nacimiento}}</td>
                    <td>{{user.edad}}</td>
                </tr>
            </tbody>
          </table>
  </div>
</template>

<script>

export default {
  name: 'App',
  data: () => {
    let result = { users: [ { nombre: 'Luis', apellido: 'Vallejos', run: '12345678-k', fecha_nacimiento: '07-05-1980', edad: '40'},
                            { nombre: 'Juan', apellido: 'Perez', run: '17513571-1', fecha_nacimiento: '08-06-1985', edad: '36'},
                            { nombre: 'Claudio', apellido: 'Bravo', run: '18753456-2', fecha_nacimiento: '07-08-1990', edad: '32'},
                          ]
    }
    return  result
  }
}
</script>

<style>
</style>
