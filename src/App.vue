<template>
  <div id="app" class="html">
    <div class="main-container container-fluid">
      <div class="row">
        <section class="col-sm-12">

          <header>
            <img src='./farmOS.png' alt="" style="max-width: 200px; margin: 0.5rem 0">
            <h3 class="page-header">{{headerText}}</h3>
          </header>

          <div class="region region-content">
            <div class="block block-system">

              <router-view/>

            </div>
          </div>

        </section>
      </div>
    </div>
  </div>
</template>

<script>
import { mapState } from 'vuex';
export default {
  name: 'App',
  data () {
    return {

    }
  },
  computed: mapState({
    headerText: state => state.shell.greeting,
  }),
  methods: {

    // I should parse this in an iterative way, cycling through object properties
    saveObservation (obs) {


      this.displayState = 'displayNewObservation'
    },

  }//methods

}
</script>

<style>

</style>