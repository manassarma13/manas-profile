<script>
  export let certificationsData;
  function hasCertificationLink(cert) {
    return cert.includes("http");
  }

  function getCertificationText(cert) {
    return hasCertificationLink(cert)
      ? cert.split(" ").slice(0, -1).join(" ")
      : cert;
  }

  function getCertificationLink(cert) {
    const parts = cert.split(" ");
    const lastPart = parts[parts.length - 1];
    if (lastPart.startsWith("http")) {
      return lastPart;
    }
    return "";
  }
</script>

<h2>Certifications</h2>
<ul>
  {#each certificationsData as cert (cert)}
    {#if hasCertificationLink(cert)}
      <li>
        <a href={getCertificationLink(cert)} target="_blank"
          >{getCertificationText(cert)}</a
        >
      </li>
    {:else}
      <li>{cert}</li>
    {/if}
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
