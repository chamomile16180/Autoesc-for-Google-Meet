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
1. Start or enter a Google Meet video meeting, the configuration is not account dependent and can happen in every meet room  with any number of partecipants. 
2. Inspect the page, you can do using the shortcut( ctrl + shift + i ) or right-clicking > inspect
3. Go on the sources menu <br/>  <br/> ![alt text](https://i.imgur.com/h26Upb8.png)
4. Click on the double brackets( ">>") and then click on "Snippets" <br/>  <br/> ![alt text](https://i.imgur.com/GBTWXIZ.png)
5. On the snippet page you need to make a new snippet by pressing "+New snippet" and copy paste the code that you saw at the start of this page in the new snippet blank space, at the end of the process you should have something like this: <br/>  <br/> ![alt text](https://i.imgur.com/9OTsoLE.png)
6. Now you need to change the first and the second line of the script: in order to do so you should click on the small arrow that you see on the top left of the right panel and then on the number of partecipants (not the icon, the number), right click on the highlighted element in the elements tab > copy full xpath > paste it inside the quotes of the first line of the snippet (source Tab). Then do the same thing again but this time click on the "close call" button and paste the contents of copy full xpath into the quotes of the second line. Press ctrl+S to save the snippet. I Will make a short video to make you see how the selection and pasting process should look like ->[![how to set xpaths](https://i.imgur.com/i6Fz4PD.png)](https://youtu.be/UXMG7c-ChTY "How to set xpaths - Click to Watch!") 
### USE 
When you want to use the snippet just go on the snippet window by inspecting the page, click with the right mouse button on the file icon in the left part of the snippet panel and select run. The value people_treshold is the threshold of the exit: when there aren't at least (people_threshold) partecipants the script will automatically make you leave the room, you can obviously change that value according to your preferences. If you change that value remember to save the snippet with ctrl+s. The Extension may stop working if a new release of the website comes out: in that case it is necessary to re-config the script. 



