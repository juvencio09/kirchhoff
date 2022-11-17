<template>
  <v-container class="main-container">
        <video-background
          :src="require('@/assets/videos/fondo1.gif')"
          :poster="require('@/assets/videos/fondo1.gif')"
          class="vid"
          >

          <v-card color='rgba(175, 130, 221, 0.5)' class="card-main">
              <v-row>
                <div class="div-img-cir">
                  <!--  imagen del circuito, dependiendo de la seleccion del usuario  -->
                  <v-img v-if="imgCir === 'caso1'" class="img-cir" src='../assets/img/caso1.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso2'" class="img-cir" src='../assets/img/caso2.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso3'" class="img-cir" src='../assets/img/caso3.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso4'" class="img-cir" src='../assets/img/caso4.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso5'" class="img-cir" src='../assets/img/caso5.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso6'" class="img-cir" src='../assets/img/caso6.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso7'" class="img-cir" src='../assets/img/caso7.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso8'" class="img-cir" src='../assets/img/caso8.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso9'" class="img-cir" src='../assets/img/caso9.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso10'" class="img-cir" src='../assets/img/caso10.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso11'" class="img-cir" src='../assets/img/caso11.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso12'" class="img-cir" src='../assets/img/caso12.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso13'" class="img-cir" src='../assets/img/caso13.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso14'" class="img-cir" src='../assets/img/caso14.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso15'" class="img-cir" src='../assets/img/caso15.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso16'" class="img-cir" src='../assets/img/caso16.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso17'" class="img-cir" src='../assets/img/caso17.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso18'" class="img-cir" src='../assets/img/caso18.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso19'" class="img-cir" src='../assets/img/caso19.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso20'" class="img-cir" src='../assets/img/caso20.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso21'" class="img-cir" src='../assets/img/caso21.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso22'" class="img-cir" src='../assets/img/caso22.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso23'" class="img-cir" src='../assets/img/caso23.jpeg' alt=""></v-img>
                  <v-img v-if="imgCir === 'caso24'" class="img-cir" src='../assets/img/caso24.jpeg' alt=""></v-img>

                  <!--  botones de control de usuario  -->
                  <!-- i1 -->
                  <button v-if="i1 === true" class="btn-i1" @click="change('i1')">
                    <v-icon class='icon-i1' size="50" color="#222222">{{ icons.mdiArrowRightBold }}</v-icon>
                  </button>
                  <button v-if="i1 === false" class="btn-i1" style='transform: scaleX(-1);' @click="change('i1')">
                    <v-icon class='icon-i1' size="50" color="#222222">{{ icons.mdiArrowRightBold }}</v-icon>
                  </button>
                  <!-- i2 -->
                   <button v-if="i2 === true" class="btn-i2" @click="change('i2')">
                    <v-icon class='icon-i1' size="50" color="#222222">{{ icons.mdiArrowRightBold }}</v-icon>
                  </button>
                  <button v-if="i2 === false" class="btn-i2" style='transform: scaleX(-1);' @click="change('i2')">
                    <v-icon class='icon-i1' size="50" color="#222222">{{ icons.mdiArrowRightBold }}</v-icon>
                  </button>
                  <!-- i3 -->
                   <button v-if="i3 === true" class="btn-i3" @click="change('i3')">
                    <v-icon class='icon-i1' size="50" color="#222222">{{ icons.mdiArrowUpBold }}</v-icon>
                  </button>
                  <button v-if="i3 === false" class="btn-i3" @click="change('i3')">
                    <v-icon class='icon-i1' size="50" color="#222222">{{ icons.mdiArrowDownBold }}</v-icon>
                  </button>
                  <!-- m1 -->
                   <button v-if="m1 === true" class="btn-m1" style='transform: scaleX(-1);' @click="change('m1')">
                    <v-icon class='icon-i1' size="50" color="#7502ea">{{ icons.mdiRedoVariant }}</v-icon>
                  </button>
                  <button v-if="m1 === false" class="btn-m1" @click="change('m1')">
                    <v-icon class='icon-i1' size="50" color="#7502ea">{{ icons.mdiRedoVariant }}</v-icon>
                  </button>
                  <!-- m2 -->
                   <button v-if="m2 === true" class="btn-m2" style='transform: scaleX(-1);' @click="change('m2')">
                    <v-icon class='icon-i1' size="50" color="#7502ea">{{ icons.mdiRedoVariant }}</v-icon>
                  </button>
                  <button v-if="m2 === false" class="btn-m2" @click="change('m2')">
                    <v-icon class='icon-i1' size="50" color="#7502ea">{{ icons.mdiRedoVariant }}</v-icon>
                  </button>
                  <v-alert
                    type="warning"
                    v-model="flagAlert"
                  >No se puede mover</v-alert>
                </div>
              </v-row>
              <v-row>
                <div class="card-res">
                  <v-row justify="center">
                    <h3 class="title-res">Resistencias</h3>
                  </v-row>
                  <v-row>
                    <v-col cols="4">
                      <v-row>
                        <span class="title-first-column">R1</span>
                      </v-row>
                      <v-row>
                      <input class="select-first-column" v-model="R1" type="number" min="0"/>
                        <v-icon class='icon-input-first-column' size="30" color="#7502ea">{{ icons.mdiRelationZeroOrOneToZeroOrMany }}</v-icon>
                      </v-row>
                    </v-col>
                    <v-col cols="4">
                      <v-row>
                        <span class="title-first-column">R2</span>
                      </v-row>
                      <v-row>
                      <input class="select-first-column" v-model="R2" type="number" min="0"/>
                        <v-icon class='icon-input-first-column' size="30" color="#7502ea">{{ icons.mdiRelationZeroOrOneToZeroOrMany }}</v-icon>
                      </v-row>
                    </v-col>
                    <v-col cols="4">
                      <v-row>
                        <span class="title-first-column">R3</span>
                      </v-row>
                      <v-row>
                      <input class="select-first-column" v-model="R3" type="number" min="0"/>
                        <v-icon class='icon-input-first-column' size="30" color="#7502ea">{{ icons.mdiRelationZeroOrOneToZeroOrMany }}</v-icon>
                      </v-row>
                    </v-col>
                  </v-row>
                  <v-row justify="center">
                    <p class="text-res">Escribe los valores que gustes asignar a las Resistencias</p>
                  </v-row>
                  <v-row justify="center">
                    <h3 class="title-res">Voltajes</h3>
                  </v-row>
                  <v-row>
                    <v-col cols="6">
                      <v-row>
                        <span class="title-first-column">V1</span>
                      </v-row>
                      <v-row>
                      <input class="select-first-column" v-model="V1" type="number"/>
                        <v-icon class='icon-input-first-column' size="30" color="#7502ea">{{ icons.mdiRelationZeroOrOneToZeroOrMany }}</v-icon>
                      </v-row>
                    </v-col>
                    <v-col cols="6">
                      <v-row>
                        <span class="title-first-column">V2</span>
                      </v-row>
                      <v-row>
                      <input class="select-first-column" v-model="V2" type="number"/>
                        <v-icon class='icon-input-first-column' size="30" color="#7502ea">{{ icons.mdiRelationZeroOrOneToZeroOrMany }}</v-icon>
                      </v-row>
                    </v-col>
                  </v-row>
                  <v-row justify="center">
                    <p class="text-res">Escribe los valores que gustes asignar a las Voltajes</p>
                  </v-row>
                </div>
                <div class="card-answ">
                  <v-row justify="center">
                    <h1 class="title-res-2">Matriz del Circuito</h1>
                  </v-row>
                  <v-row justify="center">
                    <ul style="list-style:none; margin-left: -30px; margin-top: 10px">
                      <li>
                          Ec1: <span class="valorReal">{{ matriz[0][0].valor }}</span><span class="valorCss">{{ matriz[0][0].id }}</span>, <span class="valorReal">{{ matriz[0][1].valor }}</span><span class="valorCss">{{ matriz[0][1].id }}</span>, <span class="valorReal">{{ matriz[0][2].valor }}</span><span class="valorCss">{{ matriz[0][2].id }}</span> = <span class="valorReal">{{ matriz[0][3].valor }}</span><span class="valorCss">{{ matriz[0][3].id }}</span>
                      </li>
                      <li>
                          Ec2: <span class="valorReal">{{ matriz[1][0].valor }}</span><span class="valorCss">{{ matriz[1][0].id }}</span>, <span class="valorReal">{{ matriz[1][1].valor }}</span><span class="valorCss">{{ matriz[1][1].id }}</span>, <span class="valorReal">{{ matriz[1][2].valor }}</span><span class="valorCss">{{ matriz[1][2].id }}</span> = <span class="valorReal">{{ matriz[1][3].valor }}</span><span class="valorCss">{{ matriz[1][3].id }}</span>
                      </li>
                      <li>
                          Ec3: <span class="valorReal">{{ matriz[2][0].valor }}</span><span class="valorCss">{{ matriz[2][0].id }}</span>, <span class="valorReal">{{ matriz[2][1].valor }}</span><span class="valorCss">{{ matriz[2][1].id }}</span>, <span class="valorReal">{{ matriz[2][2].valor }}</span><span class="valorCss">{{ matriz[2][2].id }}</span> = <span class="valorReal">{{ matriz[2][3].valor }}</span><span class="valorCss">{{ matriz[2][3].id }}</span>
                      </li>
                    </ul>
                  </v-row>
                  <v-row justify="center">
                    <h1 class="title-res-2">Procedimiento</h1>
                  </v-row>
                  <v-row justify="center">
                    <h1 class="title-res-3">Paso 1</h1>
                  </v-row>
                  <v-row justify="center">
                    <ul style="list-style:none; margin-left: -30px; margin-top: 10px">
                      <li>
                          Ec1: <span class="valorReal">{{ matriz[0][0].valor * getValMenor() }}</span><span class="valorCss">{{ matriz[0][0].id }}</span>, <span class="valorReal">{{ matriz[0][1].valor * getValMenor() }}</span><span class="valorCss">{{ matriz[0][1].id }}</span>, <span class="valorReal">{{ matriz[0][2].valor * getValMenor() }}</span><span class="valorCss">{{ matriz[0][2].id }}</span> ( {{ getValMenor() }} )
                      </li>
                      <li>
                          Ec2: <span class="valorReal">{{ matriz[1][0].valor }}</span><span class="valorCss">{{ matriz[1][0].id }}</span>, <span class="valorReal">{{ matriz[1][1].valor }}</span><span class="valorCss">{{ matriz[1][1].id }}</span>, <span class="valorReal">{{ matriz[1][2].valor }}</span><span class="valorCss">{{ matriz[1][2].id }}</span>
                      </li>
                      <li>
                          Ec4: <span class="valorReal">{{ matrizPaso1[0][0].valor }}</span><span class="valorCss">{{ matrizPaso1[0][0].id }}</span>, <span class="valorReal">{{ matrizPaso1[0][1].valor }}</span><span class="valorCss">{{ matrizPaso1[0][1].id }}</span>, <span class="valorReal">{{ matrizPaso1[0][2].valor }}</span><span class="valorCss">{{ matrizPaso1[0][2].id }}</span>
                      </li>
                    </ul>
                  </v-row>
                   <v-row justify="center">
                    <h1 class="title-res-3">Paso 2</h1>
                  </v-row>
                  <v-row justify="center">
                    <ul style="list-style:none; margin-left: -10px; margin-top: 10px">
                      <li>
                          Ec2: <span class="valorReal">{{ matriz[1][0].valor * -1}}</span><span class="valorCss">{{ matriz[1][0].id }}</span>, <span class="valorReal">{{ matriz[1][1].valor * -1 }}</span><span class="valorCss">{{ matriz[1][1].id }}</span>, <span class="valorReal">{{ matriz[1][2].valor * -1 }}</span><span class="valorCss">{{ matriz[1][2].id }}</span> ( -1 )
                      </li>
                      <li>
                          Ec3: <span class="valorReal">{{ matriz[2][0].valor }}</span><span class="valorCss">{{ matriz[2][0].id }}</span>, <span class="valorReal">{{ matriz[2][1].valor }}</span><span class="valorCss">{{ matriz[2][1].id }}</span>, <span class="valorReal">{{ matriz[2][2].valor }}</span><span class="valorCss">{{ matriz[2][2].id }}</span>
                      </li>
                      <li>
                          Ec5: <span class="valorReal">{{ matrizPaso2[0][0].valor }}</span><span class="valorCss">{{ matrizPaso2[0][0].id }}</span>, <span class="valorReal">{{ matrizPaso2[0][1].valor }}</span><span class="valorCss">{{ matrizPaso2[0][1].id }}</span>, <span class="valorReal">{{ matrizPaso2[0][2].valor }}</span><span class="valorCss">{{ matrizPaso2[0][2].id }}</span>
                      </li>
                    </ul>
                  </v-row>
                  <v-row justify="center">
                    <h1 class="title-res-3">Paso 3</h1>
                  </v-row>
                  <v-row justify="center">
                    <ul style="list-style:none; margin-left: -10px; margin-top: 10px">
                      <li>
                          Ec4: <span class="valorReal">{{ matrizPaso1[0][0].valor * obtenerDatoMostrar(this.matrizPaso1[0][1].valor,this.matrizPaso2[0][1].valor).a }}</span><span class="valorCss">{{ matrizPaso1[0][0].id }}</span>, <span class="valorReal">{{ matrizPaso1[0][1].valor * obtenerDatoMostrar(this.matrizPaso1[0][1].valor,this.matrizPaso2[0][1].valor).a}}</span><span class="valorCss">{{ matrizPaso1[0][1].id }}</span>, <span class="valorReal">{{ matrizPaso1[0][2].valor * obtenerDatoMostrar(this.matrizPaso1[0][1].valor,this.matrizPaso2[0][1].valor).a }}</span><span class="valorCss">{{ matrizPaso1[0][2].id }}</span> ({{ obtenerDatoMostrar(this.matrizPaso1[0][1].valor,this.matrizPaso2[0][1].valor).a }})
                      </li>
                      <li>
                          Ec5: <span class="valorReal">{{ matrizPaso2[0][0].valor * obtenerDatoMostrar(this.matrizPaso1[0][1].valor,this.matrizPaso2[0][1].valor).b}}</span><span class="valorCss">{{ matrizPaso2[0][0].id }}</span>, <span class="valorReal">{{ matrizPaso2[0][1].valor * obtenerDatoMostrar(this.matrizPaso1[0][1].valor,this.matrizPaso2[0][1].valor).b}}</span><span class="valorCss">{{ matrizPaso2[0][1].id }}</span>, <span class="valorReal">{{ matrizPaso2[0][2].valor * obtenerDatoMostrar(this.matrizPaso1[0][1].valor,this.matrizPaso2[0][1].valor).b}}</span><span class="valorCss">{{ matrizPaso2[0][2].id }}</span> ({{ obtenerDatoMostrar(this.matrizPaso1[0][1].valor,this.matrizPaso2[0][1].valor).b }})
                      </li>
                    </ul>
                  </v-row>
                  <v-row justify="center">
                    <ul style="list-style:none; margin-left: -10px; margin-top: 10px">
                      <li>
                         <span class="valorReal">{{ matrizPaso3[0][0].valor }}</span><span class="valorCss">{{ matrizPaso3[0][0].id }}</span>, <span class="valorReal">{{ matrizPaso3[0][1].valor }}</span><span class="valorCss">{{ matrizPaso3[0][1].id }}</span>, <span class="valorReal">{{ matrizPaso3[0][2].valor }}</span><span class="valorCss">{{ matrizPaso3[0][2].id }}</span>
                      </li>
                    </ul>
                  </v-row>
                  <v-row justify="center">
                    <ul style="list-style:none; margin-left: -10px; margin-top: 10px">
                      <li>
                          <span class="valorCss2">I1: </span><span class="valorReal">{{ ((-matrizPaso3[0][1].valor) / matrizPaso3[0][0].valor).toFixed(4) }}</span> A
                      </li>
                    </ul>
                  </v-row>
                  <v-row justify="center">
                    <h1 class="title-res-3">Paso 4</h1>
                  </v-row>
                  <v-row justify="center">
                    <ul style="list-style:none; margin-left: -10px; margin-top: 10px">
                      <li>
                          Ec4: <span class="valorReal">{{ matrizPaso1[0][0].valor * obtenerDatoMostrar(this.matrizPaso1[0][0].valor,this.matrizPaso2[0][0].valor).a }}</span><span class="valorCss">{{ matrizPaso1[0][0].id }}</span>, <span class="valorReal">{{ matrizPaso1[0][1].valor * obtenerDatoMostrar(this.matrizPaso1[0][0].valor,this.matrizPaso2[0][0].valor).a}}</span><span class="valorCss">{{ matrizPaso1[0][1].id }}</span>, <span class="valorReal">{{ matrizPaso1[0][2].valor * obtenerDatoMostrar(this.matrizPaso1[0][0].valor,this.matrizPaso2[0][0].valor).a }}</span><span class="valorCss">{{ matrizPaso1[0][2].id }}</span> ({{ obtenerDatoMostrar(this.matrizPaso1[0][0].valor,this.matrizPaso2[0][0].valor).a }})
                      </li>
                      <li>
                          Ec5: <span class="valorReal">{{ matrizPaso2[0][0].valor * obtenerDatoMostrar(this.matrizPaso1[0][0].valor,this.matrizPaso2[0][0].valor).b}}</span><span class="valorCss">{{ matrizPaso2[0][0].id }}</span>, <span class="valorReal">{{ matrizPaso2[0][1].valor * obtenerDatoMostrar(this.matrizPaso1[0][0].valor,this.matrizPaso2[0][0].valor).b}}</span><span class="valorCss">{{ matrizPaso2[0][1].id }}</span>, <span class="valorReal">{{ matrizPaso2[0][2].valor * obtenerDatoMostrar(this.matrizPaso1[0][0].valor,this.matrizPaso2[0][0].valor).b}}</span><span class="valorCss">{{ matrizPaso2[0][2].id }}</span> ({{ obtenerDatoMostrar(this.matrizPaso1[0][0].valor,this.matrizPaso2[0][0].valor).b }})
                      </li>
                    </ul>
                  </v-row>
                  <v-row justify="center">
                    <ul style="list-style:none; margin-left: -10px; margin-top: 10px">
                      <li>
                         <span class="valorReal">{{ matrizPaso4[0][0].valor }}</span><span class="valorCss">{{ matrizPaso4[0][0].id }}</span>, <span class="valorReal">{{ matrizPaso4[0][1].valor }}</span><span class="valorCss">{{ matrizPaso3[0][1].id }}</span>, <span class="valorReal">{{ matrizPaso3[0][2].valor }}</span><span class="valorCss">{{ matrizPaso3[0][2].id }}</span>
                      </li>
                    </ul>
                  </v-row>
                  <v-row justify="center">
                    <ul style="list-style:none; margin-left: -10px; margin-top: 10px">
                      <li>
                          <span class="valorCss2">I2: </span><span class="valorReal">{{ claI2() }}</span> A
                      </li>
                    </ul>
                  </v-row>
                  <v-row justify="center">
                    <h1 class="title-res-3">Paso 5</h1>
                  </v-row>
                  <v-row justify="center">_
                    <ul style="list-style:none; margin-left: -10px; margin-top: 10px">
                      <li>
                          Ec1: <span class="valorReal">{{ matriz[0][0].valor }}</span><span class="valorCss">{{ matriz[0][0].id }}</span>, <span class="valorReal">{{ matriz[0][1].valor }}</span><span class="valorCss">{{ matriz[0][1].id }}</span>, <span class="valorReal">{{ matriz[0][2].valor }}</span><span class="valorCss">{{ matriz[0][2].id }}</span>
                      </li>
                    </ul>
                  </v-row>
                  <v-row justify="center">
                    <ul style="list-style:none; margin-left: -10px; margin-top: 10px">
                      <li>
                          <span class="valorReal">{{ matriz[0][0].valor * ((-matrizPaso3[0][1].valor) / matrizPaso3[0][0].valor).toFixed(3) }}</span>, <span class="valorReal">{{ matriz[0][1].valor * ((-matrizPaso4[0][1].valor) / matrizPaso4[0][0].valor).toFixed(3)}}</span>, <span class="valorReal">{{ matriz[0][2].valor }}</span><span class="valorCss">{{ matriz[0][2].id }}</span>
                      </li>
                    </ul>
                  </v-row>
                  <v-row justify="center">
                    <ul style="list-style:none; margin-left: -10px; margin-top: 10px">
                      <li>
                          <span class="valorCss2">I3: </span><span class="valorReal">{{ calI3() }}</span> A
                      </li>
                    </ul>
                  </v-row>
                </div>
              </v-row>
          </v-card>
        </video-background>
  </v-container>
