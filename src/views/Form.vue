<template>
    <div class="mt-5">
        <h1>Formularios</h1>
        <form>
            <b-row>
                <b-col md="3">
                    <!--<b-form-input type="text" v-model="text" :state="true"></b-form-input>-->
                    <b-form-input type="text" v-model="text" :state="comprobar"></b-form-input>
                    <small>Minimo 3 caracteres</small>
                </b-col>
                <b-col md="3">
                  <b-form-select v-model="select" :options="animales"></b-form-select>
                  <p>seleccion: {{select}}</p>
                </b-col>
                <b-col md="3">
                  <b-form-radio-group v-model="radio" :options="animalesRadio"></b-form-radio-group>
                  <p>Radio: {{radio}}</p>
                </b-col>
                <b-col md="3">
                  <b-form-checkbox-group v-model="check" :options="animalesRadio"></b-form-checkbox-group>
                  <p>Multiple: {{check}} </p>
                  <ul><li v-for="(item, index) in check" :key="index">{{item}}</li></ul>
                </b-col>
            </b-row>
        </form>
        <p>text: {{text}}</p>
    </div>
</template>

<script>
export default {
  name: 'Form',
  data () {
    return {
      text: '',
      radio: null,
      select: null,
      check: [],
      animales: [
        { value: null, text: 'Seleccione un animal' },
        { value: 'perro', text: 'Guau guau' },
        { value: 'gato', text: 'Miau' },
        { value: 'pato', text: 'Cuack' }
      ],
      animalesRadio: [
        { value: 'perro', text: 'Guau guau' },
        { value: 'gato', text: 'Miau' },
        { value: 'pato', text: 'Cuack' }
      ]
    }
  },
  computed: {
    comprobar () {
      return this.text.length > 2
    }
  }
}
</script>
