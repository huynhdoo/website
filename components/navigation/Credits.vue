<template>
  <v-dialog
    v-model="credits"
    scrollable
    max-width="700px"
    light
    @click:outside="$emit('closeCredits')"
  >
    <v-card>
      <v-card-title>
        <v-avatar
          small
          class="mr-3"
          tile
          color="grey lighten-5"
          size="72"
        >
          <v-img
            contain
            max-height="100%"
            src="/logo.png"
          />
        </v-avatar>Credits
        <v-spacer />
        <v-btn
          icon
          @click="$emit('closeCredits')"
        >
          <v-icon>mdi-close</v-icon>
        </v-btn>
      </v-card-title>
      <v-divider />
      <v-card-text class="pt-6 px-6 subtitle-1">
        WPRN (Word Pandemic Research Network) is a collective effort that
        originated from
        <a
          href="https://www.paris-iea.fr"
          target="_blank"
        >IAS Paris - IEA de Paris</a>.
        <br>
        <b>Thanks</b>
        to all those whose contribution and collective intelligence provides us
        all with this shared resource.
        <br>This is a non-profit initiative. We welcome donations.
        <br>
        <span
          style="color: #1976d2; text-decoration: underline; cursor: pointer;"
          @click="
            $emit('closeCredits')
            $router.push({ path: '/advisory_board' })
          "
        >Advisory Board</span>&nbsp;-&nbsp;
        <span
          style="color: #1976d2; text-decoration: underline; cursor: pointer;"
          @click="
            $emit('closeCredits')
            $router.push({ path: '/referents' })
          "
        >Referents</span>&nbsp;-&nbsp;
        <span
          style="color: #1976d2; text-decoration: underline; cursor: pointer;"
          @click="
            $emit('closeCredits')
            $router.push({ path: '/institutions' })
          "
        >Contributors' Institutions</span>
        <br>

        <v-divider />This website and logo as well as its infrastructure have
        been designed by
        <a
          href="https://www.linkedin.com/in/antoine-cordelois/?locale=en_US"
          target="_blank"
        >Antoine Cordelois</a>. The frontend is static/lambda-generated and is powered by
        <a
          href="https://nuxtjs.org/"
          target="_blank"
        >Nuxt</a> and
        <a
          href="http://vuetifyjs.com"
          target="_blank"
        >Vuetify</a>
        .
        <br>The backend is built around a serverless/FAAS graphQL API made on
        top of
        <a
          href="https://aws.amazon.com/"
          target="_blank"
        >AWS ecosystem</a>.
        <br>The logo is based on a SVG file downloaded from
        <a
          href="https://thenounproject.com"
          target="_blank"
        >thenounproject.com</a>
        named "Globe" by
        <a
          href="https://thenounproject.com/nguyenthanhthuydesign/"
          target="_blank"
        >NTT</a>.
        <br>All the images used are free of rights (or distributed as
        such).
        <br>
        <span class="caption">
          <a
            rel="license"
            href="http://creativecommons.org/licenses/by-sa/4.0/"
          >
            <img
              alt="Creative Commons License"
              style="border-width: 0;"
              src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png"
            >
          </a>
          <br>
          <span
            xmlns:dct="http://purl.org/dc/terms/"
            property="dct:title"
          >WPRN</span>
          by
          <a
            xmlns:cc="http://creativecommons.org/ns#"
            href="https://wprn.org"
            property="cc:attributionName"
            rel="cc:attributionURL"
          >World Pandemic Research Network</a>
          is licensed under a
          <a
            rel="license"
            href="http://creativecommons.org/licenses/by-sa/4.0/"
          >
            Creative Commons Attribution-ShareAlike 4.0 International
            License
          </a>.
          <br>Based on a work at
          <a
            xmlns:dct="http://purl.org/dc/terms/"
            href="https://github.com/WPRN/website"
            rel="dct:source"
          >https://github.com/WPRN/website</a>
          By Antoine Cordelois.
        </span>
      </v-card-text>

      <v-divider />
      <v-card-actions>
        <v-spacer />
        <v-btn
          color="blue darken-1"
          text
          @click="$emit('closeCredits')"
        >
          Close
        </v-btn>
      </v-card-actions>
    </v-card>
  </v-dialog>
</template>
<script>
export default {
  props: {
    credits: {
      type: Boolean,
      default: false,
      required: false
    }
  }
}
</script>
