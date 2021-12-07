<template>
  <v-app>
    <div class="fondo-p" color="ffff">
      <div>
        <v-app-bar color="#079329" dense dark height="75">
          <router-link
            :to="{ name: 'inicio' }"
            class="noneline"
            style="text-decoration: none; color: inherit; fon"
          >
            <img src="@/assets/bank-finance.png" alt="" srcset="" />
          </router-link>
          <!-- Titulo -->
          <router-link
            :to="{ name: 'inicio' }"
            class="noneline"
            style="text-decoration: none; color: inherit"
          >
            <h2 class="fuente ml-7" style="color: rgb(247, 252, 252)">
              Sistema financiero colombiano
            </h2>
          </router-link>
        </v-app-bar>
      </div>
      
      <!-- Fondo -->
      <div class="fondo-p">
        <!-- parallax controla el espeacio de imagen -->
        <v-parallax dark src="@/assets/1.jpg" height="900" width="auto" class="fondo-p">
          <!-- Contenedor -->
          <v-container fluid>
            <v-row class="mt-0">
              <v-col cols="2">
                
                
                <!-- Primer boton -->
                <v-row>
                  <v-card class="mb-3">
                    <router-link :to="{ name: 'contenido' }">
                      <v-btn elevation="12" class="primary" x-large width="180">
                        <v-icon left color="yellow" class="mr-4" large>
                          fas fa-sticky-note
                        </v-icon>
                        <h4 class="mr-2">CONTENIDO</h4>
                      </v-btn>
                    </router-link>
                  </v-card>
                </v-row>
                
                
                <!-- Segundo boton -->
                <v-row>
                  <v-card class="mb-3">
                    <router-link :to="{ name: 'actividades' }">
                      <v-btn class="primary" elevation="12" x-large width="180">
                        <v-icon left color="yellow" class="ml-2" large>
                          import_contacts
                        </v-icon>
                        <h4 class="ml-3">ACTIVIDADES</h4>
                      </v-btn>
                    </router-link>
                  </v-card>
                </v-row>
                
                
                <!-- Tercer boton -->
                <v-row>
                  <v-card class="mb-3">
                    <router-link :to="{ name: 'evaluacion' }">
                      <v-btn class="primary" elevation="12" x-large width="180">
                        <v-icon left color="yellow" class="mr-2" large>
                          rule
                        </v-icon>
                        <h4 class="ml-1">EVALUACIÓN</h4>
                      </v-btn>
                    </router-link>
                  </v-card>
                </v-row>
                
                
                <!-- Cuarto boton -->
                <v-row>
                  <router-link :to="{ name: 'creditos' }">
                    <v-btn class="primary" elevation="12" x-large width="180">
                      <v-icon left color="yellow" class="mr-5" large>
                        groups
                      </v-icon>
                      <h4>CREDITOS</h4>
                    </v-btn>
                  </router-link>
                </v-row>
              
              
              </v-col>

              <!-- Final -->
              <v-row>
                <v-col aling="left" justific="center">
                  <v-main
                    color="rgb(255, 0, 0, 0.2)"
                    style="border: 0px solid powderblue"
                    class="fondo"
                    
                  >
                    <!-- router-view -->
                    <router-view></router-view>
                  </v-main>
                </v-col>
              </v-row>
            </v-row>
          </v-container>
        </v-parallax>
      </div>
    </div>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    //
  }),
};
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Lora:ital@1&display=swap");
h2 {
  font-family: "Lora", serif;
  font-size: 40px;
}

.fondo-p {
  height: auto;
  width: auto;
  background-color: rgb(7, 8, 31);
}
.degrade {
  background: radial-gradient(200px top, ellipse, white, #1162ac, black);
}

#alpha {
  background-color: rgba(200, 208, 231, 0.5);
  height: 2em;
  width: 150px;
  position: absolute;
  top: 10px;
  color: #fff;
  text-align: center;
  padding-top: 1em;
}
.fondo {
  background-color: rgba(0, 0, 0, 0.5);
  color: #fff;
  border-radius: 2rem;
}
</style>