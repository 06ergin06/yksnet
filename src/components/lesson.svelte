<script>
    export let name = "";
    export let saltdogru;
    export let saltyanlis;
    export let net = 0;
    function netHesap(){
        let yanlis = saltyanlis * 0.25
        net = saltdogru - yanlis;
    }
 
</script>
<div class="my-5">
    <h3 class="text-xl">{name}</h3>
    <input placeholder="Doğru" bind:value={saltdogru} class="input" type="text">
    <input placeholder="Yanlış" on:change={netHesap} bind:value={saltyanlis} class="input" type="text">
    <div class="border-2 border-gray-800 rounded px-2">
        {net} net
    </div>
</div>
