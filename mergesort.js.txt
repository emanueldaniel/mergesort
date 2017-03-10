function mergeSort(a) {
	if (a.length<2){
  	return a;
  } else {
  	var mijloc = a.length/2;
    var stanga = a.slice(0,mijloc);
    var dreapta = a.slice(mijloc, a.length)
  }
  return merge(mergeSort(stanga), mergeSort(dreapta));
}

function merge (s,d){
	var result = [];
  while(s.length && d.length) {
  	if(s[0] <= d[0]){
    result.push(s.shift());
    } else {
     result.push(d.shift());
    }
  } 
   while (s.length){
  		result.push(s.shift());
  } 
  while (d.length){
  		result.push(d.shift());
  }
  return result;
}

var a = [10, 9, 2, 6, 7];
console.log(mergeSort(a));