# Algo-DNAPairing
This is an algorithm to do the DNA Pairing in Javascript 

The DNA strand is missing the pairing element. Take each character, get its pair, and return the results as a 2d array.

Base pairs are a pair of AT and CG. Match the missing element to the provided character.

Return the provided character as the first element in each array.

#For example, for the input GCG, return [["G", "C"], ["C","G"],["G", "C"]]

The character and its pair are paired up in an array, and all the arrays are grouped into one encapsulating array.
```javascript
function pairElement(str) {
  let  newArray=str.split("");
  for (var i=0; i<newArray.length;i++){
     switch (newArray[i]){
      case 'C':
      newArray[i]=['C','G'];
      break;
      case 'G':
      newArray[i]=['G','C'];
      break;
      case 'T':
      newArray[i]=['T','A'];
      break;
       case 'A':
      newArray[i]=['A','T'];
      break;
  }
  }
  
  return newArray;
}

console.log(pairElement("CTCTA"));
```
