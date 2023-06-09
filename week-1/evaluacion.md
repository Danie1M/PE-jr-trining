const urls = [
"https://goaxil.com/collections/ear-buds/products/gs-electronic.js",
"https://therollingstonesshop.com/products/americana-tongue-unisex-black-t-shirt.js",
"https://offhours.co/collections/shop-all/products/affogato-1.js",
"https://www.danskin.com/products/calming-slip-on-sneaker.js",
// "https://www.url.fail/expected-error.js",
];

async function fetchUrl() {
//let response;
let data;
let dataUrls = [];
for (let url of urls) {
let response = await fetch(url).catch();
if (!response.ok) {
throw new Error(`Error, ${url}!`);
} else {
data = await response.json();
dataUrls.push(data);
}
}
console.log(dataUrls);

let result = {};
for (let dataUrl of dataUrls) {
resulUrl = {
id: {},
title: "",
brand: "",
image: {},
price: "",
};
Object.values(resulUrl).forEach((element) => {
element.id = dataUrl.id;
element.title = dataUrl.title;
element.brand = dataUrl.vendor;
element.image = dataUrl.images;
element.price = dataUrl.price;
});
console.log(resulUrl);
}

return dataUrls;
}
fetchUrl();
