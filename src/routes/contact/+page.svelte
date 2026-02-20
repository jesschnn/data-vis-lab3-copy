<svelte:head>
  <title>Contact me</title>
</svelte:head>

<nav>
    <ul>
        <li>
            <a href="./">Home</a>
        </li>
        <li>
            <a href="projects">Projects</a>
        </li>
        <li>
            <a class="current" href="contact">Contact</a>
        </li>
        <li>
            <a href="https://github.com/jesschnn" target="blank">GitHub Profile</a>
        </li>
        <li>
            <a href="resume">Resume</a>
        </li>
    </ul>
</nav>
<h1>Contact</h1>

<form action="mailto:jesschn@mit.edu" method="GET" class="wrapper">
    <label class="labelgrid">
        Email:
        <input name="email" type="email"/>
    </label>
    

    <label class="labelgrid">
        Subject:
        <input name="subject"/>
    </label>
    

    <label class="labelgrid">
        Body:
        <textarea name="body"></textarea>
    </label>
    
    <button>Send</button>
</form>