</template>

<script>
  import VideoBackground from 'vue-responsive-video-background-player'
  import { mdiArrowRightBold } from '@mdi/js';
  import { mdiArrowUpBold } from '@mdi/js';
  import { mdiRedoVariant } from '@mdi/js';
  import { mdiArrowDownBold } from '@mdi/js';
  import { mdiRelationZeroOrOneToZeroOrMany } from '@mdi/js';

  export default {
    name: 'HelloWorld',
    components: { VideoBackground },
    data: () => ({
      icons: { mdiArrowRightBold, mdiArrowUpBold, mdiRedoVariant, mdiArrowDownBold, mdiRelationZeroOrOneToZeroOrMany },
      imgCir: 'caso1',
      imgCasoTemp: 'caso1',
      flagAlert: false,
      matrizPaso1: [
         [{valor: 0, id: ''}, {valor: 0, id: ''}, {valor: 0, id: ''}, {valor: 0, id: ''}]
      ],
      matrizPaso2: [
         [{valor: 0, id: ''}, {valor: 0, id: ''}, {valor: 0, id: ''}, {valor: 0, id: ''}]
      ],
      matrizPaso3: [
         [{valor: 0, id: ''}, {valor: 0, id: ''}, {valor: 0, id: ''}, {valor: 0, id: ''}]
      ],
      matrizPaso4: [
         [{valor: 0, id: ''}, {valor: 0, id: ''}, {valor: 0, id: ''}, {valor: 0, id: ''}]
      ],
      matrizPaso5: [
         [{valor: 0, id: ''}, {valor: 0, id: ''}, {valor: 0, id: ''}, {valor: 0, id: ''}]
      ],
      matriz: [
          [{valor: 0, id: ''}, {valor: 0, id: ''}, {valor: 0, id: ''}, {valor: 0, id: ''}],
          [{valor: 0, id: ''}, {valor: 0, id: ''}, {valor: 0, id: ''}, {valor: 0, id: ''}],
          [{valor: 0, id: ''}, {valor: 0, id: ''}, {valor: 0, id: ''}, {valor: 0, id: ''}]
      ],
      i1: false,
      i2: false,
      i3: false,
      m1: true,
      m2: false,
      R1: 12,
      R2: 20,
      R3: 8,
      V1: 25,
      V2: 20
    }),
    mounted() {
        this.reolverCircuiro()
    },
    watch: {
      R1 () {
        this.reolverCircuiro()
      },
      R2 () {
        this.reolverCircuiro()
      },
      R3 () {
        this.reolverCircuiro()
      },
      V1 () {
        this.reolverCircuiro()
      },
      V2 () {
        this.reolverCircuiro()
      },
    },
    methods: {
      checkPhoto () {
        if ( this.i1 === true  && this.i2 === false && this.i3 === false && this.m1 === true  && this.m2 === false)  this.imgCir = 'caso1'
        if ( this.i1 === true  && this.i2 === false && this.i3 === false && this.m1 === true  && this.m2 === true)   this.imgCir = 'caso2'
        if ( this.i1 === true  && this.i2 === false && this.i3 === false && this.m1 === false && this.m2 === false)  this.imgCir = 'caso3'
        if ( this.i1 === true  && this.i2 === false && this.i3 === false && this.m1 === false && this.m2 === true)   this.imgCir = 'caso4'
        if ( this.i1 === true  && this.i2 === true  && this.i3 === false && this.m1 === true  && this.m2 === false)  this.imgCir = 'caso5'
        if ( this.i1 === true  && this.i2 === true  && this.i3 === false && this.m1 === true  && this.m2 === true)   this.imgCir = 'caso6'
        if ( this.i1 === true  && this.i2 === true  && this.i3 === false && this.m1 === false && this.m2 === false)  this.imgCir = 'caso7'
        if ( this.i1 === true  && this.i2 === true  && this.i3 === false && this.m1 === false && this.m2 === true)   this.imgCir = 'caso8'
        if ( this.i1 === false && this.i2 === false && this.i3 === false && this.m1 === true  && this.m2 === false)  this.imgCir = 'caso9'
        if ( this.i1 === false && this.i2 === false && this.i3 === false && this.m1 === true  && this.m2 === true)   this.imgCir = 'caso10'
        if ( this.i1 === false && this.i2 === false && this.i3 === false && this.m1 === false && this.m2 === false)  this.imgCir = 'caso11'
        if ( this.i1 === false && this.i2 === false && this.i3 === false && this.m1 === false && this.m2 === true)   this.imgCir = 'caso12'
        if ( this.i1 === false && this.i2 === true  && this.i3 === true  && this.m1 === true  && this.m2 === false)  this.imgCir = 'caso13'
        if ( this.i1 === false && this.i2 === true  && this.i3 === true  && this.m1 === true  && this.m2 === true)   this.imgCir = 'caso14'
        if ( this.i1 === false && this.i2 === true  && this.i3 === true  && this.m1 === false && this.m2 === false)  this.imgCir = 'caso15'
        if ( this.i1 === false && this.i2 === true  && this.i3 === true  && this.m1 === false && this.m2 === true)   this.imgCir = 'caso16'
        if ( this.i1 === true  && this.i2 === true  && this.i3 === true  && this.m1 === true  && this.m2 === false)  this.imgCir = 'caso17'
        if ( this.i1 === true  && this.i2 === true  && this.i3 === true  && this.m1 === true  && this.m2 === true)   this.imgCir = 'caso18'
        if ( this.i1 === true  && this.i2 === true  && this.i3 === true  && this.m1 === false && this.m2 === false)  this.imgCir = 'caso19'
        if ( this.i1 === true  && this.i2 === true  && this.i3 === true  && this.m1 === false && this.m2 === true)   this.imgCir = 'caso20'
        if ( this.i1 === false && this.i2 === false && this.i3 === true  && this.m1 === true  && this.m2 === false)  this.imgCir = 'caso21'
        if ( this.i1 === false && this.i2 === false && this.i3 === true  && this.m1 === true  && this.m2 === true)  this.imgCir = 'caso22'
        if ( this.i1 === false && this.i2 === false && this.i3 === true  && this.m1 === false && this.m2 === false)  this.imgCir = 'caso23'
        if ( this.i1 === false && this.i2 === false && this.i3 === true  && this.m1 === false && this.m2 === true)   this.imgCir = 'caso24'
        this.reolverCircuiro()
      },
      change (letra) {
        switch (letra) {
          case 'i1':
              this.i1 = !this.i1
              this.checkPhoto()
              if (this.imgCir === this.imgCasoTemp){
                this.flagAlert = true
                this.i1 = !this.i1
              } else {
                this.imgCasoTemp = this.imgCir
                this.flagAlert = false
              }
            break;
          case 'i2':
              this.i2 = !this.i2
              this.checkPhoto()
              if (this.imgCir === this.imgCasoTemp){
                this.flagAlert = true
                this.i2 = !this.i2
              } else {
                this.imgCasoTemp = this.imgCir
                this.flagAlert = false
              }
            break;
          case 'i3':
              this.i3 = !this.i3
              this.checkPhoto()
              if (this.imgCir === this.imgCasoTemp){
                this.flagAlert = true
                this.i3 = !this.i3
              } else {
                this.imgCasoTemp = this.imgCir
                this.flagAlert = false
              }
            break;
            case 'm1':
              this.m1 = !this.m1
              this.checkPhoto()
              this.flagAlert = false
            break;
            case 'm2':
              this.m2 = !this.m2
              this.checkPhoto()
              this.flagAlert = false
            break;
        }
      }, 
      reolverCircuiro () {
        // primer ecuacion
        if (this.i1 !== true) { 
          this.matriz[0][0].valor = -1
          this.matriz[0][0].id = 'i1'
        } else {
          this.matriz[0][0].valor = 1 
          this.matriz[0][0].id = 'i1' 
        }
        if (this.i2 !== true) { 
          this.matriz[0][1].valor = 1 
          this.matriz[0][1].id = 'i2'
        } else {
          this.matriz[0][1].valor = -1 
          this.matriz[0][1].id = 'i2'
        }
        if (this.i3 !== true) { 
          this.matriz[0][2].valor = -1
          this.matriz[0][2].id = 'i3'
        } else {
          this.matriz[0][2].valor = 1  
          this.matriz[0][2].id = 'i3'
        }
        // segunda ecuacion m1
        if (this.m1 === this.i1) {
          this.matriz[1][0].valor = -1 * this.R1
          this.matriz[1][0].id = 'i1'
        } else {
          this.matriz[1][0].valor = this.R1
          this.matriz[1][0].id = 'i1'
        }
        if (this.m1 !== this.i3) {
          this.matriz[1][1].valor = -1 * this.R3
          this.matriz[1][1].id = 'i3'
        } else {
          this.matriz[1][1].valor = this.R3
          this.matriz[1][1].id = 'i3'
        }
        this.matriz[1][2].valor = this.V1
        this.matriz[1][2].id = 'V1'
        // tercera ecuacion m1
        if (this.m1 !== this.i2) {
          this.matriz[2][0].valor = -1 * this.R2
          this.matriz[2][0].id = 'i2'
        } else {
          this.matriz[2][0].valor = this.R2
          this.matriz[2][0].id = 'i2'
        }
        if (this.m1 !== this.i3) {
          this.matriz[2][1].valor = -1 * this.R3
          this.matriz[2][1].id = 'i3'
        } else {
          this.matriz[2][1].valor = this.R3
          this.matriz[2][1].id = 'i3'
        }
        this.matriz[2][2].valor = this.V2
        this.matriz[2][2].id = 'V2'

        // resolvemos los siguientes pasos
        this.resPrimerPaso()
        this.resSegundoPaso()
        this.resTercerPaso()
        this.cuartoTercerPaso()
      },
      getValMenor () {
          return this.matriz[1][1].valor
      },
      resPrimerPaso () {
        this.matrizPaso1[0][0].valor = Number(this.matriz[0][0].valor * this.getValMenor()) + Number(this.matriz[1][0].valor)
        this.matrizPaso1[0][0].id    = 'i1'
        this.matrizPaso1[0][1].valor = this.matriz[0][1].valor * this.getValMenor()
        this.matrizPaso1[0][1].id    = 'i2'
        this.matrizPaso1[0][2].valor = this.matriz[1][2].valor
        this.matrizPaso1[0][2].id    = 'V'
      },
      resSegundoPaso () {
        this.matrizPaso2[0][0].valor = Number(this.matriz[1][0].valor * -1)
        this.matrizPaso2[0][0].id    = 'i1'
        this.matrizPaso2[0][1].valor = this.matriz[2][0].valor
        this.matrizPaso2[0][1].id    = 'i2'
        this.matrizPaso2[0][2].valor = Number((this.matriz[1][2].valor * -1)) + Number(this.matriz[2][2].valor)
        this.matrizPaso2[0][2].id    = 'V'
      },
      resTercerPaso () {
        this.matrizPaso3[0][0].valor = Number(this.matrizPaso1[0][0].valor) * Number(this.obtenerDatoMostrar(this.matrizPaso1[0][1].valor,this.matrizPaso2[0][1].valor).a) + Number(this.matrizPaso2[0][0].valor) * Number(this.obtenerDatoMostrar(this.matrizPaso1[0][1].valor,this.matrizPaso2[0][1].valor).b)
        this.matrizPaso3[0][0].id    = 'i1'
        this.matrizPaso3[0][1].valor = Number(this.matrizPaso1[0][2].valor) * Number(this.obtenerDatoMostrar(this.matrizPaso1[0][1].valor,this.matrizPaso2[0][1].valor).a) + Number(this.matrizPaso2[0][2].valor) * Number(this.obtenerDatoMostrar(this.matrizPaso1[0][1].valor,this.matrizPaso2[0][1].valor).b)
        this.matrizPaso3[0][1].id    = 'V'
        this.matrizPaso3[0][2].valor = 0
        this.matrizPaso3[0][2].id    = 'V'
      },
      cuartoTercerPaso () {
        this.matrizPaso4[0][0].valor = Number(this.matrizPaso1[0][1].valor) * Number(this.obtenerDatoMostrar(this.matrizPaso1[0][0].valor,this.matrizPaso2[0][0].valor).a) + Number(this.matrizPaso2[0][1].valor) * Number(this.obtenerDatoMostrar(this.matrizPaso1[0][0].valor,this.matrizPaso2[0][0].valor).b)
        this.matrizPaso4[0][0].id    = 'i2'
        this.matrizPaso4[0][1].valor = Number(this.matrizPaso1[0][2].valor) * Number(this.obtenerDatoMostrar(this.matrizPaso1[0][0].valor,this.matrizPaso2[0][0].valor).a) + Number(this.matrizPaso2[0][2].valor) * Number(this.obtenerDatoMostrar(this.matrizPaso1[0][0].valor,this.matrizPaso2[0][0].valor).b)
        this.matrizPaso4[0][1].id    = 'V'
        this.matrizPaso4[0][2].valor = 0
        this.matrizPaso4[0][2].id    = 'V'
      },
      maximoComunDivisor (a, b)  {
          let temporal //Para no perder b
          while (b !== 0) {
              temporal = b
              b = a % b
              a = temporal
          }
          return a
      },
      minimoComunMultiplo (a, b) {
        return (a * b) / this.maximoComunDivisor(a, b)
      },
      obtenerDatoMostrar (a, b) {
        const minimo = this.minimoComunMultiplo(a, b)
        const resa = minimo/a
        const resb = minimo/b
        return {a: resa, b: (resb * -1)}
      },
      claI2 () {
        return ((-this.matrizPaso4[0][1].valor) / this.matrizPaso4[0][0].valor).toFixed(4)
      },
      calI3 () {
        return this.matriz[0][0].valor * (((-this.matrizPaso3[0][1].valor) / this.matrizPaso3[0][0].valor) + this.matriz[0][1].valor * ((-this.matrizPaso4[0][1].valor) / this.matrizPaso4[0][0].valor)).toFixed(3)
      }
    }
  }
