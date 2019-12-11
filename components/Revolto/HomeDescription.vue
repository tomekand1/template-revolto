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
        <div v-for="(item,index) of list" :key="index" class="col-sm-12 col-lg-3 col-md-6 iq-mb-30">
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
            "Fotowoltaika w domu oznacza, że możesz zyskać niezależność od podwyżek cen prądu przez co najmniej 25 lat,"
        },
        {
          icon: "ion-earth",
          title: "Ekologiczne",
          description:
            "Czyste źródło energii – moduły fotwoltaiczne nie emitują zanieczyszczeń, można je także poddać recyklingowi"
        },
        {
          icon: "ion-wrench",
          title: "Nowoczesne technologie",
          description:
            "Wysoka odporność na różne anomalie pogodowe – wiatr, grad czy zalegający śnieg"
        },
        {
          icon: "ion-arrow-graph-down-right",
          title: "Niskie rachunki za prąd",
          description:
            "Niezużyta energia może zostać zmagazynowana i odebrana z sieci w ciągu dwóch lat (na mocy nowelizacji ustawy) lub sprzedana (fotowoltaika dla firm),"
        }
      ]
    };
  }
};
</script>
