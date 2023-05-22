<script lang="ts">
    import "../app.css";
	import Blob from "../components/Blob.svelte";
</script>

<main>
    <head>
        <title>Ikwue Inalegwu</title>
    </head>
    <Blob/>
    <div class="body">
        <div class="navbar">
            <span class="infobox">Hit Ctrl To See A Cool Effect</span>
            <ul class="navlinks">
                <li><a href="/">Home</a></li>
                 <li><a href="/works">Works</a></li>
                 <li><a href="/blog">Blog</a></li>
                 <li><a href="/contact">Contact Me</a></li>
            </ul>
        </div>
        <slot/>
    </div>
</main>


<style>
    .body{
        width: 100%;
        height: 100vh;
        background: transparent;
        backdrop-filter: blur(250px);
    }
    .navbar{
        width: 100%;
        height:9vh;
        padding: 20px;
        display: flex;
        align-items: center;
        align-content: center;
        justify-content: space-between;
        position: absolute;
    }
    .infobox{
        cursor: pointer;
        font-size: 14px;
        color: #ecececec;
        padding: 10px;
        background: transparent;
        backdrop-filter: blur(10px);
        border: 0.1px solid #d3d3d367;
        border-radius: 5px;
        font-weight: bold;
    }
    .navlinks{
        display: flex;
        align-items: center;
        align-content: center;
        justify-content: flex-end;
        gap:15px;
        list-style-type: none;
        width: 30%;
    }
    a{
        color: gainsboro;
        font-weight: 500;
        transition: 0.5s ease-in-out;
    }
    a:hover{
        color:black;
    }
    @media screen and (max-width:1024px){
        .infobox{
            font-size: 8px;
        }
        .body{
            backdrop-filter: blur(400px);
        }
        .navlinks{
            width: 50%;
            font-size: 10px;
        }
    }
</style>