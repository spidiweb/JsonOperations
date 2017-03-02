# JsonOperations
This project contains demo for all the basic operations on JSON using JavaScript


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
