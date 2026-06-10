<template>
  <q-page class="artist-page">
    <div class="artist-wrapper">
      <div class="artist-card">
        <div class="artist-text">
          <p>
            This page gathers my ongoing artistic work, including photographic
            series, musical projects, performances, and experiments.
          </p>

          <p>
            Explore my
            <a href="https://vsco.co/per-lentes-meas/gallery">Photography</a>,
            and check out my
            <a href="https://linktr.ee/placeholder.phc">Music</a>
          </p>

          <p>
            For collaborations, exhibitions, performances, or commissions, feel
            free to get in touch.
          </p>
        </div>
      </div>
    </div>
  </q-page>
</template>

<style>
.artist-page {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 48px 24px;

  background: #0b0c10;
  color: #e6e6e6;
}

.artist-wrapper {
  width: 100%;
  max-width: 820px;
}

.artist-card {
  padding: 52px 40px;

  background: rgba(255, 255, 255, 0.03);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 16px;

  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);

  box-shadow: 0 20px 60px rgba(0, 0, 0, 0.6);
}

.artist-text {
  font-size: 18px;
  line-height: 1.85;
  letter-spacing: 0.2px;

  color: rgba(255, 255, 255, 0.85);
}

.artist-text p {
  margin: 0 0 18px 0;
}

.artist-text a {
  color: #ffffff;
  text-decoration: none;

  border-bottom: 1px solid rgba(255, 255, 255, 0.35);
  transition: border-color 0.2s ease, opacity 0.2s ease;
}

.artist-text a:hover {
  border-color: rgba(255, 255, 255, 0.85);
  opacity: 0.8;
}

/* responsive */
@media (max-width: 768px) {
  .artist-card {
    padding: 32px 22px;
  }

  .artist-text {
    font-size: 16px;
    line-height: 1.75;
  }
}

@media (max-width: 480px) {
  .artist-page {
    padding: 24px 16px;
  }

  .artist-card {
    padding: 22px 18px;
  }
}
</style>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "ArtistPage",
});
</script>
