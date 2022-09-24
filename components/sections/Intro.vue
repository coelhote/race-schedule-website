<template>
  <section id="intro" class="py-16">
    <v-container>
      <v-responsive class="max-auto mx-auto text-center" max-width="80%">
        <h2 class="text-h4 text-md-h3 text-center font-weight-black mb-7">
          Agenda da semana
        </h2>
        <v-tabs
          v-model="tab"
          background-color="transparent"
          color="basil"
          show-arrows
        >
          <v-tabs-slider color="teal lighten-3"></v-tabs-slider>
          <v-tab v-for="item1 in todos" :key="item1.name">
            {{ item1.name }}
          </v-tab>
        </v-tabs>

        <v-tabs-items v-model="tab">
          <v-tab-item v-for="item in todos" :key="item">
            <v-card color="basil" flat>
              <v-simple-table dense>
                <template v-slot:default>
                  <thead>
                    <tr>
                      <th class="text-center">Categoria</th>
                      <th class="text-center">Etapa</th>
                      <th class="text-center">Data/Hora</th>
                      <th class="text-center">Transmissão</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr v-for="item2 in item.infos" :key="item2.id">
                      <td>{{ item.name }}</td>
                      <td>{{ item2.gp }}</td>
                      <td>{{ item2.dataHora }}</td>
                      <td>{{ item2.transmissao }}</td>
                    </tr>
                  </tbody>
                </template>
              </v-simple-table>
            </v-card>
          </v-tab-item>
        </v-tabs-items>
      </v-responsive>

      <v-row class="pt-12">
        <v-col cols="12" md="6" sm="12" xs="12" lg="6">
          <v-responsive class="">
            <h2 class="text-h4 text-md-h3 text-center font-weight-black mb-7">
              Resultados da semana
            </h2>
            <v-tabs
              v-model="tab2"
              background-color="transparent"
              color="basil"
              show-arrows
            >
              <v-tabs-slider color="teal lighten-3"></v-tabs-slider>
              <v-tab v-for="item1 in todos" :key="item1.name">
                {{ item1.name }}
              </v-tab>
            </v-tabs>

            <v-tabs-items v-model="tab2">
              <v-tab-item v-for="item in todos" :key="item">
                <v-card color="basil" flat>
                  <v-simple-table dense>
                    <template v-slot:default>
                      <thead>
                        <tr>
                          <th class="text-center">Categoria</th>
                          <th class="text-center">Etapa</th>
                          <th class="text-center">Data/Hora</th>
                          <th class="text-center">Transmissão</th>
                        </tr>
                      </thead>
                      <tbody>
                        <tr v-for="item2 in item.infos" :key="item2.id">
                          <td>{{ item.name }}</td>
                          <td>{{ item2.gp }}</td>
                          <td>{{ item2.dataHora }}</td>
                          <td>{{ item2.transmissao }}</td>
                        </tr>
                      </tbody>
                    </template>
                  </v-simple-table>
                </v-card>
              </v-tab-item>
            </v-tabs-items>
          </v-responsive>
        </v-col>
        <v-col cols="12" md="6" sm="12" xs="12" lg="6">
          <v-responsive class="">
            <h2 class="text-h4 text-md-h3 text-center font-weight-black mb-7">
              Classificação
            </h2>
            <v-tabs
              v-model="tab"
              background-color="transparent"
              color="basil"
              show-arrows
            >
              <v-tabs-slider color="teal lighten-3"></v-tabs-slider>
              <v-tab v-for="item1 in todos" :key="item1.name">
                {{ item1.name }}
              </v-tab>
            </v-tabs>

            <v-tabs-items v-model="tab">
              <v-tab-item v-for="item in todos" :key="item">
                <v-card color="basil" flat>
                  <v-simple-table dense>
                    <template v-slot:default>
                      <thead>
                        <tr>
                          <th class="text-center">Categoria</th>
                          <th class="text-center">Etapa</th>
                          <th class="text-center">Data/Hora</th>
                          <th class="text-center">Transmissão</th>
                        </tr>
                      </thead>
                      <tbody>
                        <tr v-for="item2 in item.infos" :key="item2.id">
                          <td>{{ item.name }}</td>
                          <td>{{ item2.gp }}</td>
                          <td>{{ item2.dataHora }}</td>
                          <td>{{ item2.transmissao }}</td>
                        </tr>
                      </tbody>
                    </template>
                  </v-simple-table>
                </v-card>
              </v-tab-item>
            </v-tabs-items>
          </v-responsive>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  data() {
    return {
      tab: null,
      tab2: null,
      todos: [
        {
          infos: [
            {
              id: '1',
              gp: 'GP do Brasil',
              dataHora: '15/11 - 14:00',
              transmissao: 'Band',
            },
            {
              id: '2',
              gp: 'GP do Brasil',
              dataHora: '15/11 - 14:00',
              transmissao: 'Band',
            },
          ],
          name: 'Fórmula 1',
        },
        {
          infos: [
            {
              id: '3',
              gp: 'GP do Brasil',
              dataHora: '15/11 - 14:00',
              transmissao: 'Band',
            },
            {
              id: '4',
              gp: 'GP do Brasil',
              dataHora: '15/11 - 14:00',
              transmissao: 'Band',
            },
          ],
          name: 'Fórmula 2',
        },
      ],
      cards: [
        {
          title: 'Best Productivity',
          subtitle: 'Professionally developed',
          text: 'All components and features are developed using the most up-to-date coding practices.',
          callout: '01',
        },
        {
          title: 'Fast & optimized',
          subtitle: 'Performance',
          text: 'Themes are designed for maximum performance and are semantically structured to maximize SEO.',
          callout: '02',
        },
        {
          title: 'Built on Vuetify',
          subtitle: 'Material Design',
          text: "Being developed with Vuetify means you have access to all of the framework's available features.",
          callout: '03',
        },
      ],
    }
  },
}
</script>
