<template>
  <div class="about">
<!--    <h1>This is a table page</h1>-->
      <v-table>
        <thead>
        <tr>
          <th class="text-left">
            Name
          </th>
          <th class="text-left">
            Calories
          </th>
          <th class="text-left">
            Calories
          </th>
        </tr>
        </thead>
        <tbody>
        <tr
            v-for="item in desserts"
            :key="item.name"
        >
          <td>{{ item.name }}</td>
          <td>{{ item.calories }}</td>
          <td><v-btn @click="gotoDetail">
            Button
          </v-btn></td>
        </tr>
        </tbody>
      </v-table>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>

<script>
import router from "@/router";

export default {
  data () {
    return {
      desserts: [
        {
          name: 'Frozen Yogurt',
          calories: 159,
        },
        {
          name: 'Ice cream sandwich',
          calories: 237,
        },
        {
          name: 'Eclair',
          calories: 262,
        },
        {
          name: 'Cupcake',
          calories: 305,
        },
        {
          name: 'Gingerbread',
          calories: 356,
        },
        {
          name: 'Jelly bean',
          calories: 375,
        },
        {
          name: 'Lollipop',
          calories: 392,
        },
        {
          name: 'Honeycomb',
          calories: 408,
        },
        {
          name: 'Donut',
          calories: 452,
        },
        {
          name: 'KitKat',
          calories: 518,
        },
      ],
    }
  },
  methods: {
    gotoDetail() {
      router.push('halo')
    }
  }
}
</script>