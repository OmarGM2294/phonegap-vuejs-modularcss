<template>
    <div class="grid-container grid-container-padded hello" :style="{ height: clientHeight }">
      <div class="grid-y grid-frame">
        <div class="cell auto"></div>
        <div class="cell">
          <figure class="hello__figure">
            <img :src="imageSrc" />            
          </figure>
        </div>
        <div class="cell shrink">
          <div class="grid-x">
            <div class="cell small-12 medium-offset-1 medium-10 large-offset-2 large-8">
              <div class="content-section">
                  <h6 class="hello__subtitle">
                    {{ $t("language") }} &#x2022; <b>{{ getLanguage() }}</b>
                  </h6>
                  <h1 class="hello__title">
                    {{ $t("hello.welcome") }}
                  </h1>
                  <h5 class="hello__paragraph">
                    {{ $t("hello.paragraph") }}
                  </h5>

                  <hr>

                  <div class="hello__terms"><b>{{ $t("references") }}:</b> <a :href="url.bem" target="_blank">BEM</a>, <a :href="url.smacss" target="_blank">SMACSS</a>, <a :href="url.modularScale" target="_blank">Modular Scale</a> {{ $t("and") }} <a :href="url.foundation" target="_blank">Foundation</a>.</div>

                  <div class="hello__copyright">
                    {{ $t("by") }} <a :href="url.omar" target="_blank">Omar González</a> {{ $t("and") }} <a :href="url.felipe" target="_blank">Felipe Castillo</a>
                  </div>
              </div>              
            </div>
          </div>
        </div>
        <div class="cell auto"></div>
      </div>
    </div>
</template>

<script>
    export default {
        data(){
            return {
                imageSrc: '',
                clientHeight: 0,
                url: {
                  omar: 'http://omargm2294.github.io/Portafolio/',
                  felipe: 'https://www.behance.net/dafelipe',
                  bem: 'https://en.bem.info/methodology/key-concepts',
                  smacss: 'https://smacss.com',
                  modularScale: 'https://github.com/modularscale/modularscale-sass',
                  foundation: 'http://foundation.zurb.com/sites/docs/xy-grid.html'
                }
            }
        },
        methods:{
        },
        created() {
            this.$http.get('https://vuejs.org/images/logo.png').then(function(response){
                this.imageSrc = response.url;
            });
        },
        mounted(){
            this.clientHeight = document.documentElement.clientHeight + 'px';
            this.updateLanguage(navigator.language || navigator.userLanguage);
        }
    }
</script>

<style scoped>

    img{
        width: 100%;
    }

    p{
      text-align: left;
    }
</style>
