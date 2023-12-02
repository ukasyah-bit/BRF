<template>
  <div>
    <Menu />
    <div class="container">
      <h1 class="m0">Article</h1>
      <div class="row">
        <div class="col">
          <p class="mt5 mb20 tc-green">Manage your Article</p>
        </div>
        <div class="col flex">
          <router-link to="/add-article">
            <button class="bt-green">+ Add</button>
          </router-link>
        </div>
      </div>
      <div class="row bg-blue mt10 p10">
        <div class="col relative">
          <img src="../../assets/images/search.png" alt="" class="addon-left" />
          <input
            class="search-field pl40"
            type="text"
            id="deskripsi"
            placeholder="Search by invoice number, name, amount..."
          />
        </div>
        <div class="col flex relative">
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
              <th>ARTICLE NAME</th>
              <th>BROADCAST SCHEDULE</th>
              <th>VALID FROM</th>
              <th>VALID UNTIL</th>
              <th>ARTICLE STATUS</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="item of list_article" :key="item.id">
              <td class="center">{{ item.name }}</td>
              <td class="center">
                {{ item.broadcast_schedule }}
              </td>
              <td class="center">
                <label class="label-green">{{ item.valid_from }}</label>
              </td>
              <td class="center">
                <label class="label-green">{{ item.valid_until }}</label>
              </td>
              <td class="center">
                <label class="label-green">{{ item.article_status }}</label>
              </td>
              <div v-if="item.article_status === 1">
                <label class="label-green">Active</label>
              </div>
              <div v-if="item.article_status === 1">
                <label class="label-blue">Inactive</label>
              </div>
              <td class="center">
                <div class="mt5">
                  <router-link to="/edit-article">
                    <img src="../../assets/icons/edit.svg" />
                  </router-link>
                </div>
                <div class="mt5">
                  <router-link to="/detail-article">
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
  name: "list-article",
  components: {
    Menu,
  },
  data() {
    return {
      list_article: [
        {
          id: "1",
          name: "Produk Rumah dan Furniture",
          broadcast_schedule: "Senin",
          valid_from: "01-06-2021",
          valid_until: "03-06-2021",
          article_status: "Active",
        },
        {
          id: "2",
          name: "Pakaian dan Outfit",
          broadcast_schedule: "Kamis",
          valid_from: "04-06-2021",
          valid_until: "06-06-2021",
          article_status: "Active",
        },
        {
          id: "3",
          name: "Buku dan Media Digital",
          broadcast_schedule: "Rabu",
          valid_from: "07-06-2021",
          valid_until: "09-06-2021",
          article_status: "Active",
        },
      ],
    };
  },
};
</script>
