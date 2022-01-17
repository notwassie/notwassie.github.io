<main class="container">
  <div class="container__flex-flow">
    <div class="card">
      <img src="https://cdn.pixabay.com/photo/2016/11/29/08/41/apple-1868496_960_720.jpg" alt="">
    </div>
    <div class="card">
      <img src="https://cdn.pixabay.com/photo/2015/01/08/18/25/desk-593327_960_720.jpg" alt="">
    </div>
    <div class="card">
      <img src="https://cdn.pixabay.com/photo/2016/03/26/13/09/workspace-1280538_960_720.jpg" alt="">
    </div>
    <div class="card">
      <img src="https://cdn.pixabay.com/photo/2016/03/26/13/09/cup-of-coffee-1280537_960_720.jpg" alt="">
    </div>
    <div class="card">
      <img src="https://cdn.pixabay.com/photo/2017/11/27/21/31/computer-2982270_960_720.jpg" alt="">
    </div>
    <div class="card">
      <img src="https://cdn.pixabay.com/photo/2015/06/24/15/45/hands-820272_960_720.jpg" alt="">
    </div>
    <div class="card">
      <img src="https://cdn.pixabay.com/photo/2016/06/28/05/10/laptop-1483974_960_720.jpg" alt="">
    </div>
    <div class="card">
      <img src="https://cdn.pixabay.com/photo/2016/02/17/15/37/laptop-1205256_960_720.jpg" alt="">
    </div>
    <div class="card">
      <img src="https://cdn.pixabay.com/photo/2015/06/24/16/36/office-820390_960_720.jpg" alt="">
    </div>
    <div class="card">
      <img src="https://cdn.pixabay.com/photo/2017/10/10/21/47/laptop-2838921_960_720.jpg" alt="">
    </div>
    <div class="card">
      <img src="https://cdn.pixabay.com/photo/2017/06/23/11/49/laptop-2434393_960_720.jpg" alt="">
    </div>
    <div class="card">
      <img src="https://cdn.pixabay.com/photo/2015/09/04/23/28/wordpress-923188_960_720.jpg" alt="">
    </div>
  </div>
</main>

<style>
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

:root {
  --full-width: 100%;
  --max-width: 62.5rem;
  --min-width: 22.5rem;
  --flex-flow: 30rem;
  --space: 1rem;
  --conditional-space: clamp(0px, (30rem - 100%) * 999, 1rem);
}

body {
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  background: linear-gradient(
    45deg,
    hsl(236, 100%, 80%, 0.4),
    rgba(205, 155, 225, 0.3)
  );
}

.container {
  width: clamp(var(--flex-flow), 95%, var(--max-width));
  padding-block: var(--space);
  min-width: var(--min-width);
}

.container__flex-flow {
  display: flex;
  flex-wrap: wrap;
  gap: var(--space);
  margin-inline: var(--conditional-space);
}

.container__flex-flow > * {
  flex-grow: 1;
  flex-basis: calc((var(--flex-flow) - var(--full-width)) * 999);
}

.card {
  display: flex;
  min-width: 12rem;
  overflow: hidden;
  border-radius: clamp(0px, (40vw - var(--full-width)), var(--space));
  box-shadow: rgb(40, 40, 40, 0.1) 0px 2px 3px, rgb(20, 20, 20, 0.2) 0px 5px 8px,
    rgb(0, 0, 0, 0.25) 0px 10px 12px;
}

.card > img {
  display: block;
  object-fit: cover;
  width: 100%;
  /* aspect-ratio: 16 / 9; */
  transition: transform 700ms ease;
}

.card:hover img {
  transform: scale(1.2);
}

</style>
