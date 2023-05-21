<script lang="ts">
	import { browser } from "$app/environment";

    const colors = [
  "#7fffd4",
  "#9370d8",
  "#9370d8",
  " #cf743f",
  "#37b853",
  "#70a1d8",
  "#ad2f6a",
  "#b16323",
  "#311e88",
  "#1e7c88",
  "#d15115",
  "#1e3788",
  "#c5d115",
];

    if(browser){
        const blob=document.getElementById("blob")
        window.addEventListener("keydown",(e)=>{
            if(e.key==="Control"){
            blob?.style.setProperty("background",`linear-gradient(${colors[Math.floor(Math.random() * colors.length)]},${colors[Math.floor(Math.random() * colors.length + 1)]})`)
            }
        })
        window.onpointermove=(e)=>{
            const {clientX,clientY}=e
            blob?.animate({left:`${clientX}px`,top:`${clientY}px`},{duration:1000,fill:"forwards"})
        }
    }


</script>

<div class="blob" id="blob"/>

<style>
    .blob{
        width: 60vh;
        height: 60vh;
        background: linear-gradient(to bottom ,rgb(255, 17,135),rgb(93, 54, 172));
        aspect-ratio: 1;
        border-radius: 50%;
       animation: rotate 5s infinite;
       position: absolute;
       z-index: 0;
    }

    @keyframes rotate{
        0%{
            transform: rotate(90deg);
        }
        50%{
            transform: rotate(180deg);
        }
        100%{
            transform: rotate(360deg);
        }
    }

</style>