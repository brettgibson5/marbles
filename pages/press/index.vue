<template>
  <div class="Page PressDetail">
    <section class="hero is-info is-medium is-bold">
      <div class="hero-body">
        <div class="container has-text-centered">
          <h1 class="title">
            Press Releases
          </h1>
        </div>
      </div>
    </section>

    <div class="container">
      <!-- START ARTICLE FEED -->
      <section class="articles">
        <div class="column is-8 is-offset-2">
          <!-- START ARTICLE -->
          <div class="card article">
            <div class="card-content">
              <div class="media">
                <div class="media-content has-text-centered">
                  <p class="title article-title">
                    Week 1 Recap
                  </p>
                  <div class="tags has-addons level-item">
                    <span class="tag is-rounded is-info">@vtsweetlou</span>
                    <span class="tag is-rounded">June 22, 2020</span>
                  </div>
                </div>
              </div>
              <div class="content article-body">
                <p>
                  Hi Everyone, What a "crazy" first event, only a true maniac
                  would do well and that's exactly what the Minty Maniacs did.
                  They kept their balance and went the distance. Congratulations
                  to Kevin for his 3 picks (Raspberry Racers/Hero, O'Rangers,
                  Minty Maniacs) taking him into the #1 position for Event 1 and
                  winner of our first $5.00 weekly high score payout. Steve was
                  a close 2nd and Alex reached his way up to the podium with a
                  3rd place finish.
                </p>
              </div>
            </div>
          </div>
          <!-- END ARTICLE -->
        </div>
      </section>
      <!-- END ARTICLE FEED -->
    </div>
  </div>
</template>

<style lang="scss" scoped>
.hero-body {
  background-image: url('/img/bg.jpg');
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  height: 500px;
}
.articles {
  margin: 5rem 0;
  margin-top: -200px;
}
.articles .content p {
  line-height: 1.9;
  margin: 15px 0;
}
.author-image {
  position: absolute;
  top: -30px;
  left: 50%;
  width: 60px;
  height: 60px;
  margin-left: -30px;
  border: 3px solid #ccc;
  border-radius: 50%;
}
.media-center {
  display: block;
  margin-bottom: 1rem;
}
.media-content {
  margin-top: 3rem;
}
.article,
.promo-block {
  margin-top: 6rem;
}
div.column.is-8:first-child {
  padding-top: 0;
  margin-top: 0;
}
.article-title {
  font-size: 2rem;
  font-weight: lighter;
  line-height: 2;
}
.article-subtitle {
  color: #909aa0;
  margin-bottom: 3rem;
}
.article-body {
  line-height: 1.4;
  margin: 0 6rem;
}
.promo-block .container {
  margin: 1rem 5rem;
}
</style>
