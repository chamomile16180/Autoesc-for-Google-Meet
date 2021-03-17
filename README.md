# Autoesc-for-Google-Meet
This light js script will allow Google Meet users to automatically exit from calls after the number of people connected drops under a certain threshold. 
## CODE
```javascript
el = 'YOURXPATH_HERE'
button ='YOURXPATH_HERE'
people_threshold = 10
function $x(path) {
  return document.evaluate(path, document, null, XPathResult.FIRST_ORDERED_NODE_TYPE, null).singleNodeValue;
}

function check(){
    try{
         num = parseInt($x(el).textContent)
         console.log(num)
         if(num<people_threshold){
            $x(button).click()
            }
        }
        catch(err){console.log(err);}
    }
setInterval(check,1000)
```
## HOW TO USE IT 
### Configuration  
In order to start using this short script you will need to configure it first. Follow the steps below (✧≖╭͜ʖ╮≖)


