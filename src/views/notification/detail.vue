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
          <h1 class="m0">Detail Notifikasi</h1>
          <p class="mt5 mb20 tc-green">Your Notifikasi details</p>
        </div>
      </div>
      <hr class="uline-grey" />
      <div class="mt50">
        <p>Tittle</p>
        <h2>TETE</h2>
      </div>
      <div class="mt10">
        <p class="detail-title-bold">Content:</p>
        <p>NENEN</p>
      </div>
      <div class="mt10">
        <p class="detail-title-bold">Broadcast Schedule:</p>
        <p>
          <label class="label-green">23:59</label>
        </p>
      </div>
      <div class="mt10">
        <p>created by</p>
        <p>created by</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "detail-notification",
};
</script>
