<script lang="ts">
	import Blob from "../components/Blob.svelte";

    let translation=0;

    function handleMouseMove(e:any){
        console.log(e)
        translation=e.clientX;
    }

</script>
<div class="viewbox">
    <div class="contentbox">
        <h1>Ikwue Inalegwu</h1>
    <p>FullStack Developer</p>
    </div>
</div>

<style>
    .viewbox{
        width:100%;
        height: 100%;
        display: flex;
        align-items: center;
        align-content: center;
        justify-content: center;
    }
    .contentbox{
        text-align: center;
        align-items: center;
        align-content: center;
        justify-content: center;
        display: flex;
        flex-direction: column;
        gap: 5px;
    }
    .contentbox>h1{
        font-size: 40px;
    }
    .contentbox>p{
        font-size: 20px;
    }
</style>