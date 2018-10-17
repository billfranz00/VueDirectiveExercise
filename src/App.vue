<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
                <h1 v-myon:click="letsGo">Directives Exercise</h1>
                <!-- Exercise -->
                <!-- Build a Custom Directive which works like v-on (Listen for Events) -->

            </div>
        </div>
    </div>
</template>

<script>
    export default {
        directives: {
            'myon': {
                bind(el, binding) {
                    var content = el.innerText;
                    el.addEventListener(binding.arg, function() {binding.value(content)});
                }
            }
        },
        methods: {
            letsGo(NEwmessage) {
                var OGmessage = "Let's Go!!!";
                if(NEwmessage) {
                    OGmessage = NEwmessage;
                }
                alert(OGmessage);
            }
        }
    }
</script>

<style>
</style>
