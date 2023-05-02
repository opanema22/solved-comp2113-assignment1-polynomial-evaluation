Download Link: https://assignmentchef.com/product/solved-comp2113-assignment1-polynomial-evaluation
<br>
<strong>Problem 1: Polynomial Evaluation</strong>

Write a C++ program that evaluate a degree-<em>n</em> polynomial

<em>a</em><em>n</em><em>x</em><em>n </em>+ <em>a</em><em>n</em>−1<em>x</em><em>n</em>−1 + ⋯ + <em>a</em>1<em>x </em>+ <em>a</em>0

<strong>with </strong><em>n</em><strong> multiplications and </strong><em>n</em><strong> additions only</strong>. Note that this is the optimal, meaning that you cannot do this evaluation with fewer arithmetic operations.

Implement the <a href="https://en.wikipedia.org/wiki/Horner%27s_method">Horner’s method</a> to achieve this optimal computation.

<strong>Input:</strong>

A single line containing <em>n </em>+ 3 numbers, separated by spaces. The first number is the value of <em>x</em>, then the degree <em>n</em> of the polynomial to evaluate, followed by the <em>n </em>+ 1 coefficients <em>a<sub>n</sub></em>, <em>a<sub>n</sub></em><sub>−1</sub>, …,

<em>a</em><sub>0</sub>.

The value <em>x</em> is a floating-point number and the numbers <em>n</em>, <em>a<sub>n</sub></em>, <em>a<sub>n</sub></em><sub>−1</sub>, …, <em>a</em><sub>0</sub> are integers, and <em>n </em>≥ 0.

<strong>Output:</strong>

A single line containing the result of the polynomial evaluation, printed as a fixed floating number with 6 decimal places.

You may use  setprecision(n)  defined in the header  &lt;iomanip&gt;  to set the precision parameter of the output stream.

<strong>Requirement:</strong>

Use the <sub> float </sub> data type for all floating point computations in this program.

You can ONLY use the simple data types  char ,  bool ,  int ,  float . In other words, you are not allowed the use other data types or data structures such as arrays, vectors, etc.

<strong>Sample Test Cases</strong>

User inputs are shown in blue.

1_1

-1.5 0 4

4.000000

1_2

2.43 1 4 -2

7.720000

1_3

3.289 3 -1 2 4 -6

-6.787785

1_4

-0.0001 10 11 -10 9 -8 7 -6 5 -4 3 -2 1

1.000200

<strong>Problem 2: A Divisor Matrix</strong>

Write a C++ program that implement the divisor matrix as follows:

<strong>Input:</strong>

Your program should prompt the user for two positive integers <sub> a </sub>,<sub> b </sub>. (See sample test cases for the required prompt messages.) You may assume that the user will always input positive integers such that the following holds,  0 &lt;= a &lt; b &lt; 1000 .

The user will then be prompted for two divisors. You may assume that divisors entered by the user are valid, for which the following holds,  1 &lt;= divisor &lt; 1000 .

<strong>Output:</strong>

The program will then output a matrix with the following elements.

The first row will start with an <sub> M </sub> followed by the two divisors in input order.

The first column, beneath the <sub> M </sub>, will contain the integers between <sub> a </sub> and <sub> b </sub> (including <sub> a </sub> and excluding <sub> b </sub>), in increasing order.

For the remaining two elements of each row, there will be a <sub> 1 </sub> if the integer in that row is

divisible by the divisor at the head of that column, otherwise <sub> 0 </sub>.

Matrix elements should be separated by a space. Note that there is no trailing space after the last element of a row.

<strong>Requirement:</strong>

You can ONLY use the simple data types  char ,  bool ,  int ,  double . In other words, you are not allowed the use other data types or data structures such as strings, arrays, vectors, etc.

<strong>Sample Test Cases</strong>

User inputs are shown in blue.

2_1:

a: 1

b: 10

Divisor 1: 2

Divisor 2: 3

M 2 3

<ul>

 <li>0 0</li>

 <li>1 0</li>

 <li>0 1</li>

 <li>1 0</li>

 <li>0 0</li>

 <li>1 1</li>

 <li>0 0</li>

 <li>1 0</li>

 <li>0 1</li>

</ul>

2_2:

a: 134 b: 141 Divisor 1: 4

Divisor 2: 5

M 4 5

