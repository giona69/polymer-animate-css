# polymer-animate-css
Animate.css style import for Polymer

based on:
[Animate.css](https://daneden.github.io/animate.css/)

# install
bower install --save polymer-animate-css

# usage
import the polyerm-animate-css html module
include in the template styles
add animate css classes to html elements you want to animate

<link rel="import" href="../bower_components/polymer-animate-css/polymer-animate-css.html">

<dom-module id="my-polymer-module">
    <template>
        <style include="polymer-animate-css"></style>
        <style>
            :host {
                display: block;
                text-align: center;
                width: 100%;
            }
        </style>

        <div id="my-div" class="animated bounce">
            Animate Me
        </div>
    </template>

    <script>
        class MyPolymerModule extends Polymer.Element {
            static get is() {
                return 'my-polymer-module';
            }
        }

        window.customElements.define(MyPolymerModule.is, MyPolymerModule);
    </script>
</dom-module>
