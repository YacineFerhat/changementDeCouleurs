<template>
    <div ccslass="container">
        <div class="row">
            <div class="col-xs-12">
                <br>
                <button class="btn btn-primary" @click="selectedComponent='appBlue'">
                    Load Blue color
                </button>
                <button class="btn btn-success" @click="selectedComponent='appGreen'">
                    Load red green
                </button>            
                <button class="btn btn-danger" @click="selectedComponent='appRed'">
                    Load Green color
                </button>
                <hr>
                <component :is="selectedComponent">
                        <p>This is the content</p>
                </component>
            </div>
        </div>     
    </div>    
</template>

<script>

import Blue from './components/Blue.vue';
import Green from './components/Green.vue';
import Red from './components/Red.vue';

export default {
    data : function (){
        return {
            selectedComponent :'appBlue'
        }
    },
    components :{
        appBlue : Blue,
        appGreen : Green,
        appRed: Red
    }
}
</script>

<style>

</style>
