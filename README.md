# Networking for Big Data Laboratory
## Load Balancing
### Definitions
* Consider a cluster of 2 servers to which a flow of jobs is
offered through a dispatcher.
* Jobs arrive at the dispatcher according to a Poisson process
with mean rate Λ.
* Job workload is distributed as a Pareto random variable L with
Complementary Cumulative Distribution Function (CCDF):

<img src="https://render.githubusercontent.com/render/math?math=G_L(x) = P(L>x) = (\frac{b}{c})^\alpha ">  , x>= b
 
* Task processing time at server j is <img src="https://render.githubusercontent.com/render/math?math=X_j = \frac{L}{\mu _j}"> , j = 1, 2, where μ1 and μ2 are processing rates of the two servers.
* Servers use FCFS scheduling.

### Formulas and numerical values
* The first two moments of L are:
<img src="https://render.githubusercontent.com/render/math?math=E[L] = \frac{\alpha b}{\alpha -1}">
<img src="https://render.githubusercontent.com/render/math?math=E[L^2] = \frac{\alpha b^2}{\alpha -2}">

*The system load is <img src="https://render.githubusercontent.com/render/math?math=\rho = \frac{\Lambda E[L]}{\mu _1 + \mu _2}">

* Numerical values are as follows:
+ <img src="https://render.githubusercontent.com/render/math?math=005 \leqslant \rho \leq 0.9">
+ <img src="https://render.githubusercontent.com/render/math?math=\mu_2 = 10 and \mu _1 = 1">
+ <img src="https://render.githubusercontent.com/render/math?math=\alpha = 2.01, 2.05, 2.25"> (three different values) and E[L] = 1

### Assignment
* Consider SITA policy. With a given workload threshold θ,
state a queueing model of the two server cluster.
  + Identify the arrival processes at queue 1 and 2. Motivate your
models.
  + Identify the service time probability distributions at server 1
and server 2.
  + Write the expression of the mean delay E[D] through the two
server cluster.

* State the optimization problem to find the workload threshold <img src="https://render.githubusercontent.com/render/math?math=\theta^*"> that minimizes E[D]. Solve the problem numerically.
* With <img src="https://render.githubusercontent.com/render/math?math=\theta = \theta^* ">, Plot E[D] as a function of \rho 
* Repeat points 1-3 above assuming random routing, where an
arriving task is assigned to server 1 with probability p, to
server 2 with probability 1 − p. Set <img src="https://render.githubusercontent.com/render/math?math= p = p^∗ "> to minimize E[D].

Page 263
