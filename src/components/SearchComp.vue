<template>
  <div class="full-width">
    <div class="row flex flex-center">
      <div class="col-md-6 col-sm-10 col-xs-12">
        <q-input
          rounded
          clearable
          :loading="isLoading"
          :items="digimons"
          :search-input.sync="search"
          hide-details
          item-text="name"
          item-value="id"
          label="Search for ..."
          solo-inverted
        />
      </div>
    </div>
  </div>
</template>
<script>
  import _ from "lodash";

  export default {
    data: () => ({
      digimons: [],
      isLoading: true,
      search: null
    }),
    methods: {
      getDigimons(params = "") {

        this.axios
          .get("https://digimon-api.vercel.app/api/digimon" + params)
          .then(resp => {

            let tempDigimon = [...this.digimons.slice(0), ...resp.data.results];
            this.digimons = _.uniqBy(tempDigimon, "id");
            this.isLoading = false;
          })
          .catch(e => {
            console.error(e);
          });
      },
      searchDigimons(query) {

        let searchQuery = encodeURI("?search=" + query);
        this.getDigimons(searchQuery);
      }
    },
    watch: {
      search: _.debounce(function(query) {

        this.searchDigimons(query);
      }, 250)
    },
    created() {
      this.getDigimons();
    }
  };
  </script>
<style>
#gradiant {
  background: linear-gradient(
      207.53deg,
      #fa00ff 0%,
      #5690ff 25.52%,
      #fa00ff 48.96%,
      #22b0ff 74.48%,
      #e600eb 100%
    ),
    linear-gradient(0deg, #ffffff, #ffffff);
}
</style>
