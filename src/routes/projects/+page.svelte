<svelte:head>
  <title>Projects</title>
</svelte:head>

<script>
  import projects from "$lib/projects.json";
  import Project from "$lib/Project.svelte";
</script>

<nav>
    <ul>
        <li>
            <a href="./">Home</a>
        </li>
        <li>
            <a class="current" href="projects">Projects</a>
        </li>
        <li>
            <a href="contact">Contact</a>
        </li>
        <li>
            <a href="https://github.com/jesschnn" target="blank">GitHub Profile</a>
        </li>
        <li>
            <a href="resume">Resume</a>
        </li>
    </ul>
</nav>
<h1>{projects.length} Projects</h1>
<hr>

<div class="projects">
  {#each projects as p}
    <Project data={p} />
  {/each}
</div>