<script>
  export let skillsData;
</script>

<h2>Skills</h2>
<ul>
  {#each skillsData as skill (skill)}
    <li>{skill}</li>
  {/each}
</ul>

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
</style>
