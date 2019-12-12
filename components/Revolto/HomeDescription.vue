<template>
  <section class="overview-block-ptb grey-bg iq-specialities">
    <div class="container">
      <div class="row">
        <div class="col-sm-12">
          <div class="heading-title">
            <h3 class="title iq-tw-7">Korzyści</h3>
          </div>
        </div>
      </div>

      <div class="row">
        <div
          @click="openInfo(item)"
          v-for="(item,index) of list"
          :key="index"
          class="col-sm-12 col-lg-3 col-md-6 iq-mb-30"
        >
          <CardStyle6>
            <i slot="cardMedia" aria-hidden="true" :class="item.icon"></i>
            <div slot="cardBody">
              <h5 class="iq-tw-7 iq-pt-20 iq-pb-10">{{ item.title }}</h5>
              <p>{{ item.description }}</p>
            </div>
          </CardStyle6>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "Specialites",
  data() {
    return {
      list: [
        {
          icon: "ion-android-cart",
          title: "Finansowe",
          description:
            "Fotowoltaika w domu oznacza, że możesz zyskać niezależność od podwyżek cen prądu przez co najmniej 25 lat",
          description2:
            "Moduły fotowoltaiczne tworzące panel wytwarzają prąd ze słońca. ",
          description3:
            "W wielu przypadkach instalację fotowoltaiczną możesz odliczyć od podatku. ",
          description4: "Podniesienie wartości nieruchomości.",
          description5:
            "W przypadku instalacji 2-10 kWh możesz liczyć na wsparcie z programu „Mój Prąd” (do wyczerpania alokacji środków)."
        },
        {
          icon: "ion-earth",
          title: "Ekologiczne",
          description:
            "Czyste źródło energii – moduły fotwoltaiczne nie emitują zanieczyszczeń, można je także poddać recyklingowi",
          description2:
            "Energia słoneczna jest odnawialna i zrównoważona, co oznacza, że nie może jej zabraknąć, w przeciwieństwie do paliw kopalnych, które skończą się za kilkadziesiąt lat, zrównoważona oznacza możliwość zaspokojenia potrzeb współczesności bez narażania potrzeb przyszłych pokoleń.",
          description3:
            "Dostępność czystej energii – światło słoneczne jest dostępne w każdym miejscu na kuli ziemskiej i może być łatwo wykorzystane w ciągu dnia, dzięki temu praktycznie każdy ma możliwość pozyskiwania prądu ze słońca."
        },
        {
          icon: "ion-wrench",
          title: "Nowoczesne technologie",
          description:
            "Wysoka odporność na różne anomalie pogodowe – wiatr, grad czy zalegający śnieg",
          description2: "Technologia ciągle się rozwija.",
          description3:
            "Estetyka wykonania – pasują na każdy rodzaj i kolor dachu.",
          description4:
            "Moduły fotowoltaiczne nie wymagają konserwacji i są praktycznie bezawaryjne – nie posiadają ruchomych części, które są szczególnie narażone na uszkodzenia.",
          description5:
            "Możliwy montaż na gruncie – jeśli na dachu nie ma wystarczająco dużo miejsca możliwe jest zainstalowanie paneli fotowoltaicznych np. w ogrodzie.",
          description6:
            "Szybki montaż, nie wymagane jest pozwolenie na budowę mikroinstalacji."
        },
        {
          icon: "ion-arrow-graph-down-right",
          title: "Niskie rachunki za prąd",
          description:
            "Niezużyta energia może zostać zmagazynowana i odebrana z sieci w ciągu dwóch lat (na mocy nowelizacji ustawy)",
          description2:
            "W Polsce roczna suma energii promieniowania słonecznego padającego na 1 m2 powierzchni wynosi ok. 1000 kWh. To naprawdę dużo, bo żeby uzyskać taką ilość ciepła musimy spalić np. 100 m3 gazu ziemnego.",
          description3:
            "Roczne zapotrzebowanie nowego domu o powierzchni 150 m2 to 10 000-20 000 kWh."
        }
      ]
    };
  },
  methods: {
    openInfo(blog) {
      {
        const h = this.$createElement;
        // Using HTML string
        // More complex structure
        const messageVNode = h("div", { class: ["w3-ul w3-card-4"] }, [
          h("h1", { class: ["text-center", blog.icon] }),
          h("h4", { class: ["title iq-tw-5"] }, [h("strong", {}, blog.title)]),
          h("br", { class: ["text-left"] }),
          h("p", { class: ["textModal"] }, [h("li", {}, blog.description)]),
          h(
            "p",
            { class: ["textModal"] },

            [h("strong", {}, blog.description2)]
          ),
          h(
            "p",
            { class: ["textModal"] },

            [h("li", {}, blog.description3)]
          ),
          h(
            "p",
            { class: ["textModal"] },

            [h("strong", {}, blog.description4)]
          ),
          h(
            "p",
            { class: ["textModal"] },

            [h("li", {}, blog.description5)]
          ),
          h(
            "p",
            { class: ["textModal"] },

            [h("strong", {}, blog.description6)]
          )
        ]);
        // We must pass the generated VNodes as arrays
        this.$bvModal.msgBoxOk([messageVNode], {
          centered: false,
          okVariant: "secondary",
          size: "lg",
          scrollable: true,
          buttonSize: "sm",
          footerClass: "p-2 border-top-0"
        });
      }
    }
  }
};
</script>

<style>
.textModal {
  list-style-position: outside;
  list-style-image: none;
  font-style: oblique;
  color: rgb(16, 34, 4);
}
</style>