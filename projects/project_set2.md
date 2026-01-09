# Solution Code Project 2

``` javascipt
const form=document.querySelector('form')
form.addEventListener('submit',function(e){
    // submit type ka event hai ye 
    // event ko prevent karenge taaki server pe naa chala jaye 
    e.preventDefault();
    const height=parseInt(document.querySelector('#height').value)
    const weight=parseInt(document.querySelector('#weight').value)

    const results=document.querySelector('#results');

    // height and weight pe code phatt sakta hai to check laga lenge hum 

    if(height === '' || height<0 || isNaN(height)){
      results.innerHTML=`Please enter a valid height ${height}`;

    }
    

    else if(weight === '' || weight<0 || isNaN(weight)){
      results.innerHTML=`Please enter a valid weight ${weight}`;

    }
    else{
      const bmi=(weight/((height*height)/10000)).toFixed(2); // 2 integer tak lega value 

      results.innerHTML=`<span>${bmi}</span>`;
    }
    


});

```