
# ![deklok](https://deidee.com/logo.svg?str=deklok)

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 300 300" style="background:transparent">
    <title>deklok</title>
    <defs>
        <rect id="deklok__hour-mark" fill="lime" fill-opacity=".5" stroke="black" stroke-width="2" height="24" width="16" x="142" y="0"/>
    </defs>
    <rect x="0" y="0" fill="none" height="300" width="300"/>
    <circle cx="150" cy="150" r="150" fill="none"/>
    <use href="#deklok__hour-mark" transform="rotate(0)" transform-origin="center"/>
    <use href="#deklok__hour-mark" transform="rotate(30)" transform-origin="center"/>
    <use href="#deklok__hour-mark" transform="rotate(60)" transform-origin="center"/>
    <use href="#deklok__hour-mark" transform="rotate(90)" transform-origin="center"/>
    <use href="#deklok__hour-mark" transform="rotate(120)" transform-origin="center"/>
    <use href="#deklok__hour-mark" transform="rotate(150)" transform-origin="center"/>
    <use href="#deklok__hour-mark" transform="rotate(180)" transform-origin="center"/>
    <use href="#deklok__hour-mark" transform="rotate(210)" transform-origin="center"/>
    <use href="#deklok__hour-mark" transform="rotate(240)" transform-origin="center"/>
    <use href="#deklok__hour-mark" transform="rotate(270)" transform-origin="center"/>
    <use href="#deklok__hour-mark" transform="rotate(300)" transform-origin="center"/>
    <use href="#deklok__hour-mark" transform="rotate(330)" transform-origin="center"/>
    <rect id="deklok__second-hand" x="149" y="10" height="140" width="2" transform-origin="center"/>
    <rect id="deklok__minute-hand" x="148" y="30" height="120" width="4" transform-origin="center"/>
    <rect id="deklok__hour-hand" x="146" y="50" height="100" width="8" transform-origin="center"/>
    <script>
        <![CDATA[
        "use strict";

        const deklok__secondHand = document.getElementById('deklok__second-hand');
        const deklok__minuteHand = document.getElementById('deklok__minute-hand');
        const deklok__hourHand = document.getElementById('deklok__hour-hand');

        function setTime() {
            let date = new Date();
            let [hours, minutes, seconds] = [
                date.getHours(),
                date.getMinutes(),
                date.getSeconds(),
            ];

            deklok__hourHand.setAttribute('transform', 'rotate(' + (360 / 12 * (hours % 12)) + ')');
            deklok__minuteHand.setAttribute('transform', 'rotate(' + (360 / 60 * minutes) + ')');
            deklok__secondHand.setAttribute('transform', 'rotate(' + (360 / 60 * seconds) + ')');
        }

        let timer = setInterval( setTime, 1000);

        ]]>
    </script>
</svg>