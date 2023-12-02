<template>
  <div>
    <div class="container">
      <div class="row">
        <div class="mr40 mt20">
          <router-link to="/list-article">
            <img src="../../assets/icons/back.svg" />
          </router-link>
        </div>
        <div>
          <h1 class="m0">Update Article</h1>
          <p class="mt5 mb20 tc-green">Make your article looks good</p>
        </div>
      </div>
      <hr class="uline-grey" />
      <div class="mt50 row">
        <div class="w20">
          <label class="form-label">Article Image</label>
        </div>
        <div class="w80">
          <input class="hidden" type="file" id="upload-file" />
          <img
            class="cursor-pointer"
            src="../../assets/images/Frame update.png"
            alt=""
            @click="upload_file()"
          />
        </div>
      </div>
      <div class="mt30 row">
        <div class="w20">
          <label class="form-label">Article Name & Content</label>
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
            placeholder="Content (Min 1000 Char)"
          ></textarea>
          <span class="addon-right">| 5 / 20</span>
        </div>
      </div>
      <div class="mt30 row">
        <div class="w20">
          <label class="form-label">Broadcast Schedule</label>
        </div>
        <div class="w80 relative">
          <input class="form-text" type="text" placeholder="Pilih Hari" />
          <img
            width="15"
            class="addon-right"
            src="../../assets/images/edit-2.png"
            alt=""
          />
        </div>
      </div>
      <div class="mt30 row">
        <div class="w20">
          <label class="form-label">Valid From</label>
        </div>
        <div class="w80">
          <input class="form-text" type="text" placeholder="Masukkan Tanggal" />
        </div>
      </div>
      <div class="mt30 row">
        <div class="w20">
          <label class="form-label">Valid Until</label>
        </div>
        <div class="w80">
          <input class="form-text" type="text" placeholder="Masukkan Tanggal" />
        </div>
      </div>
      <div class="flex mt30">
        <router-link to="/list-article">
          <button class="bt-submit-green">Update Article</button>
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "detail-user",
};
</script>
