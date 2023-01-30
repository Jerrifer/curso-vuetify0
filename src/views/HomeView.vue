<template>
  <v-container grid-list-md>
    <v-layout row wrap>

      <v-flex xs12 sm6>

        <v-card>
          <v-img
            src="https://cdn.pixabay.com/photo/2020/07/12/07/47/bee-5396362_1280.jpg"
          ></v-img>
          <v-card-title>
            <h2>Titulo</h2>
          </v-card-title>
          <v-card-text>
            <p>
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quod
              maiores ad eaque laboriosam expedita dolore, voluptate sequi id
              nihil veniam, illo veritatis eos asperiores? Reprehenderit odit
              itaque earum deserunt rem?
            </p>
          </v-card-text>
          <v-card-actions>
            <v-btn color="info" text>
              Acción
            </v-btn>
          </v-card-actions>
        </v-card>
        
      </v-flex>

      <v-flex xs12 sm6>

        <v-card>
          <v-img
            src="https://cdn.pixabay.com/photo/2020/07/12/07/47/bee-5396362_1280.jpg"
          >
          <v-container >
            <v-layout>
              <v-flex>
                <span class="headline white--text">Lorem, ipsum dolor.</span>
              </v-flex>
            </v-layout>
          </v-container>
        </v-img>
          <v-card-title>
            <h2>Titulo</h2>
          </v-card-title>
          <v-card-text>
            <p>
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quod
              maiores ad eaque laboriosam expedita dolore, voluptate sequi id
              nihil veniam, illo veritatis eos asperiores? Reprehenderit odit
              itaque earum deserunt rem?
            </p>
          </v-card-text>
          <v-card-actions>
            <v-btn color="info" text  @click="dialog = !dialog">
              Acción
            </v-btn>
          </v-card-actions>
        </v-card>

        </v-flex>

    </v-layout>

    <v-dialog v-model="dialog" width="500" persistent>
      <v-card>
          <v-card-title>
            <h2>Titulo</h2>
          </v-card-title>
          <v-card-text>
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quod
              maiores ad eaque laboriosam expedita dolore, voluptate sequi id
              nihil veniam, illo veritatis eos asperiores? Reprehenderit odit
              itaque earum deserunt rem?
          </v-card-text>
          <v-divider></v-divider>
          <v-card-actions>
            <v-btn color="danger" text @click="dialog = false">
              Cerrar
            </v-btn>
          </v-card-actions>
      </v-card>
    </v-dialog>

  </v-container>
</template>


<script>
export default {
  data() {
    return {
    dialog: false
    }
  }
}
</script>