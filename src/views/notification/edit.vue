<template>
  <div>
    <div class="container">
      <div class="row">
        <div class="mr40 mt20">
          <router-link to="/list-notification">
            <img src="../../assets/icons/back.svg" />
          </router-link>
        </div>
        <div>
          <h1 class="m0">Update Notifikasi</h1>
          <p class="mt5 mb20 tc-green">
            Make notifications to your customers so they know about discount
            products and other things in your shop
          </p>
        </div>
      </div>
      <hr class="uline-grey" />
      <div class="mt50 row">
        <div class="w20">
          <label class="form-label w80">Tittle & Content</label>
        </div>
        <div class="w80 relative">
          <input class="form-text" type="text" placeholder="Judul Article" />
          <!-- <input
            class="form-text"
            @change.prevent="handle_article_name($event)"
            type="text"
            placeholder="Judul Article"
          /> -->
          <textarea
            class="form-text"
            cols="30"
            rows="10"
            placeholder="Content (Min. 1000 Char)"
          ></textarea>
        </div>
      </div>
      <div class="mt30 row">
        <div class="w20">
          <label class="form-label">Broadcast Schedule</label>
        </div>
        <div class="w80 relative">
          <input class="form-text" type="text" placeholder="Masukkan tanggal" />
          <span class="addon-right">x</span>
        </div>
      </div>
      <div class="flex mt30">
        <router-link to="/list-notification">
          <button class="bt-submit-green">Update Notifikasi</button>
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "detail-notification",
};
</script>
