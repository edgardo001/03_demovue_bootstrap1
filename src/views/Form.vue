<template>
    <div class="mt-5">
        <h1>Formularios</h1>
        <form>
            <b-row>
                <b-col md="6">
                    <!--<b-form-input type="text" v-model="text" :state="true"></b-form-input>-->
                    <b-form-input type="text" v-model="text" :state="comprobar"></b-form-input>
                    <small>Minimo 3 caracteres</small>
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
      text: ''
    }
  },
  computed: {
    comprobar () {
      return this.text.length > 2
    }
  }
}
</script>
