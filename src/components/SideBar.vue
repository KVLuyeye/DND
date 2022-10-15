<template>
    <aside class="sidebar" id="sidebar">    
    <div class = "sideNav" id="sideNav">
          <a href="" class="nav"> <i class="fa-solid fa-house"></i></a> 
    </div>
  
</aside>
</template>

<style lang="scss">
#sidebar{
$layer1color: linear-gradient(to top, rgba(6, 5, 8, 0.902), rgba(6, 5, 8, 1));
min-height: 100vh;
        flex:0;
            display: flex;
            flex-direction: column;
            background-image: $layer1color;
            align-items:center;
            transition: 0.25s ease-out;
            align-items: flex-start;
        
            
        div {
        display: flex;
        justify-content:space-between;
        align-items: center;
        flex-direction: column;
        padding-left: 1rem;
        .nav{
        
            text-decoration: none;
            color: white;   
            padding-top: 1rem;
            
        } 
    }
}

</style>