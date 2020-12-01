# TSI FizzBuzz Challange
Build a program that takes a number (n) and if the number is evenly divisible by 3, it should return "Fizz", 5 it should return "Buzz", both 3 and 5 return "FizzBuzz".

...

let get_fizBiz = (n) =>{
	
	// Declare a storage variable for text output
	let myOutput="";
	
	// Loop based on (n) 
	for(let i = 1; i<n+1; i++){
		
		// If (i) is divisible by 15 with no remainder print "FizzBuzz" 
		if(i % (3*5) === 0){ 
			myOutput += "FizzBuzz";
		
		// If (i) is divisible by 5 (no remainder) print "Buzz"
		}else if(i % 5 === 0){
			myOutput += "Buzz";
			
		// If (i) is divisible by 3 (no remainder) print "Fizz"
		}else if(i % 3 === 0){
			myOutput += "Fizz";
			
		// If (i) does match any of the previous conditionals add (i) as a string
		}else{
			myOutput += i.toString();
		}
		
		// Add linebreak
		myOutput += '<br/>'; 
	}
	
	// When loop is completed return the compiled output
	return myOutput;
}

// Declare variable with the returned output from get_fizBiz function
let myFizBiz = get_fizBiz(100);
	
// Grab instance of element by id that will recieve compiled output
let solOutput = document.getElementById("solution");
	
// Place the output storage vaiable as html wraping the variable in a paragraph element
solOutput.innerHTML='<p>'+myFizBiz+'</p>';

...
