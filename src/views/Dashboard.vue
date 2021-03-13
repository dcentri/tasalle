<template>
  <div>
    <base-header type="gradient-success" 
    style="
        min-height: 600px;
        background-image: url(img/theme/splash.jpg);
        background-size: cover;
        background-position: center top;"
    class="header pb-8 pt-5 pt-lg-8 d-flex align-items-center">
    
      <!-- Mask -->
      <span class="mask bg-gradient-success opacity-8"></span>
      <div class="row">
        <div class="col-lg-12">
          <stats-card
            title="Comparer et reservez en quelques clics"
            type="gradient-red"
            class="mb-4 mb-xl-0"
          >
            <template v-slot:footer>
                <div class="row">
                    <div class="col-lg-3">
                        <base-input
                        formClasses="input-group-alternative mb-3"
                        placeholder="Ville"
                        addon-left-icon="ni ni-building"
                        v-model="model.city"
                        >
                        </base-input>
                    </div>
                    
                    <div class="col-lg-3">
                        <base-input
                        formClasses="input-group-alternative mb-3"
                        placeholder="Type d'evenement"
                        addon-left-icon="ni ni-clock"
                        v-model="model.eventType"
                        >
                        </base-input>
                    </div>
                    <div class="col-lg-3">
                        <base-input
                        formClasses="input-group-alternative mb-3"
                        placeholder="Date"
                        addon-left-icon="ni ni-calendar-grid-58"
                        v-model="model.date"
                        >
                        </base-input>
                    </div>
                    <div class="col-lg-3">
                        <base-input
                        formClasses="input-group-alternative mb-3"
                        placeholder="Nb Personnes"
                        addon-left-icon="ni ni-"
                        v-model="model.nbPersons"
                        >
                        </base-input>
                    </div>
                </div>
            </template>
          </stats-card>
        </div>
      </div>
    </base-header>

    <div class="container-fluid mt-4">
        <h1 class="text-center">Comment ça marche</h1>
      <!--Charts-->
      <div class="row">

        <div class="col-xl-4">
          <card header-classes="bg-transparent">
            <template v-slot:header>
              <div class="row align-items-center">
                <div class="col">
                    <h1 class="text-center">1</h1>
                  <h3 class="text-center text-uppercase text-muted ls-1 mb-1">
                    Comparez
                  </h3>
                </div>
              </div>
            </template>
            <div class="chart-area">
            </div>
          </card>
        </div>

        <div class="col-xl-4">
          <card header-classes="bg-transparent">
            <template v-slot:header>
              <div class="row align-items-center">
                <div class="col">
                    <h1 class="text-center">2</h1>
                  <h3 class="text-center text-uppercase text-muted ls-1 mb-1">
                    Reservez
                  </h3>
                  <!-- <h5 class="h3 mb-0">Total orders</h5> -->
                </div>
              </div>
            </template>
            <div class="chart-area">
            </div>
          </card>
        </div>

        <div class="col-xl-4">
          <card header-classes="bg-transparent">
            <template v-slot:header>
              <div class="row align-items-center">
                <div class="col">
                    <h1 class="text-center">3</h1>
                  <h3 class="text-center text-uppercase text-muted ls-1 mb-1">
                    Profiter
                  </h3>
                  <!-- <h5 class="h3 mb-0">Total orders</h5> -->
                </div>
              </div>
            </template>
            <div class="chart-area">
            </div>
          </card>
        </div>
      </div>
      <!-- End charts-->
      <h1 class="text-center">Type d'événement</h1>
      <!--Charts-->
      <div class="row">

        <div class="col-xl-4">
          <card header-classes="bg-transparent">
            <template v-slot:header>
              <div class="row align-items-center">
                <div class="col">
                    <h1>1</h1>
                  <h3 class="text-uppercase text-muted ls-1 mb-1">
                    Comparez
                  </h3>
                </div>
              </div>
            </template>
            <div class="chart-area">
            </div>
          </card>
        </div>

        <div class="col-xl-4">
          <card header-classes="bg-transparent">
            <template v-slot:header>
              <div class="row align-items-center">
                <div class="col">
                    <h1>2</h1>
                  <h3 class="text-uppercase text-muted ls-1 mb-1">
                    Reservez
                  </h3>
                  <!-- <h5 class="h3 mb-0">Total orders</h5> -->
                </div>
              </div>
            </template>
            <div class="chart-area">
            </div>
          </card>
        </div>

        <div class="col-xl-4">
          <card header-classes="bg-transparent">
            <template v-slot:header>
              <div class="row align-items-center">
                <div class="col">
                    <h1>3</h1>
                  <h3 class="text-uppercase text-muted ls-1 mb-1">
                    Profiter
                  </h3>
                  <!-- <h5 class="h3 mb-0">Total orders</h5> -->
                </div>
              </div>
            </template>
            <div class="chart-area">
            </div>
          </card>
        </div>
      </div>


      <h1 class="text-center">Ville</h1>
      <!--Charts-->

      <div class="row">

        <div class="col-xl-4">
          <card header-classes="bg-transparent">
            <template v-slot:header>
              <div class="row align-items-center">
                <div class="col">
                    <h1>1</h1>
                  <h3 class="text-uppercase text-muted ls-1 mb-1">
                    Comparez
                  </h3>
                </div>
              </div>
            </template>
            <div class="chart-area">
            </div>
          </card>
        </div>

        <div class="col-xl-4">
          <card header-classes="bg-transparent">
            <template v-slot:header>
              <div class="row align-items-center">
                <div class="col">
                    <h1>2</h1>
                  <h3 class="text-uppercase text-muted ls-1 mb-1">
                    Reservez
                  </h3>
                  <!-- <h5 class="h3 mb-0">Total orders</h5> -->
                </div>
              </div>
            </template>
            <div class="chart-area">
            </div>
          </card>
        </div>

        <div class="col-xl-4">
          <card header-classes="bg-transparent">
            <template v-slot:header>
              <div class="row align-items-center">
                <div class="col">
                    <h1>3</h1>
                  <h3 class="text-uppercase text-muted ls-1 mb-1">
                    Profiter
                  </h3>
                  <!-- <h5 class="h3 mb-0">Total orders</h5> -->
                </div>
              </div>
            </template>
            <div class="chart-area">

            </div>
          </card>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
// Charts


export default {
  components: {
  },
  data() {
    return {
      model:{date: "", city:"", nbPersons: ""},
    };
  },
  methods: {
  },
  mounted() {
  },
};
</script>
<style></style>
