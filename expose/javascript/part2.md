1) At line 12 we get an output of '3'. This is because of the fact that i served as a variable for the for loop. Also it was defined as a var which is why it's scope is beyond that of the for loop. Since prices is [100, 200, 300] which has a length of 3, the for loop ends at 3 because 3 is not less than prices.length.
2) At line 13 we get an output of 150 because at the last iteration of the for loop we are looking at the last value in prices which is 300. The discountedPrice variable is then set to prices[2] or 300 * (1-0.5) = 300 * 0.5 = 150. Since this variable is a var it is kept beyond the scope of the for loop and the value is outputted.
3) At line 14 we get an output of 150 because at the last iteration of the loop finalPrice is set to Math.round(discountedPrice*100) / 100. Math.round returns the value rounded to the nearest integer however as we discussed in number 2 discountedPrice was 150 so multiplying by 100 gives 15000. 15000 rounded to the nearest integer is 15000. Then divided by 100 returns 150 which is what we got. 
4) The function returns a list of all the finalPrices for each of the prices that were pushed to the function. In this case the function would return [50, 100, 150] which were the finalPrice for the prices [100,200,300] that were passed. 
5) At line 12 the function returns a "ReferenceError: i is not defined". This is because of the fact that i in the for loop was a let variable. Therefore the scope of that variable was limited to the scope of the for loop. Since the for loop ended the variable has also which is why we get a ReferenceError.
6) At line 13 we get an error: "ReferenceError: discountedPrice is not defined". Again this is because discountedPrice was initiated and created inside the for loop using the let variable. As a result of using let discountedPrice only has the scope of the for loop. Since the for loop has ended accessing discountedPrice throws a reference error.
7) At line 14 we get 150 the value of finalPrice for the last list item of our parameter prices. This is because although finalPrice was in the for loop and was a let variable, it was initalized in the function's body. Therefore finalPrice can be referenced anywhere throughout the function which is why calling console.log(finalPrice) returns 150 the value of the variable.
8) The function returns [50, 100, 150] since discounted was initalized in the function scope and all the values added to discounted were finalPrice values. As we discussed in 7, since finalPrice's scope is the entire function, any reference to finalPrice in the function after it's initialization will not return an error. Therefore discounted returns the three finalPrice values [50, 100, 150].
9) At line 11 the function returns a ReferenceError saying that i is not defined. This is because of the fact that i was defined and initialized in the for loop using let. Therefore the scope is limited to the for loop. Line 11 is outside the for loop therefore we are not able to reference i.
10) At lie 12 the fcuntion returns 3 because the length was initalized and defined at the start as prices.length. Since it was a const variable that is the only place it will gain it's value. Since price.length is |[100, 200, 300]| = 3 we get 3.
11) This function returns [50, 100, 150] because although discount is a const variable, that does not mean the value it holds is immutable. The variable identifier discounted cannot be changed but the internal of discounted can change. That is why discounted.push(discountedPrice) adds the 50, 100, and 150 into it.
12a) student.name
12b) student["Grad Year"]
12c) student.greeting()
12d) student.["Favorite Teacher"].name
12e) student.courseLoad[0]
13a) The output is "32" because of the fact that javascript sees a string and a number and doesn't know whether string can be converted to a num in a valid way. Since + is also used for concatenation the number is converted to a string.
13b) This output is 1 because we know that the substraction symbol doesn't mean anything when it comes to strings. Therefore the only way to perform this expression is to try to convert the string to a number. 
13c) This returns 3 since null is converted to a 0 when it appears in an expression.
13d) Again this is the situation where a string and a + is observed so concatenation occurs.
13e) This returns 4 because we convert the boolean to a number because javascript sees a expression. Since true is converted to a 1, 3 + 1 = 4.
13f) This returns 0 because false is converted to a 0 and null is also converted to a zero. Again this conversion happens because they are involved with an expression.
13g) This returns '3undefined' because there is a string and a + so automatic concatenation occurs.
13h) This returns NaN because now there is a - sign which doesn't make sense when it comes to strings. Therefore both operands are converted to numbers. '3' gets converted to 3 and undefined gets converted to NaN.
14a) This returns true since this is an expression the string '2' is converted to 2 which is greater than 1. Because this is a conditional statement true is returned.
14b) This returns false, since this is a string, string comparison javascript does not convert both of these into numbers. Instead the algorithm to compare strings is run. The first characters are compared and since '2' is not less than '1' false is returned.
14c) This returns true since when comparing values of different types Javascript converts the values to numbers.
14d) This returns false because the strict equality is used where no conversion occurs. Since the string 2 is not the same as the number 2 this will return false.
14e) This returns false. This is a comparison so true is converted to 1 which isn't equal to 2.
14f) This returns true because the strict equality is used. Boolean(2) returns true because Boolean() only returns false for false for intuitively empty things like 0, "", null, undefined, or NaN.
15) The difference between == and === is that == does an equality comparision after converting both sides to numbers. === on the other hand does not perform any conversions unless explicitly stated. 
16) In part2-question16.js
17) The result is going to be [2,4,6]. So we start with modifyArray recieving a list [1,2,3] and the callback function doSomething which gets a number, and returns that number multiplied by 2. In modifyArray the array is traversed and it's elements are passed to the callback. This multiplies each element of the array by 2 and then at the end this array is returned.
18) Included in part2-question18.js
19) The output of this code is 1 4 3 2. 