# Callbacks
- Callbacks executam algo após uma tarefa síncrona ter sido executada
- É uma função passada como argumento para outra função

```js
function doSomething(callback){
  setTimeout(function(){
    callback('First data');
  }, 1000);
}

function doAll(){
  try{
    doSomething(function(data){
      var processedData = data.split('');

      try{
        doOtherThing(function(data2){
          var processedData2 = data2.split('');
          
          try{
            setTimeout(function(){
              console.log(processedData, processedData2);
            }, 1000);
          }catch(err){
            //error
          }
        })
      }catch(err){
        //error
      }
      
    })
  } catch(err){
    //Error
  }
  
}

doAll();

```