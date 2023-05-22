<script lang="ts">
    import {Instagram,Github,Linkedin,Twitter} from "lucide-svelte"
</script>
<div class="contactbox">
    <h1>Feel Free To Stalk Me , Just Don't Do Anything Weird</h1>
    <div class="medialinks">
        <a href="https://instagram.com/CasuallyProperPortraits" target="_blank">
            <Instagram size={20}/>
        </a>
         <a href="https://github.com/Inalegwu" target="_blank">
            <Github size={20}/>
        </a>
         <a href="" target="_blank">
            <Twitter size={20}/>
        </a>
         <a href="" target="_blank">
            <Linkedin size={20}/>
        </a>
    </div>
</div>

<style>
    .contactbox{
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        align-content: center;
        justify-content: center;
        text-align: center;
        gap:20px;
    }
    .contactbox>h1{
        font-size: 20px;
    }
    .medialinks{
        display: flex;
        gap: 20px;
        align-items: center;
        align-content:center;
        justify-content: center;
    }
    .medialinks>a{
        color: #000000a0;
        background: white;
        padding: 10px;
        border-radius: 5px;
        display: flex;
        align-items: center;
        align-content: center;
        justify-content: center;
        transition: 0.5s ease-in-out;
    }
    .medialinks>a:hover{
        color: black;
        transform: rotate(-5deg);
    }
</style>