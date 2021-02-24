<script>
    export let value;
    export let showBack = false;
    export let bt = 0;

    let path = value;
    let backTypes = ["back1", "back2", "back3", "back4"]

    const back = () => {
        if(showBack){
            path = backTypes[bt];
        }else{
            path = value;
        }
    }

    const handleClick = () => {
        showBack = !showBack;
        back();
    }

    back();

</script>

<img on:click={handleClick} class="w-56 cursor-pointer rounded" src="./cards/{path}.svg" alt="">
