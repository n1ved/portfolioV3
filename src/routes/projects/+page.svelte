<script>
    const projects = [
        {
            name : "Skyze",
            desc : "A simple and elegant weather app",
            tech : ["Flutter","OpenWeatherAPI"],
            gh   : "https://github.com/n1ved/skyze",
            down : "https://github.com/n1ved/skyze/releases/latest",
            isLive : false
        },
        {
            name : "0xC",
            desc : "A client to upload and keep track of files in 0x0 instance",
            tech : ["Flutter","Hive"],
            gh   : "https://github.com/n1ved/0xC",
            down : "https://github.com/n1ved/0xC/releases/latest",
            isLive : false
        },
        {
            name : "nearPG",
            desc : "A simple hostel finder app with user uploaded data",
            tech : ["ReactJS","Firebase"],
            gh   : "https://github.com/n1ved/nearpg",
            down : "https://nearpg.vercel.app",
            isLive : true
        },
        {
            name : "nCrypter",
            desc : "C++ ASCII Based text cyphering tool",
            tech : ["C++"],
            gh   : "https://github.com/n1ved/ncrypter",
            down : "https://github.com/n1ved/ncrypter/releases/latest",
            isLive: false
        }
    ]
</script>
<div class="main">
    <h1 class="title">Projects</h1>
    <div class="projects">
        {#each projects as p}
            <div class="project">
                <h2>{p.name}</h2>
                <div class="project-hover">
                    <p>{p.desc}</p>
                    <div class="blank"></div>
                    <div class="tech">
                        <b>Made With </b>
                        {#each p.tech as t}
                            <span>{t}</span>
                            {#if p.tech.length > 1}
                                {#if t !== p.tech[p.tech.length -1] && t !== p.tech[p.tech.length - 2]}
                                    <span>,</span>
                                {/if}
                                {#if t === p.tech[p.tech.length - 2]}
                                    <span> &amp; </span>
                                {/if}
                            {/if}
                        {/each}
                    </div>
                    <div class="links">
                        <a href={p.gh} target="_blank">Github</a>
                        <a href={p.down} target="_blank">
                            {#if p.isLive}
                                Live
                            {:else}
                                Download
                            {/if}
                        </a>
                    </div>
                </div>
            </div>
        {/each}
    </div>
    <div class="footer">
        Find More on <b>Github</b>
    </div>
</div>

<style>
    .main {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        justify-content: flex-start;
        max-width: 75vw;
        min-height: 100vh;
        box-sizing: border-box;
        margin-top: 50px;
    }

    .title {
        font-size: 86px;
        font-weight: 700;
        margin-left: 50px;
    }

    .projects{
        width: 75vw;
        margin-top: 30px;
        box-sizing: border-box;
        border-top: 1px solid black;
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
    }

    .project{
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        height: 200px;
        border-bottom: 1px solid black;
        border-right: 1px solid black;
        font-size: 32px;
    }

    .project:nth-child(2n){
        background-color: #1E1E1E0F;
    }

    .project:nth-child(3n){
        border-right: 0;
    }
    .project:hover h2{
        display: none;
    }
    .project-hover{
        opacity: 0;
        display: none;
    }

    .project:hover .project-hover{
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        justify-content: flex-end;
        min-height: 200px;
        width: 100%;
        font-size: 20px;
        box-sizing: border-box;
        opacity: 1;
        transition: opacity 0.5s;
        transition-delay: 0.5s;
    }
    .project-hover p{
        padding: 10px;
        justify-self: flex-start;
    }
    .blank{
        height: 100%;
        width: 100%;
    }
    .tech{
        justify-self: flex-end;
        padding: 10px;
    }

    .links{
        display: flex;
        flex-direction: row;
        justify-content: space-evenly;
        width: 100%;
        height: fit-content;
        border-top: 1px solid black;

    }
    .links a{
        width: 100%;
        text-align: center;
        text-decoration: none;
        color: black;
        font-size: 24px;
        font-weight: 400;
        padding: 10px;
    }

    .links a:first-child{
        border-right: 1px solid black;
    }

    .links a:hover{
        transition: all 0.5s;
        background-color: black;
        color: #FDF4DC;
    }
    .footer{
        align-self: center;
        padding-top: 50px;
    }


</style>