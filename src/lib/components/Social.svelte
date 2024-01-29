<script lang="ts">
  import linkedin from '$lib/images/in.png';
  import mastodon from '$lib/images/mastodon.svg';
  import x from '$lib/images/x.png';
  import github from '$lib/images/github.svg';
</script>

<div class="social">
  <a href="https://linkedin.com/in/jimmy-hogoboom" target="_blank">
    <img src={linkedin} alt="LinkeIn Logo" />
  </a>
  <!-- <a href='https://mastodon.social'><img src={mastodon} alt='Mastodon Logo' /></a> -->
  <!-- <a href="https://twitter.com"><img src={x} alt="Twitter Logo" /></a> -->
  <a href="https://github.com/jimmyhogoboom" target="_blank">
    <img src={github} alt="Github Logo" />
  </a>
</div>

<style>
  .social {
    display: flex;
    justify-content: space-evenly;
    gap: 20px;
  }
  .social a {
    flex-basis: 50px;
    width: 100%;
  }

  @media (min-width: 48rem) {
    .social {
      gap: 80px;
    }
  }
</style>
