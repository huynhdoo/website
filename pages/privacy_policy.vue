<template>
  <v-row
    align="center"
    justify="center"
  >
    <!--  BackButton takes one col -->
    <BackButton />
    <v-col
      cols="10"
      sm="10"
      md="8"
    >
      <h2 class="display-2 font-weight-bold my-3 text-uppercase text-center">
        Privacy Policy
      </h2>
    </v-col>
    <v-col cols="1" />
    <v-col
      cols="12"
      sm="12"
      md="8"
    >
      <v-responsive
        class="mx-auto mb-12"
        width="56"
      >
        <v-divider class="mb-1" />
        <v-divider />
      </v-responsive>The World Pandemic Research Network (WPRN) website’s purpose is to
      offer a global directory of research projects, surveys and
      initiatives about the societal and human impacts of the Covid-19
      pandemic. pandemic.
      <br>By registering their project on the WPRN
      website, contributors authorize the WPRN to publish online the data
      collected, except for their personal contact details (e-mail
      address). address).
      <br>E-mail addresses will never be disclosed
      online nor transferred or sold to any third party. They will be used
      only:
      <ul>
        <li>
          to redirect potential contact requests to contributors through
          the WPRN servers;
        </li>
        <li>
          by WPRN to contact contributors to enable their uploads, update
          their project, facilitate their collaborations and occasionally
          regarding evolutions of WPRN.
        </li>
      </ul>In compliance with the EU General Data Protection Regulation, you
      can exert your right to access, correct or oppose the use of your
      data by contacting info@wprn.org.
    </v-col>
  </v-row>
</template>
<script>
import { board, contributors } from '~/assets/data'
import BackButton from '~/components/navigation/BackButton'

export default {
  layout: 'page',
  components: {
    BackButton
  },
  data () {
    return {
      board,
      contributors,
      referents: []
    }
  },
  methods: {
  }
}
</script>
