<script>
export default {
    data() {
        return {
            message: ""
        }
    },

    methods: {
            onSubmit(e) {
            this.message = e.target.value;
            e.preventDefault(); 
            }
        
    }
}
</script>

<template>

<aside class="channel-sidebar">
    <div id="liveChat">
        Live Chat
        <p>{{ message }}</p>
        <div id="enterBar">
            <form> 
                <input type="text" :value="message"  placeholder="How are you ?" id="text-Bar">
                <input type="submit" @submit="onSubmit" value="Send">
            </form>
        </div>
    </div>
</aside>
</template>

<style lang="scss">

$remsize-mar: 3rem ;
$remsize-pad: 1rem; 
$layer2color: linear-gradient(to bottom, rgba(6, 5, 8, 0.154), rgb(67, 66, 68, 1));
$layer1color: linear-gradient(to top, rgba(6, 5, 8, 0.902), rgba(6, 5, 8, 1));
$layer0color: #050506;

.channel-sidebar{
                    flex: 0.75;
                    order: 3;
                   background-image:$layer1color;
                    text-align: center;
                    color: white;
                       display: flex;
                       flex: 1;
                       min-height: 100vh; 

                        #liveChat{
                            flex: 1;
                            background-image:$layer2color; 
                            border-radius: 16px;
                            transition: 0.5s ease-in-out;
                            margin-bottom: $remsize-mar;
                            margin-right: 1rem;

                                display: flex;
                                align-items: stretch;
                                justify-content:space-between;
                                flex-direction: column;
                            

                            #enterBar{
                                display: flex;
                                align-items: center; 
                                background-image: $layer1color;
                                z-index: 2;
                                border-bottom-left-radius: 16px;
                                border-bottom-right-radius: 16px;
                                padding: 0.75rem;
                                opacity: 0.75;
                                justify-content: center;
                                &:hover {
                                    opacity: 1;
                                    }

                                    form {
                                        display: flex;
                                        margin-top: 0em;
                                        width: 100%;

                                        input[type = text]  {
                                            border: none;
                                            border-radius: 16px;
                                            padding: 0.75rem;
                                            width: 85%;
                                            text-align:start;
                                            background-image:$layer0color;
                                            transition: 0.5s ease-in;
                                            margin: 0;
                                        
                                        }
    
                                        input[type = submit]  {
                                            border: none;
                                            border-radius: 64px;
                                            padding: 0.5rem;
                                            transition: 0.25s ease-in;
                                            opacity: 0.75;
                                            
                                            &:hover {
                                                opacity: 1;
                                            }
                                            
                                        }
                                    }

                                }
                            }
                        }

</style>