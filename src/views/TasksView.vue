<template>
  <v-container grid-list-xl>
    <v-layout row wrap>
      <v-flex md6>
        <v-card class="mb-3" v-for="(item, index) in listTasks" :key="index">
          <v-card-text>
            <v-chip label color="blue" text-color="white" class="ml-0">
                <v-icon left>
                        mdi-heart
                </v-icon>
                {{ item.title }}
            </v-chip>
              <p>{{ item.text }}</p>
              <v-btn @click="formUpdate(index)" color="warning" class="ml-0">Editar</v-btn>
              <v-btn @click="deleteTask(item.id)" color="error">Eliminar</v-btn>
          </v-card-text>
        </v-card>
      </v-flex>

      <v-flex md6 v-if="formAdd">
        <v-card class="mb-3 pa-3">
            <v-form @submit.prevent="addTask">
                <v-text-field label="Titulo de tarea" v-model="title"></v-text-field>
                <v-textarea label="Descripción" v-model="text"></v-textarea>
                <v-btn block class="success" type="submit">Agregar</v-btn>
            </v-form>
        </v-card>
      </v-flex>

      <v-flex md6 v-if="!formAdd">
        <v-card class="mb-3 pa-3">
            <v-form @submit.prevent="updateTask">
                <v-text-field label="Titulo de tarea" v-model="title"></v-text-field>
                <v-textarea label="Descripción" v-model="text"></v-textarea>
                <v-btn block class="warning" type="submit">Editar</v-btn>
            </v-form>
        </v-card>
      </v-flex>

    </v-layout>

    <v-snackbar
      v-model="snackbar"
    >
      {{ message }}

      <template v-slot:action="{ attrs }">
        <v-btn
          color="pink"
          text
          v-bind="attrs"
          @click="snackbar = false"
        >
          Close
        </v-btn>
      </template>
    </v-snackbar>

  </v-container>
</template>


<script>
export default {
    data() {
        return {
            listTasks: [
                {
                    id: 1,
                    title: 'Tarea #1',
                    text: `Lorem ipsum, dolor sit amet consectetur adipisicing elit. Facere
                    id sequi, distinctio consectetur et quasi rerum hic ducimus amet,
                    sapiente mollitia atque officiis neque perferendis, ab adipisci
                    sint totam vitae`
                },
                {
                    id: 2,
                    title: 'Tarea #2',
                    text: `Lorem ipsum, dolor sit amet consectetur adipisicing elit. Facere
                    id sequi, distinctio consectetur et quasi rerum hic ducimus amet,
                    sapiente mollitia atque officiis neque perferendis, ab adipisci
                    sint totam vitae`
                }
            ],

            title: '',
            text: '',
            snackbar: false,
            message: '',
            formAdd: true,
            indexTask: ''
        }
    },

    methods: {
        addTask() {

            if(this.title === '' || this.text === '') {
                this.snackbar = true
                this.message = 'Llena todos los campos!'
            }else {
                this.listTasks.push({
                    id: Date.now(),
                    title: this.title,
                    text: this.text
                });

                this.title = ''
                this.text = ''
                this.snackbar = true
                this.message = 'Tarea agregada!'
            }
        },

        deleteTask(id) {
            this.listTasks = this.listTasks.filter(e => e.id != id);
        },

        formUpdate(index) {
            this.formAdd = false
            this.title = this.listTasks[index].title
            this.text = this.listTasks[index].text
            this.indexTask = index
        },

        updateTask() {
            this.listTasks[this.indexTask].title = this.title
            this.listTasks[this.indexTask].text = this.text
            this.formAdd = true
            this.title = ''
            this.text = ''
            this.snackbar = true
            this.message = 'Se actualizó la tarea exitosamente'
        }
    }
}
</script>