1) values added: 20
2) final result: 20
3) values added: 20
4) Line 13 results in an error since the scope of result is in the if block and since it has ended you cannot reference result.
5) The code has an error because at line 4 result is trying to be assigned a value even though it already has a value. Once a const variable is assigned a value it cannot be reassigned. 
6) Nothing is printed at line 13 since an error was thrown at line 4 when a constant was tried to be reassinged a value.
