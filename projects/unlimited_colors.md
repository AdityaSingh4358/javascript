// generate a random color 
const randomColor=function(){
  const hex='0123456789ABCDEF';

  let color='#';
  for(let i=0;i<6;i++){
    color+=hex[Math.floor(Math.random()*16)]; // random color generate ho jayga 

  }
  return color;
};
console.log(randomColor())


// NOW WE HAVE TO START CHANGING COLOR 
let intervalId;
const startChangingColor=function(){
  
  if(!intervalId){ // matlab agar null nai hai to fir ye hoga 
    intervalId=setInterval(changeBgColor,1000)
  }
  function changeBgColor(){document.body.style.backgroundColor=randomColor();
  }  
  

}


const stopChangingColor=function(){
  // STOP BHI TO KARNA HAI AB 
  clearInterval(intervalId);

  intervalId=null;  // jo pehle liya tha usko hata diya ab // matlab clean up kar diya re 
  

}

document.querySelector('#start').addEventListener('click',startChangingColor);

document.querySelector('#stop').addEventListener('click',stopChangingColor);


