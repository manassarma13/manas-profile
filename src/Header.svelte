<script>
  export let name;
  export let title;
  export let phone;
  export let email;
  export let linkedin;
  export let github;
  export let location;
</script>

<main>
  <h1>{name}</h1>
  <h2>{title}</h2>
  <ul>
    <li>Phone: {phone}</li>
    <li>Email: {email}</li>
    <li>LinkedIn: <a href="https://www.{linkedin}" target="_blank">{linkedin}</a></li>
    <li>GitHub: <a href="https://www.{github}" target="_blank">{github}</a></li>
    <li>Location: {location}</li>
  </ul>
</main>
