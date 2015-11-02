#Bus

A simple javascript library to perform timer operations. It is useful to perform operations repeatedly or at a perticular time.

##Setup
Include the bus.js to your page
```
<script type="text/javascript" src="bus.js"></script>
```

##Initialization
After including the library, start the bus to run it.
```
<script>
Bus.start();
</script>
```

##Load Handlers
After starting the bus we need to load the handlers to get triggered at perticular time
```
Bus.every(Bus.time.sec,function(){
  console.log(Bus.time.to('sec'); //will get triggered at every second and show the seconds.
});
```

#Customize
You can customize the Bus frequencey ie times per second.
```
Bus.start(10); //Bus trigs 10 times a second
```

#Options
List of handler options are given below
```
Bus.every(time, function(){}); //will get triggered each time
Bus.at(time, function()); //will get triggered at the time
Bus.from(time, function()); //will get triggered from the time
Bus.till(time, function()); //well get triggered till the time
Bus.between(from_time, to_time, function(){}); //will get triggered in between the times
```

List of times
```
Bus.time.mil //milli second
Bus.time.sec //second
Bus.time.min //minute
```

List of time checkers
```
if(Bus.time.isSec()){} //true for every sec
if(Bus.time.isSec(10)){} //true for every 10th sec
if(Bus.time.isMin()){} //true for every min
if(Bus.time.isMin(10)){} //true for every 10th min
if(Bus.time.isSecOnce(10)){} //true for first 10th sec
if(Bus.time.isMinOnce(10)){} //true for first 10 min
```

Pause the bus
```
Bus.pause();
```