<ul>

 <li>0 0</li>

 <li>0 1</li>

 <li>1 0</li>

 <li>0 0</li>

 <li>0 0</li>

 <li>0 0</li>

 <li>1 1</li>

</ul>

2_3:

a: 2 b: 21 Divisor 1: 2

Divisor 2: 5

M 2 5

<ul>

 <li>1 0</li>

 <li>0 0</li>

 <li>1 0</li>

 <li>0 1</li>

 <li>1 0</li>

 <li>0 0</li>

 <li>1 0</li>

 <li>0 0</li>

 <li>1 1</li>

 <li>0 0</li>

 <li>1 0</li>

 <li>0 0</li>

 <li>1 0</li>

 <li>0 1</li>

 <li>1 0</li>

 <li>0 0</li>

 <li>1 0</li>

 <li>0 0</li>

 <li>1 1</li>

</ul>

<strong>Problem 3: Sine Function Approximation</strong>

Write a C++ program which calculates an estimation of sin<em>x</em> using Taylor series approximation with the formula:

sin<em>x </em>= ∑<em>n </em>(−1)<em>i         </em>2<em>i</em>+1, <em>x </em>(2<em>i </em>+ 1)! <em>i</em>=0

where <em>i</em>! = 1 × 2 × 3 × ⋯ × <em>i</em> denote the factorial of <em>i</em>, and 0<sup>0</sup> is defined as 1. The integer <em>n </em>governs the order of approximation and you may assume that <em>n</em> ranges from 0 to 50 inclusively in this

question.

<strong>Input:</strong>

a line with two numbers: a real number <em>x</em> (−3 ≤ <em>x </em>≤ 3) followed by an integer <em>n</em> (0 ≤ <em>n </em>≤ 50).

<strong>Output:</strong>

Your program should output the estimations of sin<em>x</em> as <em>n</em> increases. Specifically, your program should

On the first line, print the result of sin<em>x</em> as returned by the predefined function <sub> sin() </sub> in

<sub>&lt;cmath&gt; </sub> <strong>as a fixed floating number with 15 decimal places</strong>.

Output the values of <em>n</em> and sin<em>x</em> on the subsequent lines as <em>n</em> increases. The values <em>n</em> and sin<em>x</em> on each line are separated by a space. <strong>The value </strong>sin<em>x</em><strong> is printed as a fixed floating number with 15 decimal places.</strong>

You may use  setprecision(n)  defined in the header  &lt;iomanip&gt;  to set the precision parameter of the output stream.

<strong>Requirement:</strong>

Use only the  double  and  int  data types in your calculations.

You can ONLY use the simple data types  char ,  bool ,  int ,  double . In other words, you are not allowed the use other data types or data structures such as strings, arrays, vectors, etc.

<em>Note</em>:

You cannot evaluate the factorial operator in a brute-force manner using multiplications only, because <strong>overflow</strong> can easily occur which means that the resulting value is too large to be stored in an <sub> int </sub>. (Consider 30! ~= 2.6525e+32 which cannot be held by even the

unsigned long long  type).

Divisions involving some large numbers can easily run into numerical inaccuracy issues (you will learn more about this in the machine organization course).

Hence, <strong>you should do divisions before multiplications (whenever possible) to keep the intermediate values at each iteration of the calculation small</strong>.

Since different orders of arithmetic operations may entail slight difference in the final evaluation, <strong>your results will be check against the test outputs for correctness up to the first 5 decimal points only</strong>.

<strong>Sample Test Cases</strong>

User inputs are shown in blue.

3-1

<ul>

 <li>0</li>

</ul>

sin(x) by cmath: 0.000000000000000

Taylor series approximation: 0 0.000000000000000

3_2

<ul>

 <li>10</li>

</ul>

sin(x) by cmath: 0.841470984807897

Taylor series approximation:

<ul>

 <li>000000000000000</li>

 <li>833333333333333</li>

 <li>841666666666667</li>

 <li>841468253968254</li>

 <li>841471009700176</li>

 <li>841470984648068</li>

 <li>841470984808658</li>

 <li>841470984807894</li>

 <li>841470984807897</li>

 <li>841470984807897</li>

 <li>841470984807897</li>

</ul>

3_3

-2.9 20

sin(x) by cmath: -0.239249329213982

Taylor series approximation:

0 -2.900000000000000 1 1.164833333333333

