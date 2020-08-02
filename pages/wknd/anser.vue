<template lang="pug">
  div
    // コメント
    header
      .container
        h1 WKND
    main
      section#mv.section
        .hero
          .hero-body.container
            h3.hero-title
              span WKND Adventures
            p Join us on one of our next adventures. Browse our list of curated experiences and sign up for one when you’re ready to explore with us.

            a.btn-primary(href="") View trips

      .container
        section#last.section
          .body
            .body-left
              h3.section-title
                span Last Article
              p Camping in Western Australia
              p A vibrant red, dusty highway stretches out before us into what seems like infinity, at the far reach of our sights it distorts and shimmers from the afternoon heat, fading into the blue of the horizon.

              a.btn-primary(href="#") Read More

            .body-right
              img(src="/wknd/image-1.png")

        section#recent.section.border
          h3.section-title
            span Recent Articles

          .row
            .col
              img(src="/wknd/image-2.png")
              h5.title aaaaaaaaaa
              p.lead aaaaaaaaaa
            .col
              img(src="/wknd/image-2.png")
              h5.title aaaaaaaaaa
              p.lead aaaaaaaaaa
            .col
              img(src="/wknd/image-2.png")
              h5.title aaaaaaaaaa
              p.lead aaaaaaaaaa
            .col
              img(src="/wknd/image-2.png")
              h5.title aaaaaaaaaa
              p.lead aaaaaaaaaa

      section#next.section
        .container
          h3.section-title
            span Next Adventures

        .hero
          .hero-body.container
            h3.hero-title Climbing New Zealand
            p Let us help you make your New Zealand climbing vacation a memory you will cherish forever! Come join us for a guided rock climbing adventure in the mountains that trained Sir Edmund Hilary.
            a.btn-primary(href="") View trips

      .container
        section#where.section.border
          h4 Where do you want to go?
          .row
            .col
              img(src="/wknd/image-2.png")
              h5.title aaaaaaaaaa
              p.lead aaaaaaaaaa
            .col
              img(src="/wknd/image-2.png")
              h5.title aaaaaaaaaa
              p.lead aaaaaaaaaa
            .col
              img(src="/wknd/image-2.png")
              h5.title aaaaaaaaaa
              p.lead aaaaaaaaaa
            .col
              img(src="/wknd/image-2.png")
              h5.title aaaaaaaaaa
              p.lead aaaaaaaaaa

          a.btn-secondary(href="") View trips


    footer
      .container

</template>

<script lang="ts">
</script>

<style lang="scss">
  /*コンテンツ幅*/
  .container {
    padding-left: 2.5rem;
    padding-right: 2.5rem;
    margin-left: auto;
    margin-right: auto;
    max-width: 1164px;
    width: 100%;
  }

  /*ボタン共通*/
  .btn-primary, .btn-secondary {
    display: inline-block;

    line-height: 20px;
    text-align: center;
    text-decoration: none;

    padding-top: 1rem;
    padding-bottom: 1rem;
    padding-left: 40px;
    padding-right: 40px;
  }

  /*押してほしいボタン*/
  .btn-primary {
    background: #FFEB00;
    color: #202020;
  }

  /*まぁまぁ押してほしいボタン*/
  .btn-secondary {
    background: #202020;
    color: #FFFFFF;
  }

  /*大きいセクション*/
  .section {
    /*padding-bottom: 3rem;*/
    &:after{
      content: "";
      display: block;
      margin-top: 3rem;
    }
    margin-bottom: 4rem;
  }

  .section-title {
    color: #202020;
    margin-bottom: 3rem;

    span {
      display: block;
      margin-bottom: 12px;
    }

    &:after {
      content: "";
      display: block;
      width: 5rem;
      height: 2px;
      background: #FFE900;
    }
  }

  /*画面いっぱいのエリア*/
  .hero {
    background-size: cover;
    background-position: center center;
    padding-top: 400px;
  }

  .hero-body {
    background-color: #FFFFFF;
    padding-top: 20px;
    padding-bottom: 20px;
  }

  .hero-title {

  }

  .row {
    display: flex;
    margin-left: -1rem;
    margin-right: -1rem;
    margin-bottom: 3rem;

    .col {
      padding-left: 1rem;
      padding-right: 1rem;
      flex: 1;
    }
  }

  .border {
    border-bottom: 2px solid #EBEBEB;
  }

  /*個別の設定*/

  /*============================
  #mv
  ============================*/
  #mv {
    .hero {
      background-image: url("/wknd/image.png");

      .hero-body {
        .section-title {
        }
      }
    }
  }

  /*============================
  #last
  ============================*/
  #last {
    .body {
      background-color: #F7F7F7;
      display: flex;

      .body-left {
        padding: 20px;

        .section-title {
        }
      }

      .body-right {
      }
    }
  }

  /*============================
  #recent
  ============================*/
  #recent {
    .section-title {
    }

    .row {
      .col {
        .title {
        }

        .lead {
        }
      }
    }
  }

  /*============================
  #next
  ============================*/
  #next {
    .section-title {
    }

    .hero {
      background-image: url("/wknd/image-10.png");

      .hero-body {
      }
    }
  }

  /*============================
  #where
  ============================*/
  #where {
    .row {
      .col {
        .title {
        }

        .lead {
        }
      }
    }
  }
</style>
