<script>
  import { siteTitle } from '$lib/config';
  import me from '$lib/images/me.jpg';
  import Social from '$lib/components/Social.svelte';

  export let data;
</script>

<svelte:head>
  <title>{siteTitle}</title>
</svelte:head>

<div class="profile">
  <!-- <figure> -->
  <!--   <img src={me} alt='Incredibly handsome man wears glasses and poses handomsly.'/> -->
  <!-- </figure> -->
  <span>
    <svelte:component this={data.ReadMe} />
  </span>
</div>
<div class="profile-social">
  <Social />
</div>

<style>
  .profile {
    display: flex;
    justify-content: space-evenly;
    margin-bottom: 2rem;
  }
  .profile span {
    flex-basis: 85%;
  }

  @media (min-width: 48rem) {
    .profile span {
      flex-basis: 55%;
    }

    .profile-social {
      display: flex;
      justify-content: space-evenly;
    }
  }

  /* .profile { */
  /*   display: grid; */
  /*   grid-template-columns: 1fr; */
  /*   grid-template-rows: 1fr 2fr; */
  /*   justify-content: center; */
  /* } */
  /* .profile figure { */
  /*   grid-row-start: 2; */
  /*   grid-row-end: 3; */
  /*   text-align: center; */
  /* } */
  /* .profile img { */
  /*   border-radius: 15rem; */
  /*   object-fit: cover; */
  /*   width: 100%; */
  /*   max-width: 200px; */
  /* } */

  /* @media (min-width: 48rem) { */
  /*   .profile { */
  /*     grid-template-columns: repeat(2, 1fr); */
  /*     grid-template-rows: 1fr; */
  /*     justify-content: start; */
  /*   } */
  /*   .profile figure { */
  /*     grid-row-start: 1; */
  /*     grid-row-end: 2; */
  /*   } */
  /*   .profile img { */
  /*     max-width: 400px; */
  /*   } */
  /* } */
</style>
