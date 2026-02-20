<script>
  import projects from "$lib/projects.json";
  import Project from "$lib/Project.svelte";
  import reading from "$lib/reading.json";
  import ReadingItem from "$lib/ReadingItem.svelte";
</script>


<nav>
    <ul>
        <li>
            <a class="current" href="./">Home</a>
        </li>
        <li>
            <a href="projects">Projects</a>
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

<h1>Jessica Chen</h1>


<div class="intro-section">
    <div class="intro">
        <p>Hi! I'm Jessica, and I like watching shows and taking naps.</p>
        <img src="images/jessica_jumping.JPG" alt="Picture of me jumping">
    </div>

    <div class="reading">
        <h2>What I'm Reading</h2>
        <div class="readings">
            {#each reading as b}
                <ReadingItem data={b} />
            {/each}
        </div>
    </div>
</div>
<hr>

<div class="project-highlights">
    <br>
    <h2>Latest Projects</h2>
    <br>

    <div class="projects">
        {#each projects.slice(0, 3) as p}
            <Project data={p} />
        {/each}
    </div>
</div>






<style>
    .intro-section {
        display: flex;
        gap: 2em;
    }

    .intro {
        flex: 1.25;
    }

    .reading {
        flex: 0.75;
        background-color: oklch(from var(--color-accent) 95% 5% h);
        padding: 1em;
    }
</style>


