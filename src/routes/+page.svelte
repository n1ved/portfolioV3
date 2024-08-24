<script>

</script>

<div>
    <h1 class="name">Nived</h1>

    <p class="home_desc">
        Hi I’m Nived , Third year <span>Computer Science Engineering</span> student at <span>Govt. Model Engineering College</span>

        <span class="sep"></span>

        I like to work with <span>Front End</span> and <span>Mobile App Development</span> and currently learning other programming technologies
    </p>
</div>

<style>
    div{
        max-width: 75vw;
        height: 100vh;
        box-sizing: border-box;
        padding: 50px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: flex-start;
    }
    .name{
        font-size: 200px;
    }
    .sep{
        display: block;
        width: 100%;
        height: 2px;
        margin: 5px 0;
    }
    .home_desc{
        width: 70%;
        font-size: 24px;
        font-family: ClashDisplay-Light,'serif';
        font-weight: 300;
    }
    span{
        font-weight: 600;
    }

    @media screen and (max-width: 480px){
        div{
            align-items: center;
            max-width: 100vw;
            max-height: 90vh;
            padding: 20px;
            box-sizing: border-box;
        }
        .name{
            font-size: 120px;
            text-align: center;
        }
        .home_desc{
            font-size: 16px;
            width: 100%;
            text-align: center;
        }
    }
</style>