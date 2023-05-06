Download Link: https://assignmentchef.com/product/solved-ee5111-mini-project-3
<br>
<strong>Study of Expectation Maximization (EM) algorithm</strong>

The objective of this exercise is to understand the Expectation Maximization (EM) algorithm. Assume that there are two biased coins, labelled as <em>A </em>and <em>B</em>. Coin <em>A </em>lands up as head with probability <em>p </em>and coin <em>B </em>lands up as head with probability <em>q</em>. An experiment is performed with <em>n </em>independent trials and in each trial, a coin is chosen at random (coin <em>A </em>with probability <em>π </em>and coin <em>B </em>with probability 1 − <em>π</em>) and tossed <em>m </em>times (independently).

Let <em>z</em><sup>(<em>i</em>) </sup>∈ {<em>A,B</em>} be the label of the coin selected and <em>x</em><sup>(<em>i</em>) </sup>∈ {<em>H,T</em>}<em><sup>m </sup></em>be the observed sequence in the <em>i<sup>th </sup></em>trial of the experiment, <em>i </em>∈ 1<em>,</em>2<em>,…,n</em>. The labels of the coins {<em>z</em><sup>(<em>i</em>)</sup><em>,i </em>∈ 1<em>,</em>2<em>,…,n</em>} remain hidden and the observer could only record the faces {<em>x</em><sup>(<em>i</em>)</sup><em>,i </em>∈ 1<em>,</em>2<em>,…,n</em>}. Hence, the observations <em>x</em><sup>(<em>i</em>) </sup>can be considered as <em>i.i.d </em>samples from a <em>Mixture of two Binomial models</em>:

<em>P</em><em><sub>X</sub></em>(<em>x</em>) = <em>π </em>× <em>P</em><em><sub>X</sub></em>(<em>x</em>|<em>z</em><sup>(<em>i</em>) </sup>= <em>A</em>) + (1 − <em>π</em>) × <em>P</em><em><sub>X</sub></em>(<em>x</em>|<em>z</em><sup>(<em>i</em>) </sup>= <em>B</em>)

Our aim is to obtain maximum likelihood estimate for parameter vector <em>θ </em>using Expectation Maximization (EM) algorithm. Generate the observations (<em>x</em><sup>(<em>i</em>)</sup><em>,z</em><sup>(<em>i</em>)</sup>) for following two cases

(i) <em>π </em>= 0<em>.</em>50<em>, p </em>= 0<em>.</em>35 and <em>q </em>= 0<em>.</em>60. (ii) <em>π </em>= 0<em>.</em>25<em>, p </em>= 0<em>.</em>35 and <em>q </em>= 0<em>.</em>60.

Choose <em>m </em>= 1<em>,</em>10 and <em>n </em>= 10<em>,</em>1000<em>,</em>10000. Run the EM algorithm for following experiments

<strong>Experiment: 1 </strong>Assume that we know <em>π</em>. Thus, the vector of parameters is given by <em>θ </em>= [<em>p q</em>]<em><sup>T</sup></em>.

<ul>

 <li>Use observations from case (i) and assume that <em>π </em>= 0<em>.</em>50 and initial estimates are [0<em>.</em>45 0<em>.</em>50]<em><sup>T</sup></em></li>

 <li>Use observations from case (ii) and assume that <em>π </em>= 0<em>.</em>50 and initial estimates are [0<em>.</em>45 0<em>.</em>50]<em><sup>T</sup></em></li>

 <li>Use observations from case (ii) and assume that <em>π </em>= 0<em>.</em>25 and initial estimates are [0<em>.</em>45 0<em>.</em>50]<em><sup>T</sup></em></li>

</ul>

<strong>Experiment: 2 </strong>Assume that we do not know <em>π</em>. Thus, the vector of parameters is given by <em>θ </em>= [<em>π p q</em>]<em><sup>T</sup></em>.

<ul>

 <li>Use observations from case (ii) and initial estimates are [0<em>.</em>50 0<em>.</em>45 0<em>.</em>50]<em><sup>T</sup></em></li>

 <li>Repeat above experiment with initial estimate [0<em>.</em>50 0<em>.</em>50 0<em>.</em>45]<em><sup>T</sup></em></li>

</ul>

<strong>Experiment: 3 </strong>Now use a Beta prior over <em>π</em>. Derive the update equations for MAP estimate. Use the following priors <em>Beta</em>(1<em>,</em>1)<em>,Beta</em>(1<em>,</em>3)<em>,Beta</em>(2<em>,</em>6)<em>,Beta</em>(3<em>,</em>9).

Make the following inferences from the algorithm for the aforementioned choices of <em>n, m </em>and <em>θ</em><strong>ˆ</strong><sub>0</sub>:

1

<ul>

 <li>Plot the <em>learning curve</em><a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a> and show the convergence of the algorithm<a href="#_ftn2" name="_ftnref2"><sup>[2]</sup></a> for each experiment.</li>

 <li>Observe how the final estimate of <em>θ </em>from the algorithm (call it <em>θ</em><strong>ˆ</strong><em><sub>EM</sub></em>), and number of iterations needed for convergence, change when we increase <em>m </em>and <em>n</em>.</li>

 <li>Report your observation about case (b) and case (c) of experiment 1, where in former case we are assuming a wrong value of <em>π </em>and in later case we are assuming the true value of <em>π</em></li>

 <li>Report your observation about experiment 2 when we swap the prior for <em>p </em>and <em>q</em>.</li>

 <li>Compare the result of experiment 3 with the result of experiment 2.</li>

</ul>

<a href="#_ftnref1" name="_ftn1">[1]</a> Plot of the estimate at iteration <em>k</em>, <em>θ</em><strong>ˆ</strong><em><sub>k </sub>vs. </em>iteration index, <em>k</em>.

<a href="#_ftnref2" name="_ftn2">[2]</a> You shall consider that the algorithm has converged at iteration <em>k </em>when the update to any of the parameter is not more than