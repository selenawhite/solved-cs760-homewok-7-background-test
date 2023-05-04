Download Link: https://assignmentchef.com/product/solved-cs760-homewok-7-background-test
<br>
<h1>Directed Graphical Model</h1>

Consider the directed graphical model (aka Bayesian network) in Figure ??.

Figure 1: A Bayesian Network example.

Compute <em>P</em>(<em>B </em>= <em>t </em>| <em>E </em>= <em>f,J </em>= <em>t,M </em>= <em>t</em>) and <em>P</em>(<em>B </em>= <em>t </em>| <em>E </em>= <em>t,J </em>= <em>t,M </em>= <em>t</em>). These are the conditional probabilities of a burglar in your house (yikes!) when both of your neighbors John and Mary call you and say they hear an alarm in your house, but without or with an earthquake also going on in that area (what a busy day), respectively.

<h1>2          Chow-Liu Algorithm</h1>

Suppose we wish to construct a directed graphical model for 3 features <em>X</em>, <em>Y </em>, and <em>Z </em>using the Chow-Liu algorithm. We are given data from 100 independent experiments where each feature is binary and takes value <em>T </em>or <em>F</em>. Below is a table summarizing the observations of the experiment:

<em>X      Y       Z      </em>Count

<ol>

 <li>Compute the mutual information <em>I</em>(<em>X,Y </em>) based on the frequencies observed in the data.</li>

 <li>Compute the mutual information <em>I</em>(<em>X,Z</em>) based on the frequencies observed in the data.</li>

 <li>Compute the mutual information <em>I</em>(<em>Z,Y </em>) based on the frequencies observed in the data.</li>

 <li>Which undirected edges will be selected by the Chow-Liu algorithm as the maximum spanning tree?</li>

 <li>Root your tree at node <em>X</em>, assign directions to the selected edges.</li>

</ol>

<h1>3          Kernel SVM</h1>

Consider the following kernel function defined over <em>z,z</em><sup>0 </sup>∈ <em>Z</em>:

<sub>0 </sub>(1    if <em>z </em>= <em>z</em><sub>0</sub><em>, k</em>(<em>z,z </em>) =

0     otherwise.

<ol>

 <li>Prove that for any integer <em>m &gt; </em>0, any <em>z</em><sub>1</sub><em>,…,z<sub>m </sub></em>∈ <em>Z</em>, the <em>m </em>× <em>m </em>kernel matrix <em>K </em>= [<em>K<sub>ij</sub></em>] is positive semi-definite, where <em>K<sub>ij </sub></em>= <em>k</em>(<em>z<sub>i</sub>,z<sub>j</sub></em>) for <em>i,j </em>= 1<em>…m</em>. (Let us assume that for <em>i </em>6= <em>j</em>, we have <em>z<sub>i </sub></em>6= <em>z<sub>j</sub></em>.) Hint: An <em>m </em>× <em>m </em>matrix <em>K </em>is positive semi-definite if ∀<em>v </em>∈ R<em><sup>m</sup></em><em>,v</em><sup>&gt;</sup><em>Kv </em>≥ 0.</li>

 <li>Given a training set (<em>z</em><sub>1</sub><em>,y</em><sub>1</sub>)<em>,…,</em>(<em>z<sub>n</sub>,y<sub>n</sub></em>) with binary labels, the dual SVM problem with the above kernel <em>k </em>will have parameters <em>α</em><sub>1</sub><em>,…,α<sub>n</sub>,b </em>∈ (Assume that for <em>i </em>6= <em>j</em>, we have <em>z<sub>i </sub></em>6= <em>z<sub>j</sub></em>.) The predictor for input <em>z </em>takes the form</li>

</ol>

Recall the label prediction is sgn(<em>f</em>(<em>z</em>)). Prove that there exists <em>α</em><sub>1</sub><em>,…,α<sub>n</sub>,b </em>such that <em>f </em>correctly separates the training set. In other words, <em>k </em>induces a feature space rich enough such that in it any training set can be linearly separated.

<ol start="3">

 <li>How does that <em>f </em>predict input <em>z </em>that is not in the training set?</li>

</ol>

Comment: One useful property of kernel functions is that the input space <em>Z </em>does not need to be a vector space; in other words, <em>z </em>does not need to be a feature vector. For all we know, <em>Z </em>can be turkeys in the world. As long as we can compute <em>k</em>(<em>z,z</em><sup>0</sup>), kernel SVM works on turkeys.

<h1>4          Extra Credit: Kernel functions over discrete space</h1>

Kernel functions can be defined over objects as diverse as graphs, sets, strings, and text documents. Consider, for instance, a fixed set <em>D </em>and define a nonvectorial space consisting of all possible subsets of this set <em>D</em>. If <em>A</em><sub>1 </sub>and <em>A</em><sub>2 </sub>are two such subsets then one simple choice of kernel would be

<em>k</em>(<em>A</em>1<em>,A</em>2) = 2|<em>A</em>1∩<em>A</em>2|

where <em>A</em><sub>1 </sub>∩<em>A</em><sub>2 </sub>denotes the intersection of sets <em>A</em><sub>1 </sub>and <em>A</em><sub>2</sub>, and |<em>A</em>| denotes the size of <em>A</em>. Show that this is a valid kernel function, by showing that it corresponds to an inner product in a feature space. Solution goes here.

<h1>5          Extra Credit: Support Vector Machines</h1>

Given data {(<em>x<sub>i</sub>,y<sub>i</sub></em>)<em>,</em>1 ≤ <em>i </em>≤ <em>n</em>}, the (hard margin) SVM objective is

s.t. <em>y<sub>i</sub></em>(<em>w</em><sup>&gt;</sup><em>x<sub>i </sub></em>+ <em>b</em>) ≥ 1(∀<em>i</em>)<em>.</em>

The dual is

s.t. <em>α<sub>i </sub></em>≥ 0(∀<em>i</em>)<em>, </em><sup>X</sup><em>α<sub>i</sub>y<sub>i </sub></em>= 0<em>.</em>

<em>i</em>=1

Suppose the optimal solution for the dual is, and the optimal solution for the primal is

(<em>w</em><sup>∗</sup><em>,b</em><sup>∗</sup>). Show that the margin

satisfies

<em>.</em>

Hint: use the KKT conditions. Solution goes here.