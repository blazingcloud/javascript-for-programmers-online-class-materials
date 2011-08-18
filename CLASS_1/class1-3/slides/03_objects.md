!SLIDE 
# JavaScript For Programmers #
# .x Introduction - Part 3 x. #
# .(  Object  ). #


!SLIDE bullets incremental small
# Objects #

* Object is the superclass of all other objects 
* Object == Hash == Associative Array 

!SLIDE 
## Creating an object ##
<br><br><br><br>

    @@@ javaScript
    var myObject = new Object();
    
    var myObject = {};

!SLIDE 
## Setting properties on an object ##
<br><br><br><br>

    @@@ javaScript
    myObject.a == "a";
    
    myObject['a'] = "a";

!SLIDE
## Accessing an object's properties ##
<br><br><br><br>

    @@@ javaScript
    myObject.a;
    
    myObject['a'];
    
!SLIDE small
## Setting functions on objects ##
<br><br><br><br>

    @@@ javaScript
    myObject.myFunction = function() {
      console.log('function prints myObject.a: ',
        myObject.a);
    };

!SLIDE
## Calling the function ##
<br><br><br><br>

    @@@ javaScript
      myObject.myFunction()
      myObject.myFunction(1,2,3)
      myObject.myFunction.apply(myObject,[1,2,3])
      myObject.myFunction.call(myObject,1,2,3)

      
!SLIDE
## Displaying all of the attributes and functions on objects ##
<br><br><br><br>

    @@@ javaScript
      for (var prop in myObject) {
        console.log(prop, ": ", myObject[prop]);
      }

!SLIDE
## New and Prototype chain
    @@@ javaScript
      var A = function(){ 
            console.log('A Called')
            return this 
      }

      console.log(
          'A.constructor == Function :'
          , A.constructor == Function)
      console.log(
        'A.prototype.constructor == A :'
        ,A.prototype.constructor == A )

!SLIDE
## New and Prototype Continued
    @@@ javaScript
  
      A.what_is_my_name = function() { 
        console.log("what is my name?",this)
        return this
      }
      var B = function() { 
        console.log('B Called')
        return this
      }
      B.prototype = A
      var ab = new B
      ab.what_is_my_name()
      console.log(
      'ab.prototype == A.prototype'
      , ab.prototype == A.prototype)


