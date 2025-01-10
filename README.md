# customize-google-landing

```js
// ==UserScript==
// @name         Expand Google Home Icons
// @namespace    http://tampermonkey.net/
// @version      2025-01-10
// @description  try to take over the world!
// @author       You
// @match        https://www.google.com.hk/
// @icon         https://www.google.com/s2/favicons?sz=64&domain=google.com.hk
// @grant        none
// ==/UserScript==

(function() {
    'use strict';

    setTimeout(()=>{
        main();
        document.querySelector("body > div.L3eUgb").style.backgroundColor = "bisque";
    }, 100)

    function main(){
        const btnContainer = document.createElement('div');
        btnContainer.style.display = "flex";
        btnContainer.style.justifyContent = "space-between";
        btnContainer.style.listStyle = "none";
        btnContainer.style.position = "fixed";
        btnContainer.style.top = 0;
        btnContainer.style.padding = "20px";
        btnContainer.style.color = "white";
        btnContainer.style.zIndex = "999";

        btnContainer.innerHTML = `
    <a href="https://mail.google.com/mail/?authuser=0" style="background-color: darkorange; font-size: 1.25rem; margin-left: 15px; font-weight: bold; padding: 5px 10px; color: white; text-decoration: none; border-radius: 8px;">Gmail</a>
    <a href="https://calendar.google.com/calendar?authuser=0" style="background-color: darkorange; font-size: 1.25rem; margin-left: 15px; font-weight: bold; padding: 5px 10px; color: white; text-decoration: none; border-radius: 8px;">Calendar</a>
    <a href="https://translate.google.com/?authuser=0" style="background-color: darkorange; font-size: 1.25rem; margin-left: 15px; font-weight: bold; padding: 5px 10px; color: white; text-decoration: none; border-radius: 8px;">Translate</a>
    <a href="https://contacts.google.com/?authuser=0" style="background-color: darkorange; font-size: 1.25rem; margin-left: 15px; font-weight: bold; padding: 5px 10px; color: white; text-decoration: none; border-radius: 8px;">Contacts</a>
    <a href="https://maps.google.com/?authuser=0" style="background-color: darkorange; font-size: 1.25rem; margin-left: 15px; font-weight: bold; padding: 5px 10px; color: white; text-decoration: none; border-radius: 8px;">Maps</a>
    <a href="https://play.google.com/?authuser=0" style="background-color: darkorange; font-size: 1.25rem; margin-left: 15px; font-weight: bold; padding: 5px 10px; color: white; text-decoration: none; border-radius: 8px;">Play</a>
    <a href="https://news.google.com?authuser=0" style="background-color: darkorange; font-size: 1.25rem; margin-left: 15px; font-weight: bold; padding: 5px 10px; color: white; text-decoration: none; border-radius: 8px;">News</a>
    <a href="https://meet.google.com?hs=197&amp;authuser=0" style="background-color: darkorange; font-size: 1.25rem; margin-left: 15px; font-weight: bold; padding: 5px 10px; color: white; text-decoration: none; border-radius: 8px;">Meet</a>
    <a href="https://drive.google.com/?authuser=0" style="background-color: darkorange; font-size: 1.25rem; margin-left: 15px; font-weight: bold; padding: 5px 10px; color: white; text-decoration: none; border-radius: 8px;">Drive</a>
    <a href="https://photos.google.com/?authuser=0" style="background-color: darkorange; font-size: 1.25rem; margin-left: 15px; font-weight: bold; padding: 5px 10px; color: white; text-decoration: none; border-radius: 8px;">Photos</a>
    <a href="https://www.google.com/shopping?source=og&amp;authuser=0" style="background-color: darkorange; font-size: 1.25rem; margin-left: 15px; font-weight: bold; padding: 5px 10px; color: white; text-decoration: none; border-radius: 8px;">Shopping</a>
`;
        document.body.appendChild(btnContainer)
    }
})();
```