</script>
<style>
  .container {
    max-width: 100% !important;
  }
  .main-container {
    margin: 0;
    padding: 0;
    width: 100%
  }
  .vid {
    widows: 100%;
    max-height: 1080px;
    min-height: 280vh;
  }
  .card-main {
    margin-left: 10%;
    border-radius: 30px !important;
    top: 8%;
    width: 80%;
    height: calc(280vh - 200px);
  }
  .div-img-cir{
    width: 80%;
    height: 500px;
    margin-left: 11%;
    margin-top: 50px;
    border-radius: 30px;
    background-color: #e6e6e6;
    position: absolute;
  }
  .img-cir{
    width: 600px;
    height: 360px;
    margin: 0 auto;
    margin-top: 65px;
  }
  .btn-i1{
    position: relative;
    top: -400px;
    left: 150px;
  }
  .btn-i2{
    position: relative;
    top: -400px;
    right: -600px;
  }
  .btn-i3{
    position: relative;
    right: -300px;
  }
  .btn-m1{
    position: relative;
    right: -135px;
    top: -180px
  }
  .btn-m2{
    position: relative;
    right: -310px;
    top: -180px
  }
  .card-res {
    width: 50%;
    height: 400px;
    margin-left: 11%;
    margin-top: 600px;
    border-radius: 30px;
    background-color: #e6e6e6;
    position: absolute;
    padding-left: 30px;
    padding-top: 30px;
  }
  .title-res{
    color: #7502ea
  }
  .title-first-column{
    color: #7502ea;
    margin-left: 30%;
    margin-top: 10px
  }
  .select-first-column{
    width: 80%;
    background-color: white;
    color: #7502ea;
    height: 30px;
    border-radius: 10px;
    padding-left: 10px;
    margin-top: 5px
  }
  input:focus{
    box-shadow: 0 1px 1px rgba(229, 103, 23, 0.075)inset, 0 0 8px #7502ea;
    outline: 0 none;
  }
  .icon-input-first-column{
    position: relative;
    right: 40px;
    top: 2px;
  }
  .text-res {
    padding-top: 20px;
    color: #7502ea;
  }
  .card-answ {
    width: 28%;
    height: 1000px;
    margin-left: 63%;
    margin-top: 600px;
    border-radius: 30px;
    background-color: #e6e6e6;
    position: absolute;
    padding-top: 30px;
  }
  .valorCss {
    font-size: 12px;
    color: #7502ea;
  }
  .valorCss2 {
    font-size: 20px;
    color: #7502ea;
  }
  .valorReal {
    font-size: 18px;
  }
  .title-res-2 {
    font-size: 20px;
    padding-top: 20px;
    color: #7502ea;
  }
  .title-res-3 {
    font-size: 15px;
    padding-top: 5px;
    color: #7502ea;
  }

</style>
