<script>
  export let position;
  export let company;
  export let date;
  export let description;
  export let skills;
</script>

<div>
  <h3>{position}</h3>
  <p class="company">{company}, {date}</p>
  <ul>
    {#each description
      .split("\n")
      .filter((line) => line.trim() !== "") as line (line)}
      <li>{line.replace(/^\s*-\s*/, "")}</li>
    {/each}
  </ul>
  <p class="skills">Skills: {skills}</p>
</div>

<style>
  ul {
    margin-left: 1rem;
  }
  @media (max-width: 767px) {
    ul {
      margin-left: 0;
      padding-left: 1rem;
    }
  }
  .skills {
    margin-left: 2rem;
  }
  .company {
    font-weight: 700;
    font-size: 0.8rem;
  }
</style>
