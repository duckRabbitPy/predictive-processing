<script>
    export let link
</script>


<style>
    .button1{
    display:inline-block;
    padding:0.5em 3em;
    border:0.16em solid #FFFFFF;
    margin:0 0.3em 0.3em 0;
    box-sizing: border-box;
    text-decoration:none;
    text-transform:uppercase;
    font-family:'Roboto',sans-serif;
    font-weight:400;
    color:#153d33;
    text-align:center;
    transition: all 0.15s;}

    .button1:hover{
    color:#153d33;
    border-color:#153d33;}
    
    .button1:active{
    color: black;
    border-color: black;}

    @media all and (max-width:30em){
        .button1{
            display:block;
            margin:0.4em auto;}}
</style>

<a href="{link}" class="button1"><slot></slot></a>