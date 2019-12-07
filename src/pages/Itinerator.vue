<template>
  <div class="q-pa-md row items-start q-gutter-md">
    <q-card class="my-card">
      <q-card-section class="bg-green-10 text-white">
        <div class="text-subtitle2">Places</div>
      </q-card-section>

      <q-separator />

      <q-card-actions vertical class="bg-amber-1" align="around">
        <q-select
          class="city"
          bg-color="green-2"
          square outlined
          v-model="placesTypeModel"
          :options="placeOptions"
          label="Select Type of Place"
        />
        <q-select
          class="city"
          bg-color="green-2"
          square outlined
          v-model="placesCityModel"
          :options="cityOptions"
          label="Select City"
        />
        <q-btn>Get Places</q-btn>
      </q-card-actions>
    </q-card>

    <q-card class="my-card">
      <q-card-section class="bg-green-8 text-white">
        <div class="text-subtitle2">Events</div>
      </q-card-section>

      <q-card-actions vertical class="bg-amber-1" align="around">
        <q-select
          class="city"
          bg-color="green-2"
          square outlined
          v-model="eventTypeModel"
          :options="eventOptions"
          label="Select Type of Event"
        />
        <q-select
          class="city"
          bg-color="green-2"
          square outlined
          v-model="eventDateModel"
          :options="eventDateOptions"
          label="Select Date Range"
        />
        <q-btn>Get Events</q-btn>
      </q-card-actions>
    </q-card>

    <q-card class="my-card">
      <q-card-section class="bg-green-6 text-white">
        <div class="text-subtitle2">Trails</div>
      </q-card-section>
      <q-card-actions vertical class="bg-amber-1" align="around">
        <q-select
          class="city"
          bg-color="green-2"
          square outlined
          v-model="trailDifficultyModel"
          :options="trailOptions"
          label="Select Type of Trail"
        />
     <q-select
          class="city"
          bg-color="green-2"
          square outlined
          v-model="trailRadiusModel"
          :options="trailRadiusOptions"
          label="Select Radius (miles)"
        />
        <q-btn>Get Trails</q-btn>
      </q-card-actions>
    </q-card>

    <q-card class="my-card">
      <q-card-section class="bg-green-10 text-white">
        <div class="text-subtitle2">Directions</div>
      </q-card-section>

      <q-card-actions vertical class="bg-amber-1" align="around">
        <q-select
          class="city"
          bg-color="green-2"
          square outlined
          v-model="directionsModel"
          :options="directionsOptions"
          label="Type of Directions"
        />
        <q-btn class="q-mt-md">Display Trip</q-btn>
        <q-btn>Display Directions</q-btn>
      </q-card-actions>
    </q-card>
  </div>

  <!-- <div class="text-white">
    
        <q-select class="city" bg-color="deep-purple-3" square outlined v-model="model" :options="options" label="Select City" />
     
    <q-list padding bordered class="rounded-borders">
      <q-expansion-item
        expand-separator
        icon="fas fa-map-marker-alt"
        label="Places"
        header-class="bg-green text-grey-9"
        dense
      >
       
        <q-card class="bg-green-2 text-black">
        
              <div class="row">
             <q-select filled v-model="model" :options="options" label="Select Type of Place" />
             <q-select filled v-model="model" :options="options" label="Select City" />
             </div>
    
        </q-card>
      </q-expansion-item>

      <q-expansion-item
        expand-separator
        icon="fas fa-guitar"
        label="Events"
        header-class="bg-red-5 text-grey-9"
        dense
      >
         <q-card class="bg-red-2">
         
              <div class="row">
              <q-select filled v-model="model" :options="options" label="Select Date" />
             <q-select filled v-model="model" :options="options" label="Select Type of Event" />
             </div>
         
        </q-card>
      </q-expansion-item>

      <q-expansion-item
        expand-separator
        icon="fas fa-hiking"
        label="Trails"
        header-class="bg-amber-6 text-grey-9"
        dense
      >
        <q-card class="bg-amber-2">
         
              <q-select filled v-model="model" :options="options" label="Select Type of Trail" />
         
        </q-card>
      </q-expansion-item>
      <div class="q-pa-sm q-gutter-xs">
      <q-btn unelevated rounded color="primary" label="Display Trip" />
      <q-btn unelevated rounded color="secondary" label="Display Directions" />
      </div>
  </q-list>-->
</template>

<script>
export default {
  data() {
    return {
      directionsModel: null,
      trailRadiusModel: null,
      trailDifficultyModel: null,
      eventDateModel: null,
      eventTypeModel: null,
      placesTypeModel: null,
      placesCityModel: null,
      placeOptions: ["Museum", "Restaurant", "Bakery"],
      cityOptions: ["Boston", "New York", "Seattle"],
      eventOptions: ["Concert", "Festival", "Performing Arts"],
      eventDateOptions: ["Today", "Tomorrow", "This Week", "Next Week"],
      trailOptions: ["Easy", "Medium", "Difficult"],
      directionsOptions: ["Driving", "Walking"],
      trailRadiusOptions: [1,5,10,20]
    };
  },
  methods: {
    async print() {
      alert("This works!");
    }
  }
};
</script>


<style lang="sass" scoped>
.my-card 
  width: 100%
  max-width: 250px
  height: 215px
  background-color: cornsilk

.q-select
    width: 50%

.q-list
    width: 100%

.q-btn

.city
    width: 100%

  </style>
