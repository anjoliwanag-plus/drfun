<template>
  <v-table>
    <thead>
      <tr>
        <th class="text-left">
          test
        </th>
        <th class="text-left">
          test1
        </th>
        <th class="text-left">
          test2
        </th>
      </tr>
    </thead>
    <tbody v-if="data">
      <tr v-for="item, index in data.data" :key="index">
        <td>{{ item.test }}</td>
        <td>{{ item.test1 }}</td>
        <td>{{ item.test2 }}</td>
      </tr>
    </tbody>
  </v-table>
</template>
  
<script lang="ts" setup>
import { useFetch } from '@vueuse/core'
const { data, error } = useFetch('https://script.googleusercontent.com/macros/echo?user_content_key=7G-LCIN8i_0QV6oTcoeJAncquANMxW85MQ0nnLktJrT3fEZSHLinHY8UJJx8Y270rbsJ4p2JdG4ky3HWvOqebA6z5KhCYy3bm5_BxDlH2jW0nuo2oDemN9CCS2h10ox_1xSncGQajx_ryfhECjZEnDOv62INWHc57QDkj9WUmDJkZmMhnvOU47cTmJCVFbZy5hwdJVbMGSpC2tIT3Bo7RSiEdqMbFSJnw4kdwQ-WGlE44dDzxQ-41w&lib=Ma-l7ffZ08duyZ8j_mgYtaNSIthR4QL2e', { refetch: true }).json()
</script>
  