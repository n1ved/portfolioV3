<script>
    import './NavBar.css'
    import {base} from '$app/paths'

    function sleep() {
        return new Promise(resolve => setTimeout(resolve, 250));
    }

    function toggleMenu() {
        const menu = document.querySelector('.navbar')
        menu?.classList.toggle('active')
    }
    
    function toggleMenuOnLinks(){
        const menu = document.querySelector('.navbar')

        if(menu?.classList.contains('active')){
            sleep().then(() => {
                menu?.classList.remove('active')
            })
        }
    }
</script>
<div class="navbar-hamburger">
    <button class="menu-btn" on:click={toggleMenu}>
        MENU
    </button>
</div>
<div class="navbar">
    <div class="links">
        <a href="{base}/" on:click={toggleMenuOnLinks}>Home</a>
        <a href="{base}/about" on:click={toggleMenuOnLinks}>About</a>
        <a href="{base}/projects" on:click={toggleMenuOnLinks}>Projects</a>
        <a href="{base}/docs/resume.pdf" target="_blank" on:click={toggleMenuOnLinks}>Resume</a>
    </div>
    <div class="socials">
        <div>
            <h2>Socials</h2>
        </div>
        <div>
            <a href="https://github.com/n1ved/" target="_blank" on:click={toggleMenuOnLinks}>Github</a>
            <a href="https://linkedin.com/in/n1ved" target="_blank" on:click={toggleMenuOnLinks}>LinkedIn</a>
            <a href="https://fosstodon.org/@n1ved/" target="_blank" on:click={toggleMenuOnLinks}>Mastodon</a>
            <a href="https://t.me/n1vxd" target="_blank" on:click={toggleMenuOnLinks}>Telegram</a>
            <a href="mailto:n1ved@proton.me" target="_blank" on:click={toggleMenuOnLinks}>Email</a>
        </div>
    </div>
</div>