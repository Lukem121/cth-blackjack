<script>
    export let value;
    export let showBack = false;
    export let bt = 0;

    let path = value;
    let backTypes = ["back1", "back2", "back3", "back4"]

    const handleClick = () => {
        showBack = !showBack;
        if(showBack){
            path = backTypes[bt];
        }else{
            path = value;
        }
    }

</script>

<div on:click={handleClick} class="cursor-pointer">
    <img class="w-56 h-56 rounded" src="./cards/{path}.svg" alt="">
</div>