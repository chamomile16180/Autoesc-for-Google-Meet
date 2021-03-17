# Autoesc-for-Google-Meet
This light js script will allow Google Meet users to automatically exit from calls after the number of people connected drops under a certain threshold. 

```javascript
el = '/html/body/div[1]/c-wiz/div[1]/div/div[9]/div[3]/div[1]/div[3]/div/div[2]/div[1]/span/span/div/div/span[2]'
button ='/html/body/div[1]/c-wiz/div[1]/div/div[9]/div[3]/div[9]/div[2]/div[2]/div'
function $x(path) {
  return document.evaluate(path, document, null, XPathResult.FIRST_ORDERED_NODE_TYPE, null).singleNodeValue;
}

function check(){
    try{
         num = parseInt($x(el).textContent)
         console.log(num)
         if(num<10){
            $x(button).click()
            }
        }
        catch(err){console.log(err);}
    }
setInterval(check,1000)
```
