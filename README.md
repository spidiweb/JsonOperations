# JsonOperations
This project contains demo for all the basic operations on JSON using JavaScript
#Basic Operations
var array = [];//Create a blank Array

arr.push(10);//Add an element on the last index + 1 of array.
//the above line could also be written as below
arr[arr.length] = 10;//arr is filled till arr.length - 1 index, adding new element to next index.

arr.push(20);
arr.push(30);
arr.push(40);
arr.push(50);


console.log(arr[1]);//Access element by index no.

arr.pop();//Takes out the max index element from arr and return it. This element will be #deleted# from arr.



#Add Element at begining

#ReplaceAll in JavaScript:
1. 
String.prototype.replaceAll = function (toReplace, replaceWith)
{
    return this.split(toReplace).join(replaceWith);
}
2. 
str = str.replace(/John/gi,'He');
# Searching in Array of Objects:
var Employees = 
  [
    {ID:1, Name:'Spidi',DOB:'26-May-1992',Salary:2010000},
    {ID:2, Name:'John',DOB:'6-June-1987',Salary:2510000},
    {ID:3, Name:'Petr',DOB:'6-July-1992',Salary:210000},
    {ID:4, Name:'Joe',DOB:'2-August-1992',Salary:2310000},
    {ID:5, Name:'Frank',DOB:'2-Sept-1992',Salary:3010000},
    {ID:6, Name:'Aman',DOB:'16-Javuary-1992',Salary:4010000}
  ];
  
//Using filter function
var result = Employees.filter(function(elem){
   //return true or false from here. true means this element is the part of resultset for your search.
   //Example: Search employee with salary more than 230000
   return elem.Salary > 230000;
})

# Sorting a JSON Array of Objects.

var Employees = 
  [
    {ID:1, Name:'Spidi',DOB:'26-May-1992',Salary:2010000},
    {ID:2, Name:'John',DOB:'6-June-1987',Salary:2510000},
    {ID:3, Name:'Petr',DOB:'6-July-1992',Salary:210000},
    {ID:4, Name:'Joe',DOB:'2-August-1992',Salary:2310000},
    {ID:5, Name:'Frank',DOB:'2-Sept-1992',Salary:3010000},
    {ID:6, Name:'Aman',DOB:'16-Javuary-1992',Salary:4010000}
  ];

//Sort by Salary
var sortedEmp = Employees .sort(function(a, b) {
  return a.Salary - b.Salary;
});

//Sort by Name
var sortedEmp = Employees .sort(function(a, b) {
  if(a.Name < b.Name) return -1;
  if(a.Name > b.Name) return 1;
  return 0;
});

//Sort by Name
var sortedEmp = Employees .sort(function(a, b) {
  return new Date(a.DOB) - new Date(b.DOB);
});
