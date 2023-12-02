<template>
  <div>
    <Menu />
    <div class="container">
      <h1 class="m0">Notifikasi</h1>
      <div class="row">
        <div class="col">
          <p class="mt5 mb20 tc-green">Manage your Notifikasi</p>
        </div>
        <div class="col flex">
          <router-link to="/add-notification">
            <button class="bt-green">+ Add</button>
          </router-link>
        </div>
      </div>
      <div class="row bg-blue mt10 p10">
        <div class="col">
          <input
            class="search-field"
            type="text"
            id="deskripsi"
            placeholder="Search by invoice number, name, amount..."
          />
        </div>
        <div class="col flex">
          <button class="bt-blue">
            <img src="../../assets/images/filter.png" alt="" width="15" />
            Filter
          </button>
        </div>
      </div>
      <div class="mt50">
        <table>
          <thead>
            <tr>
              <th>TITLE</th>
              <th>BROADCAST SCHEDULE</th>
              <th>ARTICLE STATUS</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="item of list_notification" :key="item.id">
              <td class="center">{{ item.title }}</td>
              <td class="center">
                <div v-if="item.notification_status === 1">
                  <label class="label-green">{{
                    item.broadcast_schedule
                  }}</label>
                </div>
                <div v-if="item.notification_status === 2">
                  <label class="label-red">{{ item.broadcast_schedule }}</label>
                </div>
              </td>
              <td class="center">
                <div v-if="item.notification_status === 1">
                  <label class="label-green">Active</label>
                </div>
                <div v-if="item.notification_status === 2">
                  <label class="label-red">Inactive</label>
                </div>
              </td>
              <td class="center">
                <div class="mt5">
                  <router-link to="/edit-notification">
                    <img src="../../assets/icons/edit.svg" />
                  </router-link>
                </div>
                <div class="mt5">
                  <router-link to="/detail-notification">
                    <img src="../../assets/icons/detail.svg" />
                  </router-link>
                </div>
                <div class="mt5">
                  <img src="../../assets/icons/delete.svg" />
                </div>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
import Menu from "../../components/menu.vue";

export default {
  name: "list-notification",
  components: {
    Menu,
  },
  data() {
    return {
      list_notification: [
        {
          id: "1",
          title: "Diskon 50% untuk Handphone Samsung Seria A",
          broadcast_schedule: "07-06-2021 09:41PM",
          notification_status: 2,
        },
        {
          id: "2",
          title: "Diskon 10% untuk Handphone Iphone 11",
          broadcast_schedule: "09-06-2021 09:41PM",
          notification_status: 1,
        },
        {
          id: "3",
          title: "Produk yang Anda Lihat Kembali Tersedia!",
          broadcast_schedule: "09-06-2021 09:41PM",
          notification_status: 1,
        },
      ],
    };
  },
};
</script>
