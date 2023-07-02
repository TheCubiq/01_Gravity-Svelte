<script>
	import Folder from "./folder.svelte";

    let langs = [
        { name: "js", icon: "js" },
        { name: "ts", icon: "ts" },
        { name: "svelte", icon: "svelte" },
        { name: "stylus", icon: "stylus" },
        { name: "html", icon: "html"}
    ]

    let toggled = false
</script>

<div class="contentWrapper">
    <Folder>
        {#each langs as lang}
            <div class="file">{lang.icon}</div>
        {/each}
    </Folder>
</div>

<style lang="stylus" type="text/stylus">    


    .contentWrapper
        display flex
        position relative
        height 100%
        // width 100%
        color #fff
        font-family 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif
        
        padding-left 10%

        justify-content center
        align-items center
</style>