<ul>

 <li>-0.544429083333334</li>

 <li>-0.202169632757937</li>

 <li>-0.242147438026535</li>

 <li>-0.239090953096454</li>

 <li>-0.239255728982749</li>

 <li>-0.239249130100826</li>

 <li>-0.239249334132433</li>

 <li>-0.239249329115164</li>

 <li>-0.239249329215629</li>

 <li>-0.239249329213960</li>

 <li>-0.239249329213983</li>

 <li>-0.239249329213983</li>

 <li>-0.239249329213983</li>

 <li>-0.239249329213983</li>

 <li>-0.239249329213983</li>

 <li>-0.239249329213983</li>

 <li>-0.239249329213983</li>

 <li>-0.239249329213983</li>

 <li>-0.239249329213983</li>

</ul>

<strong>Problem 4: Caesar Shifting</strong>

Write a C++ program which encrypts and decrypts some input characters using the Casesar Shifting algorithm detailed below.

<strong>Input:</strong>

a line of input <em>s</em> <em>k</em> <em>c</em><sub>1</sub> <em>c</em><sub>2</sub> <em>c</em><sub>3</sub> …, where <em>s</em> is either the character <sub> e </sub> for encryption, or the character <sub> d </sub> for decryption <em>k</em> is an integer for the number of shifts used in the Caesar shift algorithm

<em>c</em><sub>1</sub> <em>c</em><sub>2</sub> <em>c</em><sub>3</sub> … is a sequence of space separated characters, ended by <sub> ! </sub>, to be encrypted or decrypted

<strong>Output:</strong>

the encrypted/decrypted message ended by <sub> ! </sub>. No space between two consecutive characters.

<strong>Algorithm:</strong>

To encrypt (decrypt) a letter <em>c</em> (within the alphabet A-Z or a-z) with a shift of <em>k</em> positions:

<ol>

 <li>Let <em>x</em> be <em>c</em>‘s position in the alphabet (0 based), e.g., position of <sub>B </sub> is 1 and position of <sub> g </sub> is 6.</li>

 <li>For encryption, calculate <em>y </em>= <em>x </em>+ <em>k</em> modulo 26; for decryption, calculate <em>y </em>= <em>x </em>− <em>k</em> modulo 26.</li>

 <li>Let <em>w</em> be the letter corresponding to position <em>y</em> in the alphabet. If <em>c</em> is in uppercase, the encrypted (decrypted) letter is <em>w</em> in lowercase; otherwise, the encrypted (decrypted) letter is <em>w</em> in uppercase.</li>

</ol>

<strong>A character which is not within the alphabet A-Z or a-z will remain unchanged under encryption or decryption.</strong>

<em>Example</em>. Given letter <sub> B </sub> and <em>k</em> = 3, we have <em>x</em> = 1, <em>y</em> = 1 + 3 mod 26 = 4, and <em>w</em> = <sub> E </sub>. As <sub> B </sub> is in uppercase, the encrypted letter is <sub> e </sub>.

<strong>Requirement:</strong>

Implement a function  CasesarShift()  which takes in a  char c  and an  int k , where  c  is the character to undergo Caesar Shifting and <sub> k </sub> is the number of positions (can be negative) to shift, and return the processed <sub> char </sub> after Caesar Shifting. The function prototype is given by:

char CaesarShift(char c, int k)

You can ONLY use the simple data types  char ,  bool ,  int ,  double . In other words, you are not allowed the use other data types or data structures such as strings, arrays, vectors, etc.

<strong>Sample Test Cases</strong>

User inputs are shown in blue.

4_1

e 1 ! !

4_2

e 3 a B c D e !

DeFgH!

4_3

<ul>

 <li>3 D e F g H ! aBcDe!</li>

</ul>

4_4

<ul>

 <li>-1 H e l l o E N G G 1 3 4 0 / C O M P 2 1 1 3 ! gDKKNdmff1340/bnlo2113!</li>

</ul>

4_5

d 10 n 3 V 3 D 3 N _ M Y N 3 _ S C _ N 3 L E Q Q 3 N _ M Y N 3 ! D3l3t3d_cod3_is_d3bugg3d_cod3!

<strong>Problem 5: Bounding Boxes</strong>

Write a C++ program to compute a <strong>minimum-sized</strong> axis-aligned bounding box (AABB) for a set of input 2D geometries. An AABB is a rectangle with sides parallel to the x-, y-axes which encloses some given geometries. The input and output of your program are as follows:

