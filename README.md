# closure-concept

var a = 1;

function abc(){
console.log("First..", a);
if(a){
         var a = 10
        console.log("Second..", a);
    }else{
        a = 20
        console.log("Third..", a);
    }
        a = 30
    console.log("Forth..", a);
}

console.log("Fifth..", a);

abc();

console.log("Sixth..", a);




/-----------------------------------------------------------/

function abc(a){
  var sum = a;
  function add(b){
     if(b){
        sum += b;
        console.log(sum, b)
        return add;
     } else {
return sum;
     }
  }
  return add;
}

var c = abc(3)(4)(5)();
console.log(c);
