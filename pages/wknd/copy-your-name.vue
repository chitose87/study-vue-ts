<template lang="html">
  <div>
    <header>
      <div class="container">
        <h1>WKND</h1>
      </div>
    </header>

    <main>

      <section id="mv" class="section">
        <div class="hero">
          <div class="hero-body container">

          </div>
        </div>
      </section>

      <div class="container">
        <section id="last" class="section">
          <div class="body">
            <div class="body-left">

            </div>
            <div class="body-right">
              <img src="/wknd/image-1.png">
            </div>
          </div>
        </section>

        <section id="recent" class="section">
          <div class="row">
            <div class="col">
              <img src="/wknd/image-2.png">
              <h5 class="title">aaaaaaaaaa</h5>
              <p class="lead">aaaaaaaaaa</p>
            </div>
            <div class="col">
              <img src="/wknd/image-2.png">
              <h5 class="title">aaaaaaaaaa</h5>
              <p class="lead">aaaaaaaaaa</p>
            </div>
            <div class="col">
              <img src="/wknd/image-2.png">
              <h5 class="title">aaaaaaaaaa</h5>
              <p class="lead">aaaaaaaaaa</p>
            </div>
            <div class="col">
              <img src="/wknd/image-2.png">
              <h5 class="title">aaaaaaaaaa</h5>
              <p class="lead">aaaaaaaaaa</p>
            </div>
          </div>
        </section>
      </div>

      <section id="next" class="section">
        <div class="container">
          <h3 class="section-title">
            <span>Next Adventures</span>
          </h3>
        </div>
        <div class="hero">

        </div>
      </section>

      <div class="container">
        <section id="where" class="section">
          <div class="row">

          </div>
        </section>
      </div>
    </main>

    <footer>
      <div class="container">

      </div>
    </footer>
  </div>

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
  }

  /*押してほしいボタン*/
  .btn-primary {
    /*background: ;*/
    /*color: ;*/
  }

  /*まぁまぁ押してほしいボタン*/
  .btn-secondary {
  }

  /*大きいセクション*/
  .section {
    /*padding-bottom: 3rem;*/
    &:after {
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
      /*background-image: url("/wknd/image.png");*/

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
      //background-image: url("");

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
