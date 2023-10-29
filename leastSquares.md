# Least square solution
We have an unknown system with a vector-valued input function $$\overrightarrow{x}$$ in an $$n$$ dimensional space and outputs $$y$$ in real space. This system can be defined as $$y=f(\overrightarrow{x})$$, as shown in the figure.

![systemPic](https://github.com/makeabhishek/Numerical-optimization/assets/47937684/98f107fc-7c99-474f-b716-1599d4245bf2)

Let's we have some data points corresponding to the input and output. 

\begin{equation}
$$ \overrightarrow{x}_1 \rightArrow y_1 $$ \\
$$ \overrightarrow{x}_2 \rightArrow y_2 $$ \\
$$ \overrightarrow{x}_3 \rightArrow y_3 $$ \\
$$ \overrightarrow{x}_4 \rightArrow y_4 $$ \\
$$ . \quad \quad. \quad \quad. $$ \\
$$ . \quad \quad. \quad \quad. $$ \\
$$ . \quad \quad. \quad \quad. $$ \\
$$ \overrightarrow{x}_k \rightArrow y_k $$ \\
\end{equation}

Using these data points, we can model the function defined by the system. We can find the solution by minimising the error. between observed data and calculated data obtained from $$y=f(\overrightarrow{x})$$ by using Least squares (LSQR).
𝑋=[■8(𝑥_11&𝑥_12&…&𝑥_1𝑘@𝑥_21&𝑥_22&…&𝑥_2𝑘@.&.&…&.@.&.&…&.@𝑥_𝑛1&𝑥_𝑛2&…&𝑥_𝑛𝑘 )]_(𝑛×𝑘)

Matrix of Input vectors, 𝑘 samples of 𝑛−dimensional vectors.

![image](https://github.com/makeabhishek/Numerical-optimization/assets/47937684/e95ea779-9ba8-43ca-8f0e-ae86754895fc)


To utilise the LSQR method, define the data points in terms of matrices.
\begin{equation}
X = 
𝑌_(1×𝑘)=𝜃_(1×𝑛)∙𝑋_(𝑛×𝑘)
\begin{equation}
To solve this system of equations, multiply the equation on both sides by 𝑋^𝑇.
𝑌𝑋^𝑇=𝜃 𝑋𝑋^𝑇
𝑋𝑋^𝑇 is a square matrix, we can multiply both side of the equation by inverse of this matrix.
𝑌𝑋^𝑇 (𝑋𝑋^𝑇 )^(−1)=𝜃  ⏟(𝑋𝑋^𝑇 (𝑋𝑋^𝑇 )^(−1) )┬(=𝐼)
𝜃=𝑌 ⏟(𝑋^𝑇 (𝑋𝑋^𝑇 )^(−1) )┬(𝑋^† )
𝑋^† is a pseudo inverse of non-square matrix.
This is the general solution of linear equation and 𝜃 guarantees the minimum amount of sum of errors between observed and calculated data of 
