<script>
  import Section1 from "./section1.svelte";
  import Section2 from "./section2.svelte";
  import { onMount } from "svelte";
  export let date;
  onMount(async () => {
    const res = await fetch("/api/date");
    const newDate = await res.text();
    date = newDate;
  });
</script>

<div class="main">
  <section id="home" class="full-screen-section">
    <div class="header">
      <a class="nav-link" href="#section-1">Section 1</a>
      <a class="nav-link" href="#section-2">Section 2</a>
    </div>

    <h1>COMORKING YAT</h1>

  </section>
  <Section1 />
  <Section2 />
</div>
