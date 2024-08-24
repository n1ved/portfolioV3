<script>

    let lang = [
        'C',
        'C++',
        'HTML',
        'CSS',
        'JavaScript',
        'Dart'
    ]

    let frameworks = [
        'ReactJS',
        'NextJS',
        'Flutter',
    ]

    let experience = [
        {
            role : "Frontend Developer",
            org: 'ETHICVAL',
            start : '2023',
            end : 'Present'
        },
        {
            role : 'Tech Team Member',
            org: 'FOSSMEC',
            start : '2023',
            end : 'Present'
        },
        {
            role : 'Tech Trainee',
            org: 'TinkerHubMEC',
            start : '2023',
            end : 'Present'
        }
    ]
</script>

<div class="main">
    <h1 class="title">About</h1>
    <p class="desc">
        <b>Hi !</b><br/>
        I am Nived , A computer science student from Kerala . Currently in my third year of BTech Degree and exploring different technologies in this domain
        <br/>
    </p>

    <div class="skills">
        <h2>Technologies Known</h2>
        <ul>
            <li><b>Languages</b></li>
            {#each lang as l}
                <li>{l}</li>
            {/each}
        </ul>
        <ul>
            <li><b>Frameworks</b></li>
            {#each frameworks as l}
                <li>{l}</li>
            {/each}
        </ul>
    </div>
    <div class="experience">
        <h2>Experience</h2>
        <ul>
            {#each experience as l}
                <li>
                    <div><b>{l.role}</b>&nbsp;&nbsp;at&nbsp;&nbsp;{l.org}</div>
                    <div>{l.start} - {l.end}</div>
                </li>
            {/each}
        </ul>
    </div>
</div>

<style>
    .main {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        justify-content: center;
        max-width: 75vw;
        box-sizing: border-box;
        margin-top: 50px;
        margin-left: 50px;
    }

    .title {
        font-size: 86px;
        font-weight: 700;
    }

    .desc {
        font-size: 24px;
        font-family: ClashDisplay-Light, 'serif';
        font-weight: 300;
        width: 70%;

    }

    .skills{
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        width: fit-content;
        border: 1px solid black;
        font-size: 28px;
        margin: 50px 0;
    }

    .skills h2{
        padding: 10px;
        font-weight: 500;
    }

    .skills ul{
        list-style-type: none;
        padding: 0;
        margin: 0;
        display: flex;
        flex-direction: row;
        border-top: 1px solid black;
        font-size: 26px;
    }

    .skills ul li{
        padding: 10px;
        border-right: 1px solid black;
    }

    .skills ul li:first-child{
        width: 200px;
    }

    .skills ul li:last-child{
        border-right: none;
    }
    .experience{
        display: flex;
        flex-direction: column;
        margin: 50px 0;
        justify-content: space-between;
        width: 50vw;
        border: 1px solid black;
        font-size: 28px;
        font-weight: 200;
    }

    .experience h2{
        padding: 10px;
        font-weight: 500;
    }

    .experience ul{
        list-style-type: none;
        margin: 0;
        display: flex;
        flex-direction: column;
        font-size: 26px;
    }

    .experience ul li{
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        padding: 10px;
        border-top: 1px solid black;
    }

    @media screen and (max-width: 480px){
        .main {
            margin: 20px;
            max-width: 100vw;
        }
        .title {
            font-size: 48px;
        }

        .desc {
            font-size: 18px;
            width: 100%;
        }

        .skills{
            width: 100%;
            font-size: 20px;
            margin: 20px 0;
        }

        .skills ul , .experience ul{
            font-size: 18px;
            flex-wrap: wrap;
        }

        .skills ul li:first-child{
            width: 100%;
            border-right: none;
            border-bottom: 1px solid black;
            text-align: center;
        }

        .skills ul li{
            padding: 5px;
        }

        .experience{
            width: 100%;
            font-size: 18px;
            margin: 20px 0;
        }

        .experience ul li{
            padding: 5px;
        }
    }

</style>