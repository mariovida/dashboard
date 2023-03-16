<template>
  <div class="about">
    <section>
      <div class="wrapper">
        <h1>This is an about page</h1>

        <b-button v-b-modal.modal-1>Launch demo modal</b-button>
        <b-modal id="modal-1" title="BootstrapVue">
          <p class="my-4">Hello from modal!</p>
        </b-modal>

        <b-button v-b-toggle.collapse-2 variant="primary">Toggle Collapse</b-button>
        <b-collapse id="collapse-2" class="mt-2">
          <b-card>
            <p class="card-text">Collapse contents Here</p>
            <b-button v-b-toggle.collapse-2-inner size="sm">Toggle Inner Collapse</b-button>
            <b-collapse id="collapse-2-inner" class="mt-2">
              <b-card>Hello!</b-card>
            </b-collapse>
          </b-card>
        </b-collapse>
      </div>  
    </section>
  </div>
</template>
