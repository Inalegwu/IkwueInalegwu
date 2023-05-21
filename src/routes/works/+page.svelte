<script lang="ts">
    import {Github,Globe} from "lucide-svelte"
    function handleDrag(e:any){
        console.log(e)
    }
    const works=[
        {
            title:"ClipSync",
            description:"The Clipboard Mangager That Syncs",
            gitHubLink:"https://github.com/Inalegwu/ClipSync",
            websiteLink:"https://clipsync.com"
        },
        {
            title:"Instagram Creator",
            description:"Creator Specific Dashboard For Instagram",
            link:"https://github.com/Inalegwu",
            websiteLink:"https://github.com/Inalegwu"
        }
    ]
</script>

<div class="works">
    <div class="heading">
        <h1>I Love Building Cool Shit</h1>
    <p>Here's some things I'm building</p>
    </div>
    <div class="workscontainer">
        {#each works as work}
             <div class="workitem" on:drag={handleDrag}>
                 <h1>{work.title}</h1>
                 <p>{work.description}</p>
                 <div>
                    <a href={work.gitHubLink}>
                        <Github size={20}/>
                    </a>
                    <a href={work.websiteLink}>
                        <Globe size={20}/>
                    </a>
                 </div>
             </div>
        {/each}
    </div>
</div>

<style>
    .works{
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        align-content: center;
        justify-content: center;
        gap: 30px;
    }
    .heading{
        display: flex;
        flex-direction: column;
        align-items: center;
        align-content: center;
        gap:10px;
    }
    .heading>p{
        color: #222222ac;
    }
    .workscontainer{
        display: flex;
        gap: 10px;
        align-items: center;
        align-content: center;
        justify-content: center;
    }
    .workitem{
        border: 0.1px solid #ececec;
        padding: 10px;
        width: 300px;
        height: 200px;
        border-radius: 10px;
        gap: 10px;
        display: flex;
        flex-direction: column;
        align-items: center;
        align-content: center;
        justify-content:center;
        text-align: center;
        color: black;
    }
    .workitem>div{
        padding:10px;
        display: flex;
        align-items: center;
        align-content: center;
        justify-content:center;
        gap: 20px;
        width: 100%;
    }
    .workitem>div>a{
        color: rgba(38, 38, 38, 0.609);
        transition: 0.5s ease-out;
    }
    .workitem>div>a:hover{
        color: black;
    }
    .workitem>h1{
        font-size: 20px;
        pointer-events: none;
    }
    .workitem>p{
        font-size: 15px;
        color:#222222ac;
    }
    @media screen and (max-width:1024px){
        .works{
            width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
            align-content: center;
            justify-content: center;
            text-align: center;
        }
        .workscontainer{
            display: flex;
            flex-direction: column;
            gap:10px
        }
    }
</style>