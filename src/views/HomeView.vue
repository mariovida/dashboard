<template>
  <div class="home">
    <section class="">
      <div class="wrapper">
        <div class="title-row">
          <h1>Statistika</h1>
          <div class="title-row_btns">
            <a class="btn btn-primary"><font-awesome-icon icon="fa-solid fa-plus" />Novi ugovor</a>
            <a class="btn btn-outline-primary"><font-awesome-icon icon="fa-solid fa-file-import" />Predaj zahtjev</a>
          </div>
        </div>
        <b-form-group>
          <b-input-group size="sm">
            <b-form-input
              id="filter-input"
              v-model="filter"
              type="search"
              placeholder="Pretraži..."
            ></b-form-input>
          </b-input-group>
        </b-form-group>
        <b-table hover :filter="filter" :bordered="bordered" :head-variant="headVariant" :items="items" :fields="fields">
          <template #cell(status)="data">
            <span v-html="data.value"></span>
          </template>
        </b-table>
      </div>
      
    </section>
  </div>
</template>

<script>
export default {
  name: 'HomeView',
  data: function() {
      return {
        fields: [
          {
            key: 'name',
             label: 'Korisnik',
            sortable: true
          },
          {
            key: 'number',
            label: 'Broj ugovora',
            sortable: true,
          },
          {
            key: 'contract_name',
            label: 'Naziv ugovora',
            sortable: false,
          },
          {
            key: 'value',
            label: 'Iznos ugovora',
            sortable: false,
          },
          {
            key: 'date',
            label: 'Datum potpisa',
            sortable: false,
          },
          {
            key: 'status',
            label: 'Status',
            sortable: false,
          },
           {
            key: 'action',
            label: 'Akcija',
            sortable: false,
          }
        ],
        items: [
          { name: 'Lukić Luka', number: '24596157486', contract_name: 'Lorem ipsum solor dit', value: '1.235,87 €', date: '02.03.2023.', status: '<button class="badge-green">Odobreno</button>', action: 'X' },
          { name: 'Perić Pero', number: '60684203417', contract_name: 'Scelirius obus trentis', value: '32.307,34 €', date: '12.12.2022.', status: '<button class="badge-red">Odbijeno</button>', action: 'X' },
          { name: 'Jurić Juro', number: '67947752158', contract_name: 'Poluris scit et grebus',  value: '17.647,03 €', date: '24.01.2023.', status: '<button class="badge-red">Odbijeno</button>', action: 'X' },
          { name: 'Marić Marko', number: '41542982204', contract_name: 'Vinictus lorus ipor sum', value: '2.674,22 €', date: '21.11.2022.', status: '<button class="badge-green">Odobreno</button>', action: 'X' }
        ],
        bordered: true,
        headVariant: 'light',
        filter: null,
      }
    },
}
</script>
