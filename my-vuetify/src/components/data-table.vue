
<template>
    <v-data-table v-bind:headers="headers" :items="items" hide-actions class="elevation-1">
        <template slot="items" scope="props">
            <td>{{ props.item.name }}</td>
            <td class="text-xs-right">{{ props.item.webSite }}</td>
            <td class="text-xs-right">{{ props.item.date }}</td>
            <td class="text-xs-right">{{ props.item.availableCount }}</td>
            <td class="text-xs-right">{{ props.item.roomId }}</td>
        </template>
    </v-data-table>
</template>

<script>
export default {
  name : 'data-table',
  data() {
      return {
          headers: [
              {
                  text: '房間名稱',
                  align: 'left',
                  sortable: false,
                  value: 'name'
              },
              { text: '網站', value: 'webSite' },
              { text: '時間', value: 'date' },
              { text: '剩餘房數', value: 'availableCount' },
              { text: '房間ID', value: 'roomId' }
          ],
          items: [
              {
                webSite: 'Agoda',
                date: '2017-09-08',
                availableCount: 1,
                name: "標準雙人房 (Standard  Double)",
                roomId: "3647395",
              },
              {
                webSite: 'Agoda',
                date: '2017-09-08',
                availableCount: 1,
                name: "小型雙人房 (Small Double Room)",
                roomId: "14441008"
              },
              {
                  webSite: 'Agoda',
                  date: '2017-09-10',
                  availableCount: 1,
                  name: "標準雙人房 (Standard  Double)",
                  roomId: "3647395",
              },
              {
                  webSite: 'Agoda',
                  date: '2017-09-10',
                  availableCount: 1,
                  name: "小型雙人房 (Small Double Room)",
                  roomId: "14441008"
              },
              {
                  webSite: 'Booking',
                  date: '2017-09-08',
                  availableCount: 1,
                  name: "小型雙人房 (Small Double Room)",
                  roomId: "2000"
              },
              {
                  webSite: 'Booking',
                  date: '2017-09-08',
                  availableCount: 1,
                  name: "高級雙人房 (Superior Double Room)",
                  roomId: "50000"
              },
              {
                  webSite: 'Booking',
                  date: '2017-09-09',
                  availableCount: 1,
                  name: "小型雙人房 (Small Double Room)",
                  roomId: "2000"
              },
              {
                  webSite: 'Booking',
                  date: '2017-09-09',
                  availableCount: 1,
                  name: "高級雙人房 (Superior Double Room)",
                  roomId: "50000"
              }
          ]
      }
  }
}
</script>

