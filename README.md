# application-week-4-p0-solved
**TO GET THIS SOLUTION VISIT:** [Application Week 4 P0 Solved](https://www.ankitcodinghub.com/product/application-p0-solved-4/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;124726&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;3&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (3 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;Application Week 4  P0 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (3 votes)    </div>
    </div>
Application of Matlab for Finance

Week 4

I Portfolio Optimization

I Minimize portfolio variance https://.comI Maximize the Sharpe ratio

I Global minimum variance portfolio (GMVP)

I Optimization with constraints

I Construct the efficient frontierAdd Harvard Management Company Case Study

I On a daily basis, you need to make investment decisions to allocate capital across a range of asset classes in order to satisfy yourhttps://.com investors.

I File HMC data.xls reports relevant information on the real return of 12 asset classes: mean, standard deviation and variancecovariance matrix.Add

I You’d like to visually explore the data to understand the relationship between risk (standard deviation) and return among these assets.

Read Data &amp; Scatter Plot

Assignment Project Exam

Help1 [num, txt] = xlsread(‘HMC data.xls’);

2 % read mean, std deviation and covariance matrix 3 avg_ret = num(:,1);

4 stdev = num(:,2); 5 cov_mat = num(:,3:end);

https://.com

1

figure

2

scatter(stdev, avg_ret, 40,’filled’); % 40mm circle area …

with filled color

3 title(Add ‘Scatter Plot’);

4 xlabel(‘Risk (%)’);

5 ylabel(‘Return (%)’);

6 xlim([0 25]); % x-axis limits

7 ylim([0 10])

Scatter Plot

https://.com

Add

The Investment Decision

I The scatter plot confirms the traditional finance mantra I Higher risk, higher return.

I However, to efficiently manage your funds, you want the benefit of diversification in order to reduce risk.

I To do so, you will construct a portfolio contains these 12 assets,https://.com with a weight ωi of your capital invested in asset i.

I Your objective is to find the optimal investment weight combination wAdd = [ω1,ω2,…,ω12]0 so that your portfolio variance σ2 (i.e., the risk level) is the minimum.

I Meanwhile, sum of your weights equals to 1 as you invest all of your capital without borrowing.

Compute Portfolio Variance

I w = [ω1,ω2,…,ω12]0 is a column vector (12×1) representing weights

of capital allocated to different assets.

I Σ is the variance-covariance matrix with size (12×12)

I By definition, the portfolio variance can be calculated by

https://.comw (1)

I That is, portfolio is a function of the weight vector w.

I The optimization problem is to find the optimal weightAdd combination w that minimizes the function outputwith a constraint

that sum of the portfolio weights w is 1.

I We term such optimal portfolio as the Global Minimum Variance Portfolio (GMVP).

Global Minimum Variance Portfolio (GMVP)

I Formulate such portfolio optimization problem as follows: w

s.t. 10w = 1

wherehttps://.com1 is a column vector of 1 with size (12×1). and

I We want to find the optimal w and the corresponding minimized

fmincon Optimization:

I x = fmincon(fun,x0,A,b,Aeq,beq,lb,ub,nonlcon,options)

A · x ≤ b

minf (x) Aeq · x = beq x lb

≤ x ≤ ub

fmincon

I funhttps://.com: the name of the objective function whose value to minimize

I x0: the starting point value of input x

I A,b, Aeq, beq, lb, ub: elements to define constraints

I nonlconAdd : the indicator for nonlinear constraint function I

If no specific value used, use [] to skip

I options: define for iterations, limits, increments for the optimization

process as well as screen display. Optimisation:

fmincon

I x1 = fmincon(@myfun(x),x0,..) finds the optimal value x1 that minimizes the result of function myfun, with starting point

at x0.

I x1 = fmincon(@(x)myfun(x,y),x0,..) is the same as above https://.comI the function myfun(x,y) requires 2 inputs

I @(x) defines that x is the optimizer and treats y as a constant

I [x1, fval1] = fmincon(@(x)myfun(x,y),x0,..) is the same as above, but with two outputsAdd

I x1 is the optimal value of x that minimizes the function output

I fval1 is the minimized value of myfun

fmincon I

fval1 = myfun(x1,y) Optimisation:

I x1 = fmincon(@myfun(x),x0,A,b) specifies the 1st type of constraint A*x≤b

I x1 = fmincon(@myfun(x),x0,A,b,Aeq,beq) has 2 types of constraintshttps://.comAeq*x = beq, in addition to A*x≤b.

I x1 = fmincon(@myfun(x),x0,[],[],Aeq,beq) has 1 type of constraint Aeq*x = beq only.

fmincon

I x1 = fmincon(@myfun(x),x0,A,b,Aeq,beq,lb,ub) has all 3 types of constraints with additional lower and upper bounds onAdd x, so that the solution is always in the range lb≤x≤ub.

Step 1: Define the Objective Function

I Going back to our global minimum variance portfolio question w

s.t. 10w = 1

I Create a function file namedhttps://.comcompute_pvar outputs the portfolio

variance (pvar) with inputs weight vector (w) and covariance

matrix (cov_mat)

Add 1 function [pvar] = compute_pvar( w, cov_mat ) 2

3 % w is a column

vector 4 pvar = w’ * cov_mat * w; 5

Step 2: Define the Constraint

w s.t. 10w = 1

I Compare the actual constraint against the 3 types of constrainthttps://.com

formats, and find the matching type

10w = 1

Add A · x ≤ b

Aeq · x = beq

lb ≤ x ≤ ub

I Aeq = 10 = [1,1,..,1]

I beq = 1

Step 3: Optimize w1 = fmincon(@(w)compute_pvar(w, cov_mat),

w0, [], … [], Aeq, beq,..)

1 % constraint: sum of weights is 1

2 N = length(avg_ret);

3 Aeq = ones(1, N);

4 beq = 1;

5 w0 =

% starting weight

6 % suppress message display

7 options = optimset(‘Display’, ‘off’);

9 8

% option 1: return optimal weight vector w1

10

w1 = fmincon(@(w)compute_pvar(w, cov_mat), w0, [], [],Add

Aeq, beq, [], [], [], options);

11 % option 2: return both the optiomal weight w1

12 % and the minimized portfolio variance pvar1

13 [w1,pvar1] = fmincon(@(w)compute_pvar(w, cov_mat), w0, …

[], [], Aeq, beq, [], [], [], options);

14 disp([‘The variance of GMVP is ‘, num2str(pvar1)]);

With Further Constraints

I Add two more constraints to the portfolio variance optimization:

I NO short-selling is allowed. That is wi ≥ 0 ∀i ∈ [1,N].

I Diversification Requirements: NO individual asset class can have a https://.comweight greater than 20%. That is wi ≤ 0.2 ∀i ∈ [1,N].

I The portfolio optimization problem is formulated as:

w

Add s.t. 10w = 1

0 ≤ wi ≤ 0.2 ∀i ∈ [1,N]

With Further Constraints

I Same objective function compute_pvar

I Define the constraints

0

With Further Constraints

Aeq · x = beq

Add lb ≤ x ≤ ub

I Aeq= 10 = [1,1,..,1], and beq = 1

With Further Constraints

I lb = [0,0,..,0] and ub =[0.2,0.2,..,0.2]

With Further Constraints

1 %% With Further constraints

2 % weights with ceiling (20%) and no short sell

3 Aeq = ones(1, N);

4 beq = 1;

5 lb = zeros(1,

6 ub = ones(1,N) * 0.2;

7 8 w0 = ones(N,1)*(1/N); % initial weight

9 w2 = fmincon(@(w)compute_pvar(w, cov_mat), w0, [], [], …

10

[w2,pvar2] = fmincon(@(w)compute_pvar(w, cov_mat), w0,Add

[], [], Aeq, beq, lb, ub, [], options);

11 disp([‘The minimised portfolio variance is ‘, … num2str(pvar2)]);

With Further Constraints

Dataset Overviews

Optimization

With a Target Return

I Minimize portfolio variance for a given target return 10%

min w0Σw

s.t. 10w = 1

https://.comr0w = 10%

where r is the column vector of asset returns (avg_ret).

Add A · x ≤ b

Aeq · x = beq

lb ≤ x ≤ ub

I Aeq =, and beq =

Maximize Sharpe Ratio

With a Target Return

Maximize Sharpe Ratio

1 %% With a target return of 10%

2 Aeq = [ones(1,N); avg_ret’];

3 beq = [1; 10];

5 w0 = ones(N,1)*(1/N);

6 w3 = fmincon(@(w)compute_pvar(w, cov_mat), w0, [], [], … Aeq,

beq, [], [], [], options);

7 [w3,pvar3] = fmincon(@(w)compute_pvar(w, cov_mat), w0, … Add

[], options);

8 disp([‘The minimised portfolio variance is ‘, … num2str(pvar3)]);

I The portfolio Sharpe Ratio is calculated as

Maximize Sharpe Ratio

Assignment ProjSharpe Ratio =ectrp − rf Exam Help

rp = w0r σp = w0Σw

rp is the portfolio return, r is the vector of individual asset’s average

returnhttps://.com

I Step 1: Define the function

1 function [p_sharpe] = compute_sharpe(w, avg_ret, …

Add cov_mat )

2 % w and avg_ret are column vectors

3 pvar = w’ * cov_mat * w;

Maximize Sharpe Ratio

4

pret = w’ * avg_ret;

5 % assume risk free rate =

3% annually

6 % 3 as return in

percentage

7

p_sharpe= (pret – 3) / sqrt(pvar);

8

end

Maximize Sharpe Ratio

I Maximise the Sharpe ratio allows a relative optimization

I For the same level of risk σp, max Sharpe = max return rp

I For the same level of return rp, max Sharpe = min risk σp I Sharpe ratio is a function of portfolio weight f (w)

I The formulation of our maximization problem ishttps://.com max SR = f (w) s.t. 10w = 1

Maximize Sharpe Ratio

which is equivalent to the following minimization problem:Add min − SR = −f (w) s.t.

10w = 1

I Put a negative sign – on the compute_sharpe objective function: maximization problem into a minimization one:

Construct Efficient Frontier

1 %% Maximize Sharpe ratio

2 Aeq = ones(1,N); 3 beq = 1;

ones(N,1)*(1/N);

4

6 % NOTE: use – to convert max optimization to a min … optimization problem

7 w4 = fmincon(@(w)-compute_sharpe(w, avg_ret, …

Maximize Sharpe Ratio

cov_mat), w0, [], [], Aeq, beq, [], [], [], …

powcoderoptions);

8 [w4,fval4] = fmincon(@(w)-compute_sharpe(w, avg_ret, … cov_mat), w0, [], [], Aeq, beq, [], [], [], … options);

9 % fval4 = -sr1 as the fun = -compute_sharp fval4;

10 sr = –

11 disp([‘The maximised portfolio Sharpe ratio is ‘, … num2str(sr)]);

Construct Efficient Frontier

I The efficient frontier is the best return vs. risk investment

risky assets. combinations that one can obtain via portfolio diversification on I All assets that lie on the frontier are the most efficient.

I Any asset that is inside the frontier is not efficient or optimal

Maximize Sharpe Ratio

I To construct the efficient frontier, we minimize the portfolio variancehttps://.com for a range of target returns. I We exclude Cash since it is the risk-free asset.

I Loop through all target return levels, find the optimal portfolioAdd weights that minimize the portfolio risk with respect to the target

return.

Construct Efficient Frontier

I With the optimal weights, calculate the portfolio variance and plot against the target return.

Construct Efficient Frontier

1 target_ret = 3:0.2:15;

2

3 M = length(target_ret); w0

pstdevs = zeros(M,1); % empty maxtrix for portfolio stdev 4 = ones(N-1,1)*(1/N-1);

5 https://.com

6 % Minimize variance for a range of target returns

7 for i=1:M %N-1 and end-1 to exclude cash

Construct Efficient Frontier

8 Aeq = [ones(1,N-1); avg_ret(1:end-1)’]; 9 beq = [1; target_ret(i)];

Add 1:end-1)), w0, [], [], Aeq, beq, [], [], [], options); 10 w_opt = fmincon(@(w)compute_pvar(w, cov_mat(1:end-1, …

11 pstdevs(i) = sqrt(compute_pvar(w_opt, … cov_mat(1:end-1, 1:end-1)));

12 end

I Plot the efficient frontier

Construct Efficient Frontier

1 % plot https://.com2 figure

3 plot(pstdevs, target_ret)

4 hold on % hold on and add individual assets without cash

5 scatter(stdev(1:end-1), avg_ret(1:end-1), 40, ‘filled’);

6 title(‘Efficient Frontier’) Add 7 xlabel(‘Risk (%)’);

Construct Efficient Frontier

8 ylabel(‘Return (%)’) https://.com

Add

Dataset

Overviews Optimization

TakeAway

I After today’s class, you will be able to finish the Coursework Question 1.

Dataset Overviews Optimization

I Ensure that you write relevant comments on your CW code.https://.com I When define the function for calculation, the dimensions of mean and standard deviation in the CW are not the same as in this class exercises’. Write the codes accordingly.

I Do not forget to assume your risk free rate.Add
