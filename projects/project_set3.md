# Project 3 solution 

``` javascipt

document.getElementById('clock')

// merko chaiye ki har second  baad time update hota rahe 
// iske liye use karte hain setInterval function 

setInterval(function (){
  let date=new Date();
  //console.log(date.toLocaleTimeString());
  // isse har step pe value aati rahegi console mein 
  clock.innerHTML=date.toLocaleTimeString();

  // humein to node mein value update karni hai 

},1000);
```