<strong>Input:</strong> Each line of the user input begins with a character indicating the type of geometry, followed by some parameters of the geometric object. The input line can be one of the followings:

R  <em>x</em> <em>y</em> <em>width</em> <em>height</em>

where <sub> R </sub> represents an input rectangle, <em>x</em>, <em>y</em> are floating-point numbers for the x-, y-coordinates of the rectangle center, <em>width</em> and <em>height</em> are floating-point numbers for the rectangle size along the x- and y-axes, respectively.

C  <em>x</em> <em>y</em> <em>radius</em>

where <sub> C </sub> represents an input circle, <em>x</em>, <em>y</em> are floating-point numbers for the x-, y-coordinates of the circle center, and <em>radius</em> is a floating-point number for the radius of the center

P  <em>n</em> <em>x</em><sub>1</sub> <em>y</em><sub>1</sub> <em>x</em><sub>2</sub> <em>y</em><sub>2</sub> … <em>x<sub>n</sub></em> <em>y<sub>n</sub></em>

where <sub> P </sub> represents an input point set, <em>n</em> is an integer indicating the number of points in the set, and <em>x<sub>i</sub></em>, <em>y<sub>i</sub></em>, <em>i </em>= 1,…,<em>n</em> are floating point numbers for the x-, y-coordinates of the <em>n</em> points

<h2><a name="_Toc13660"></a> #</h2>

indicates end of input

<strong>Output:</strong>

A single line

<em>x</em> <em>y</em> <em>width</em> <em>height</em>

where <em>x</em> and <em>y</em> are floating-point numbers for the x-, y-coordinates of the center of the minimumsized AABB, <em>width</em> and <em>height</em> are floating-point numbers giving the sizes of the AABB along the x-, y-axes, respectively.

<strong>Requirement:</strong>

Use the  double  data type for floating point calculations.

Implement the functions  RectangleBB() ,  CircleBB()  and  PointSetBB()  which take user inputs and calculate the corresponding bounding boxes of the different geometries (rectangles, circles &amp; point sets). The function prototypes are:

void RectangleBB(double &amp;xmin, double &amp;xmax, double &amp;ymin, double &amp;ymax)

void CircleBB(double &amp;xmin, double &amp;xmax, double &amp;ymin, double &amp;ymax)

void PointSetBB(double &amp;xmin, double &amp;xmax, double &amp;ymin, double &amp;ymax) where  xmin ,  xmax ,  ymin ,  ymax  are the calculated extends of the bounding boxes for the geometry. Note that these parameters are pass-by-reference, since they are the computation results with we would like the calling function to be able to access after function termination. By using pass-by-reference, the functions would be able to modify the actual arguments passed in from the calling function.

You can ONLY use the simple data types  char ,  bool ,  int ,  double . In other words, you are not allowed the use other data types or data structures such as strings, arrays, vectors, etc.

<em>Note</em>:

<strong> The questions assume no bound for the floating-point parameters (</strong><em>x</em><strong>, </strong><em>y</em><strong>, </strong><em>width</em><strong>, </strong><em>height</em><strong>, </strong><em>radius</em><strong>) of the input geometries and therefore they can be any values that a double data type can hold.</strong> You may use  std::numeric_limits&lt;double&gt;::lowest()  and

std::numeric_limits&lt;double&gt;::max()  defined in the header  &lt;limits&gt;  in your program to obtain the smallest and the largest possible values, respectively, for the double data type.

<strong>Sample Test Cases</strong>

User inputs are shown in blue.

5_1

R 0 0 3 2

#

0 0 3 2

5_2

<h2><a name="_Toc13661"></a>C -0.5 3.2 1.6</h2>

<a href="#_Toc13660">#             </a>

<a href="#_Toc13661">-0.5 3.2 3.2 3            2 </a>

<a href="#_Toc13662">5                                                                                                                                                                            3</a>

<a href="#_Toc13663">P 2 3 -2 -1  4 </a>




# 1 1 4 6

<h1><a name="_Toc13662"></a>5_4</h1>

P 3 -1.5 3 3 3 5 3

#

1.75 3 6.5 0

5_5

<h2><a name="_Toc13663"></a>P 2 3 -2 -1 4</h2>

C -0.5 3.2 1.6

P 3 -1.5 3 3 3 5 3

R 0 5.75 3 2

#

1.45 2.375 7.1 8.75