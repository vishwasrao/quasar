<template>
 <q-layout>
   <div class="layout-padding docs-input row justify-center">
    <q-card  style="width: 700px" >
  <q-card-title class="bg-light-blue">
    Search in Blockchain for NCB
  </q-card-title>
  <q-card-separator />
  <q-card-main>
    <q-field
    icon="assignment_ind"
    label="<strong>Policy Number</strong>"
    :label-width="3"
    error-label="Please type a valid policy number"
    required="true">
    <q-input
      type="text"
      v-model="policy_number"
    />
  </q-field>
  <q-field
    icon="account_circle"
    label="First Name"
    :label-width="3"
    error-label="Please type a valid first name"
    required="true">
    <q-input
      type="text"
      v-model="first_name"
    />
  </q-field>
  <q-field
    icon="account_circle"
    label="Last Name"
    :label-width="3"
    error-label="Please type a valid last name"
    required="true">
    <q-input
      type="text"
      v-model="first_name"
    />
  </q-field>
  <q-field
    icon="business"
    label="Insurer Name"
    :label-width="3"
    error-label="Please type a valid insurer name"
    required="true">
    <q-input
      type="text"
      v-model="insurer_name"
    />
  </q-field>
    <q-field
    icon="directions_car"
    label="Vehicle Class"
    :label-width="3"
    error-label="Please type a valid insurer name"
    required="true">
    <q-select
      v-model="vehicle_class"
      radio
     :options="selectOptions"
    />
  </q-field>
  <q-field
    icon="directions_car"
    label="Vehicle Number"
    :label-width="3"
    error-label="Please type a valid vehicle number"
    required="true">
    <q-input
      type="text"
      v-model="vehicle_number"
    />
  </q-field>
  </q-card-main>
  </q-card-separator>
  <q-card-actions class="bg-blue" align="center">
    <q-btn flat color="default">Clear</q-btn>
    <q-btn flat color="default">Submit</q-btn>
  </q-card-actions>
</q-card>
 </div>
  </q-layout>
</template>
<script>
import { required, email } from 'vuelidate/lib/validators'
export default {
  name: 'search',
  data () {
    return {
      msg: 'This is searh page',
      policy_number: '',
      first_name: '',
      last_name: '',
      insurer_name: '',
      vehicle_class: '',
      vehicle_number: '',
      selectOptions: [
        {
          label: 'Private Car',
          value: '11'
        },
        {
          label: 'Two Wheeler',
          value: '14'
        },
        {
          label: 'Goods Carrying Private',
          value: '18'
        },
        {
          label: 'Passenger Carrying 4 Wheeler',
          value: '21'
        }
      ]
    }
  },
  validations: {
    email: { required, email }
  }
}
</script>

<style lang="stylus">

</style>
