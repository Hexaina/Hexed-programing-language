```
//these are comments
/*
they will be used to take you through the big ideas
i will migrate the original doc to here soon 
*/
//functions
  function name(parameters)[type /*optional*/ ]{
    code
  }

//base functions
	print("string")
		\\prints to the standerd output
	
  
//variables
	var name = value //dynamic
	int name = whole number //type safe
	float name = decimal //type safe
	double name = precise decimal //type safe
	string name = "string" //type safe, use only "" for strings
	bool name = Boolean //type safe
	bianary name = bianary number //used to store a bianary number
	hexadecimal name = hexadecimal number //used to store a hexadecimal number
	enum name = {posibleValue1, posibleValue2, ect}
	nameOfAnEnum name = value //use this to make a variable with a type dictated by an enum

//data types
	hash name = type: name, type: name 
		//only one key value pair. for a hash map, use a table
	
	struct name = {
		type name: value
	} 
		//defines values that are grouped together and accesesed through dot notation (structName.valueName)

	bianaryString name = string of bianary numbers
		//seperated by a space ex - 10011011 10001101
	hexadecimalString name = string of hexadecimal numbers
		//seperated by a space ex - 86B2 F20E
	table name = [type: value, type: value, ect]
		//useing "type:" is optinal. not using it is equivelent to useing "var:"
	RGB name = [red, gree, blue]
	CMYK name = [cyan, magenta, yellow, black]
	RYB name = [red, yellow, blue]
	HSL name = [hue, saturation, lightness]
	HSV name = [hue, saturation, value]
	hexCol name = #hex value //such as #FF0000

//senders and receivers
	//sender
		beacon name{
		    globalSignal("message") //or
		    localSignal("message")
	    }
	//receiver
	    receiver name("message"){
		    code //no return
	    }

//class
	class name = (inherit name /*if no inheritance input "void"*/ ){
	    
	}

//object
	name = (inherit name /*if no inheritance input "void"*/ ){
	    
	}

//proportys
	type name: value //just replace "=" with ":", use with classes and objects, and data types

//methods
	method name(parameters)[type /*optional*/ ]{
		
	} //just replace "function" with "method"

//front end
	//there are two kinds of elements, parent elements and base elements
	//parent element syntax is <item(parameters)>{child elements}
	//base element syntax is <item(parameters)>
	//all colors are one of the following - RGB, CMYK, RYB, HSL, HSV, or HEX. to add color into the paramaters, use the color type followed by the values. ex- RGB[255,255,255] ex- CMYK[255,255,255,255]. or use a variable of one of the color types

	//for desktop (or used in the canvas)
		<window(name, hight /*in pixels*/, width /*in pixels*/, fullscreen /*bool*/ )>{
			
	    }
	    <text(id, text, size /*in pixels*/, bold /*bool*/, italic /*bool*/, font)>
	    <square(id, x, y, hight, width, color)>
	    <box(id, x, y, hight, width, color)>{
			
	    }
	    <circle(id, x, y, hight, width, color)>
	    <shape(id, color, point1x, point1y, point2x, point2y, ect...)>
	    <geomitry(id, color, point1x, point1y, point2x, point2y, ect...)>{
			
	    }
	    <image(id, x, y, hight, width, imageFilePath)>
	    <output(id, x, y, hight, width, text size /*in pixels*/, bold /*bool*/, italic /*bool*/, text font)> //displays the standerd output

	//web spesific
		//web apps must compile to html, so the elements will be similar to that of html elements
		
		<canvas(name, hight /*in rows*/, width /*in coloms*/, fullpage /*bool*/ )>{
			
		}
		<text(id, text, size /*in pixels*/, bold /*bool*/, italic /*bool*/, font)>
		<link("url")>{
			
		}
		<style(color, size /*in pixels*/, bold /*bool*/, italic /*bool*/, font)>{
			
		}
		<square(id, x, y, hight, width, color)>
	    <box(id, x, y, hight, width, color)>{
			
	    } //basicly a div

	//other
		//mobchain
		    //id pairs is a pair of ints that contains the id of the last mob in the chain and the first number +1
		    mobchain name = (starting id){
			    
			}
		        //things to put inside
			        type name: value 
				        //mobchain proportys always add a mob to the chain when exacuted with data containing an id pair and the porporty name. they can only be changed by a mobchain method from the same chain but they can be read from anywere
		        
			        method name(parameters){
				        
			        }
				        //mobchain methods always add a mob to the chain when executed with data containing an id pair, the method name, and the changes caused.
				//functions
				    mobchainName.addMob(type, data) 
					    //adds mob to the chain containing an id pair and a piece of data witch can only be read

				    mobchainName.addcode(code) 
					    //adds a proporty or method to the mobchain witch can be used afterwards

					mobchainName.read(id, request /*change, data, value*/)
						//returns a value from a block

				    mobchainName.disableMethod(methodName) 
					    //removes the method from the mobchain obgect and adds a block with a message reading "removed methodName" and in id pair
```
