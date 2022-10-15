
<template>

    <div class="head-wrapper">
            <div id="buttonDIV">
                <button type="button" class="action-btn" id= "menu-btn" aria-label="MenuButton" @click="">
                    MENU
                </button>
            </div> 
            <div id = "channels">
                <div>
                    <a href="" class="head-nav"> FOR YOUR LOVE </a>
                </div>
                <div>
                    <a href="" class="head-nav"> FOR YOUR SOUL </a>
                </div>
            </div>
    
            <div id="logOut">
                <button class="head-nav"> LOG OUT </button>
            </div>
        </div>
    
    </template>

    <script>

    </script>

<style lang="scss">

        .head-wrapper {
            display:flex; 
            min-height: 2.5vh;
            background-color: #060508;
            flex-direction: row;
            align-items: center;
            justify-content: space-between;
            
            .head-nav {
                text-decoration: none;
                color: white;  
                opacity: 0.75;

            }
             

                    &:hover{ 
                        opacity: 1;
                    } 
                       

            div{
                color:white;
                border-radius: 16px;
                transition: 0.5s ease-in-out;
            } 

            #logOut{
                margin-right: 2rem;
            }

            #channels { 
                display: flex;
                flex-direction: row;
                flex: 1;
                justify-content: space-evenly;
            }

            #buttonDIV {
                flex: 0;
                margin-right: 1rem;
            }            

            #menu-btn {
                flex: 0 ;
                border: none;
                background-color:inherit;
                color: white;
                cursor: pointer;
                font-size: large;
                flex: none;
                opacity: 0.75; 
            }
                
                    &:hover {
                    opacity: 1; 
                }
        }
                    
</style>