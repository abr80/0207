// ==UserScript==
// @name         YandexBot
// @namespace    http://tampermonkey.net/
// @version      0.1
// @description  try to take over the world!
// @author       Andrey
// @match        https://yandex.ru/*
// @icon         data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==
// @grant        none
// ==/UserScript==

let keywords = ["обеденные группы для кухни", "обеденные группы для кухни купить", "обеденные группы на кухню"];
let keyword = keywords[getRandom(0, keywords.length)];
let btnK = document.querySelectorAll (".mini-suggest__button")[0];
let links = document.links;

if(btnK !== undefined) {
  document.getElementsByName("text")[0].value = keyword;
  document.querySelectorAll(".mini-suggest__button")[0].click();
} else {
  for (let i = 0; i < links.length; i++) {
    if (links[i].href.indexOf("qupi-stol.ru") !== -1) {
      let link = links[i]
      console.log("Нашел строку " + links[i]);
      link.click();
      break;
    }
  }
}

function getRandom(min, max) {
return Math.floor(Math.random() * (max - min) + min);
}
