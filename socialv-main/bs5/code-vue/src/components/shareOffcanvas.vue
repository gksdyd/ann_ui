<template>
  <b-modal id="modal-share-offcanvas" centered title="Share" hide-backdrop bodyClass="mt-4" size="lg"
    modalClass="sharemodal" hideFooter title-tag="h3">
    <div class="row gy-3">
      <div class="col-lg-2 col-sm-4 col-6 text-center">
        <a href="#" class="d-inline-block">
          <span class="image">
            <img src="@/assets/images/icon/embed.png" class="img-fluid" />
          </span>
          <h6 class="mt-2 mb-0 font-size-14 fw-semibold">Embed</h6>
        </a>
      </div>
      <div class="col-lg-2 col-sm-4 col-6 text-center">
        <a href="#" class="d-inline-block">
          <span class="image">
            <img src="@/assets/images/icon/whatsapp.png" class="img-fluid" />
          </span>
          <h6 class="mt-2 mb-0 font-size-14 fw-semibold">WhatsApp</h6>
        </a>
      </div>
      <div class="col-lg-2 col-sm-4 col-6 text-center">
        <a href="#" class="d-inline-block">
          <span class="image">
            <img src="@/assets/images/icon/facebook.png" class="img-fluid" />
          </span>
          <h6 class="mt-2 mb-0 font-size-14 fw-semibold">Facebook</h6>
        </a>
      </div>
      <div class="col-lg-2 col-sm-4 col-6 text-center">
        <a href="#" class="d-inline-block">
          <span class="image">
            <img src="@/assets/images/icon/twitter.png" class="img-fluid" />
          </span>
          <h6 class="mt-2 mb-0 font-size-14 fw-semibold">Twitter</h6>
        </a>
      </div>
      <div class="col-lg-2 col-sm-4 col-6 text-center">
        <a href="#" class="d-inline-block">
          <span class="image">
            <img src="@/assets/images/icon/pinterest.png" class="img-fluid" />
          </span>
          <h6 class="mt-2 mb-0 font-size-14 fw-semibold">Pinterest</h6>
        </a>
      </div>
      <div class="col-lg-2 col-sm-4 col-6 text-center">
        <a href="#" class="d-inline-block">
          <span class="image">
            <img src="@/assets/images/icon/linkedin.png" class="img-fluid" />
          </span>
          <h6 class="mt-2 mb-0 font-size-14 fw-semibold">LinkedIn</h6>
        </a>
      </div>
    </div>
    <div class="mt-4">
      <div class="share-form">
        <input type="text" class="form-control" value="https://iqonic.design/" />
        <button class="btn btn-link share-link-btn h6 m-0 fw-semibold">
          Copy
        </button>
      </div>
    </div>
  </b-modal>
</template>
