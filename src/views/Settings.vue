<template>
    <div>
        <base-header class="pb-6 pb-8 pt-5 pt-md-8 bg-gradient-primary"></base-header>

        <card class="min-vh-100 main_body center">

            <div class="row card text-black">

                <div class="col-lg mx-auto form p-4">

                        <button type="button" class="btn" @click="currentTabComponent ='Account'" >Acount</button>
                        <button type="button" class="btn" @click="currentTabComponent ='Privacy'" >Privacy</button>
                        <button  type=" button"  class="btn"  @click="currentTabComponent ='Display'" >Display </button>
                        <button   type=" button"  class="btn"  @click="currentTabComponent ='Payment'"  >Payment</button>
                        <button   type=" button"  class="btn"  @click="currentTabComponent ='Security'" >Security</button>
                        <button   type=" button"  class="btn"  @click="currentTabComponent ='Localisation'">Localisation </button>
                        <!--  <p> {{currentTabComponent}} </p> -->
                        <component v-bind:is ="currentTabComponent" ></component>
                    <!-- <p> This will be the settings page</p> -->
                </div>
            </div>
        </card>
    </div>
</template>

<script>
import Account from  './Account.vue';
import Privacy from  './Privacy.vue';
import Security from  './Security.vue';
import Display from   './Display.vue';
import Payment from   './Payment.vue';
import Localisation from './Localisation.vue';

export default {

  components:{
    'Account': Account,
    'Privacy': Privacy,
    'Security': Security,
    'Display': Display,
    'Payment': Payment,
    'Localisation': Localisation,

  },

  data() {
    return {
          currentTabComponent:"Account"
    };
  },
};
</script>

<style>

</style>
