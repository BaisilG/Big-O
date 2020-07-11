# Big-O


// What is the Big O of the below function? (Hint, you may want to go line by line)
function anotherFunChallenge(input) {
  let a = 5;
  let b = 10;
  let c = 50;
  for (let i = 0; i < input; i++) {
    let x = i + 1;
    let y = i + 2;
    let z = i + 3;

  }
  for (let j = 0; j < input; j++) {
    let p = j * 2;
    let q = j * 2;
  }
  let whoAmI = "I don't know";
}


Big-Oh, Big-Omega, and Big-Theta are three different time-complexity notations for asymptotic analysis. Any time you run a program, that program is going to take up resources from the computer—which will take up processing time or memory (space). The goal of Big-Oh, Big-Omega, and Big-Theta and asymptotic analysis in general is to analyze how much time a program will take (the performance behavior of an algorithm) with regards to an increasing amount of input.

Asymptotic analysis relies on the use of asymptotes, which in mathematics are lines that a given curve approaches or never touches—in the context of algorithms, the curves are plotted on a graph with running time as the y-axis and input size as the x-axis. Asymptotes can act as an upper bound (Big_Oh), lower bound (Big Omega), or both/a tight bound (Big-Theta).

Big-Oh is an upper asymptotic bound for an algorithm, useful for evaluating worst-case performance. The mathematical definition is: A function  T(x)  is upper bounded by  O(F(x))  if there exists a constant  c>0  and  x0>0  such that  T(x)<=cF(x)  when  x>=x0 . What this means is that at some point, when our input  x  is  >=  a positive threshold  x0 , the processing time  T(x)  is going to always be under the bounding function  F(x)  multiplied by some constant. In the below example, the function in green is  y0=x2  and the function in red is  y1=0.2x+5 . In this case  O(x2)  qualifies as a Big-Oh upper bound for the function  y1=0.2x+5  because once  x  reaches some value  x0  (between 0 and 5),  y1  will always be less than  x2  ( c=1 ,  F(x)=x2 ,  cF(x)=x2 ).


Big-Omega is a lower asymptotic bound for an algorithm, useful for evaluating best-case performance of an algorithm. It’s essentially the opposite of Big-Oh.  T(x)  is bounded by  Ω(F(x))  if there exists a constant  c>0  such that  T(x)  is always  >=cF(x)  when  x>=  a positive threshold  x0 .

For example, the function  y=(logx)5  (red) is Big-Omega bounded by  log(x)  (blue) because for all values of  x>=  the threshold  1 ,  y=(logx)2>log(x) .


The problem with Big-Oh and Big-Omega is that they are not the tight bound. For instance, with a linear function, you can have  O(x2) ,  O(x3) ,  O(x4) , or even something crazy like  O(x!)  as the upper bound. This is why in the software engineering industry and in coding interviews, Big-Oh informally refers to the next form of asymptotic analysis, Big-Theta, which represents the tight bound to a function. It provides greater accuracy and meaning than Big-Oh (upper bound) or Big-Omega (lower bound) because it’s mathematical definition is more restrictive.

Big-Theta is the tight (most accurate) asymptotic bound for an algorithm. It isn’t an upper bound or lower bound, but it’s the bound that matches closest to the behavior of an algorithm (both an upper bound and a lower bound at the same time). In industry, this is by far the most commonly used form of asymptotic algorithm analysis. The mathematical definition is that a function  T(x)  is bounded by  Θ(F(x))  if  F(x)  is both an upper bound ( O(F(x) ) and a lower bound ( Ω(F(x)) ) for  T(x) . In other words, there exists constants  c1>0 ,  c2>0 , and  x0>0  such that  T(x)  is always  >=c1F(x)  and  T(x)  is always  <=c2F(x)  when  x  is  >=  a threshold  n0 .

For example, with the function  y=x+x−−√  (red), the Big-Theta bound is  x  (meaning that the function runs in linear time). If we choose  c1=0.5 , then  c1F(x)=0.5x (green), which will always be  <=y=x+x−−√  for any threshold  x0>0  (lower bound). If we choose  c2=2 , then  c2F(x)=2x  (blue), which will always be  >=y+x−−√  at threshold  x0>=1 .


As an extra note, the chart and table in this link is great for evaluating an algorithm’s
