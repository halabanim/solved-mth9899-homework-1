Download Link: https://assignmentchef.com/product/solved-mth9899-homework-1
<br>
<strong>Problem 1 </strong>We reviewed the closed form solution for Linear Regression/OLS in class and showed that <em>X<sup>T</sup>e </em>= 0. Explain why the following properties can be derived from this:

<ul>

 <li>Observed values of your features, <em>X </em>are uncorrelated with the residuals <em>e</em></li>

 <li>Sum of residuals is zero i.e. <sup>P</sup><em>e<sub>i </sub></em>= 0</li>

</ul>

(assume that the regression includes a constant term i.e. an intercept) iii Sample mean of the residuals is zero iv <em>y</em>¯ = ¯<em>xβ</em><sup>ˆ </sup>v Predicted values ˆ<em>y </em>are uncorrelated with the residuals <em>e</em>

<strong>Problem 2 </strong>.

<ul>

 <li>Ignoring more sophisticated algorithms, like the <a href="https://en.wikipedia.org/wiki/Strassen_algorithm">Strassen algorithm, </a>multiplying an <em>a </em>× <em>b </em>matrix by a <em>b </em>× <em>c </em>matrix takes O(<em>abc</em>). Please work out the time complexity of computing a naive <em>K</em>-Fold Cross Validation Ridge Regression on an <em>N </em>× <em>F </em>input matrix.</li>

 <li>We can be more efficient. We don’t have to compute (<em>XX<sup>T</sup></em>)<sup>−1 </sup>completely each time. In particular, if you break up <em>X </em>into <em>K </em>chunks, there is a faster way.</li>

</ul>

<ul>

 <li>Define <em>X</em><sub>−<em>i </em></sub>as X with the <em>i</em>th fold omitted. Given these hints, write a description of how you can efficiently compute for all <em>K </em></li>

</ul>

iii Assume you have a sample of data with <em>N </em>samples and <em>K </em>features i.e. X is of size <em>NxK </em>and target variable <em>Y </em>, a vector of size <em>N</em>. You wish to estimate a Ridge regression model with <em>λ </em>= <em>λ</em><sup>ˆ </sup>to find <em>β</em><sup>ˆ</sup>, a vector of size <em>K </em>s.t. <em>Y </em>= <em>Xβ</em><sup>ˆ </sup>but you are only allowed to use the closed form solution to OLS i.e. <em>β</em><sup>ˆ </sup>= (<em>X<sup>T</sup>X</em>)<sup>−1</sup><em>X<sup>T</sup>y</em>. You are not allowed to modify the existing data in <em>X </em>but you are allowed to append to it. Propose what data you would append to <em>X </em>and <em>Y </em>so that the OLS solution with the modified <em>X </em>and <em>Y </em>is equivalent to the Ridge solution. Justify why this works.

<strong>Problem 3 </strong>We discussed the tradeoff between bias and variance. In this question, we’ll run some simulations to see how <em>λ </em>can affect the variance of <em>β</em>. Attached, you will find python code to generate a number of different datasets for testing, <strong>use the data generating code exactly as provided</strong>. Write Python methods to implement the closed-form solutions for Linear Regression and Ridge Regression, as discussed in class, for use below.

<ul>

 <li>For datasets 1-2 in the code, generate each dataset 1000 times (by calling e.g. <em>get dataset</em>(1) or <em>get dataset</em>(2) each time). For each of these 1000 times, perform simple OLS regression and record the <em>β </em> Plot a histogram of the <em>β </em>values and report the <em>µ<sub>β </sub></em>and <em>σ<sub>β</sub></em><sup>2</sup>. Note that the true betas for data sets 1 and 2 are identical. Explain the differences between the histograms.</li>

 <li>Repeat what you did in (i) above for dataset 3. How does the distribution of the betas change and how do you explain this?</li>

 <li>Repeat the above trials with Ridge Regression instead, using reasonable <em>λ </em> Prepare a graph of how <em>µ<sub>β </sub></em>and <em>σ<sub>β</sub></em><sup>2 </sup>change as a function of <em>λ </em>for each of the datasets – you do NOT need to include histograms of all of your distributions. Explain the outputs.</li>

 <li>For the trials from (iii), calculate and report the effective degrees of freedom (for each dataset and lambda value), to make sure that the <em>λ </em>values you are using are reasonable. You should see effective DOFs from 2 down to less than 1 (See ESLII, equation 3.50, for effective DOF calculation, or <a href="https://web.stanford.edu/~hastie/Papers/df_paper_LJrev6.pdf">this link</a> for more details ).</li>

</ul>