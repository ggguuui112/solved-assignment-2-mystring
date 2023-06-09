Download Link: https://assignmentchef.com/product/solved-assignment-2-mystring
<br>
Objective

<ul>

 <li>In this homework assignment, you must define a number of functions that can be used to analyze and manipulate C-strings.</li>

</ul>

Project Description

Before C++ and classes, strings were stored in simple arrays of characters. The term C-string refers to the classic implementation of strings in the C programming language. A C-string is a sequence of characters terminated by the null character, ‘ ’. Since C is part of C++, C-string implementations are valid in C++ as well as C.

Recall that an array of characters is the underlying data structure for storing C-strings. For example, this definition creates such an array.

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/766-1.png?w=980&amp;ssl=1" class="aligncenter lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" class="aligncenter" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/766-1.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>

myString will be capable of holding a C-string with up to 99 characters before the terminating null character. Of course, myString can hold a shorter C-string, too. For example, these assignments give myString the value “xyz”.

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/231.png?w=980&amp;ssl=1" class="aligncenter lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" class="aligncenter" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/231.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>It is legal to initialize a string variable, like this.

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/121.png?w=980&amp;ssl=1" class="aligncenter lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" class="aligncenter" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/121.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>Now, the string example[100] contains the following:————————————————————–| F | i | r | s | t |   | v | a | l | u | e |   | * | * |…————————————————————–However, it is not legal to assign string variables, because you cannot assign to an entire array.

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/687.png?w=980&amp;ssl=1" class="aligncenter lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" class="aligncenter" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/687.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>Furthermore, you cannot do comparisons like this.

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/874.png?w=980&amp;ssl=1" class="aligncenter lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" class="aligncenter" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/874.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>The comparison myString == “xyz” is actually legal (it will compile the addresses, not the strings!), but it will always evaluate to false. To handle these kinds of difficulties, programmers can rely on the C-string library (also referred to as ). This library, which is part of every proper C++ installation, is an extensive collection of functions for handling C-strings. Following are the 4 basic string library functions that we’ll discuss:

<strong>(1) strlen(str)</strong>Returns the number of characters in the string, not including the null character.

<strong>(2) strcmp(str1, str2)</strong>This function takes two strings and compares them. If the strings are equal, it returns 0. If the first is greater than the 2nd, then it returns some value greater than 0. If the first is less than the 2nd, then it returns some value less than 0.

You might use strcmp() as in:

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/802.png?w=980&amp;ssl=1" class="aligncenter lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" class="aligncenter" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/802.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>Or

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/347.png?w=980&amp;ssl=1" class="aligncenter lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" class="aligncenter" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/347.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>The ordering for strings is lexical order based on the ASCII value of characters. Remember that the ASCII value of ‘A’ and ‘a’ (i.e., upper/lowercase) are not the same.

An easy way to remember how to use strcmp() to compare 2 strings (let’s say a and b) is to use the following mnemonics:Want… Use…a == b strcmp(a, b) == 0a &lt; b strcmp(a, b) &lt; 0a &gt;= b strcmp(a, b) &gt;= 0… …

<strong>(3) strcpy(dest, source)</strong>Copies the contents of source into dest, as in:

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/266.png?w=980&amp;ssl=1" class="aligncenter lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" class="aligncenter" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/266.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/992.png?w=980&amp;ssl=1" class="aligncenter lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" class="aligncenter" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/992.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>Now, the string str1 contains the following:——————————————-| s | e | c | o | n | d |   | u | e |   |——————————————-and the word “initvalue” has been overwritten. Note that it is the first null character ( ) that determines the end of the string. When using strcpy(), make sure the destination is big enough to hold the new string.

Note: An easy way to remember that the destination comes first is because the order is the same as for assignment, e.g:dest = sourceAlso, strcpy() returns the destination string, but that return value is often ignored.

<strong>(4) strcat(dest, source)</strong>Copies the contents of source onto the end of dest, as in:

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/302.png?w=980&amp;ssl=1" class="aligncenter lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" class="aligncenter" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/302.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/520.png?w=980&amp;ssl=1" class="aligncenter lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" class="aligncenter" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/520.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>Now, the string str2 contains the following:——————————————| f | i | r | s | t |   | o | n | e |   |——————————————When using strcat(), make sure the destination is big enough to hold the extra characters.

<strong>Note: Function strcat() also returns the destination string, but that return value is often ignored.</strong>

Assignment Directions

Your task in this assignment is to complete your own versions of these four most commonly used standard string functions.

<table>

 <tbody>

  <tr>

   <td><strong>Your version:</strong>int mystrlen( const char *s)int mystrcmp( const char *s1, const char *s2)char *mystrcpy( char *s1, const char *s2)char *mystrcat( char *s1, const char *s2)</td>

   <td><strong>C standard string library functions:</strong>int strlen( const char *s)int strcmp( const char *s1, const char *s2)char *strcpy( char *s1, const char *s2)char *strcat( char *s1, const char *s2)</td>

  </tr>

 </tbody>

</table>

Each of your functions should have the same behavior as the corresponding above C standard string function. For example, your mystrlen function should have the same behavior as the C standard strlen function.

Your functions should not call any of the standard string functions. In the context of this assignment, you should pretend that the standard string functions do not exist.

You should pay special attention to boundary cases. In particular, make sure that your functions work when given empty strings as arguments. For example, make sure that the function call mystrlen(“”) returns 0.

First create a header file named mystring.h containing the interface to your functions. The interface should consist of a set of function declarations. Then create a file named mystring.cpp containing the implementation of your functions, that is, a set of function definitions. It should “#include” the interface file to insure that each function definition is consistent with its declaration.

You may use array notation to define your functions. For example, this is an acceptable version of the mystrlen function:

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/269-1.png?w=980&amp;ssl=1" class="aligncenter lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" class="aligncenter" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/269-1.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>However we encourage you to use pointer notation instead of array notation to define your functions; pointer notation is used heavily throughout the course, and it would be wise to use this assignment to insure that you are comfortable with it. For example, we encourage you to define your mystrlen function similar to this:

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/334.png?w=980&amp;ssl=1" class="aligncenter lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" class="aligncenter" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/334.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>The comment should appear in both the .h file (for the sake of the users of the function) and the .cpp file (for the sake of the implementation of the function).

For example, here is an appropriate way to comment a mystrlen function:

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/928.png?w=980&amp;ssl=1" class="aligncenter lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" class="aligncenter" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2017/05/928.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>Note that the comment explicitly states what the function returns, and explicitly refers to the function’s parameter (pcString).

<strong>Download Test Driver</strong>: We provide a driver (file <a href="https://psu.instructure.com/courses/1876053/files/83065566/download?wrap=1">Assign2driver.cpp</a>, <strong>Note</strong>: please insert one line: <em>#include &lt;cstring&gt;</em> right between line: <em>#include &lt;iostream&gt;</em> and line: <em>using namespace std;</em>) that you can download and use for some testing of your code. If no any error outputs, your program passes all the tests. Otherwise, it will tell you the line numbers of errors in your source codes.


