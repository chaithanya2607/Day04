# day04
# How to compare two JSON have the same properties without order?
var obj1 = { name: "Person 1", age:5 };
var obj2 = { age:5, name: "Person 1" };
ANSWER---


# Use the rest countries API url -> https://restcountries.eu/rest/v2/all and display all the country flags in console.
var request=new XMLHttpRequest();
request.open("GET","https://restcountries.com/v2/all");
request.send();
request.onload=function(){
  var result=JSON.parse(request.response);
  console.log(result);
  for(var i=0;i<result.length;i++){
    console.log(result[i].name+" "+result[i].flag);
  }
}

# Use the same rest countries and print all countries name, region, sub region and population.
var request=new XMLHttpRequest();
request.open("GET","https://restcountries.com/v2/all");
request.send();
request.onload=function(){
  var result=JSON.parse(request.response);
  console.log(result);
  for(var i=0;i<result.length;i++){
    console.log(result[i].name+" - "+result[i].region+" - "+result[i].subregion+" - "+result[i].population);
  }
}
