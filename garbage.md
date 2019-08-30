% \begin{equation}
% \begin{pmatrix}
% p_{nt}\\
% p_{tt}\\
% p_{si}\\
% p_{ti}
% \end{pmatrix}
% = 
% softmax(
% \begin{pmatrix}
% W_{nt}\\
% W_{tt}\\
% W_{si}\\
% W_{ti}
% \end{pmatrix}
% \times h_{t} + 
% \begin{pmatrix}
% b_{nt} \\
% b_{tt} \\
% b_{si} \\
% b_{ti}
% \end{pmatrix}
% )
% \end{equation}







% \begin{equation}
% \begin{pmatrix}
% q\\
% f\\
% i\\
% o
% \end{pmatrix}
% =
% \begin{pmatrix}
% \sigma \\
% \sigma \\
% \sigma \\
% tanh
% \end{pmatrix}
% M_{k, 2k}
% \begin{pmatrix}
% x_{i} \\
% h_{i-1}
% \end{pmatrix}
% \end{equation}

% \begin{equation}
% c_{i} = f \odot c_{i-1} + i \odot q
% \end{equation}

% \begin{equation}
% h_{i} = o \odot tanh(c_{i})
% \end{equation}












% \begin{table}   
% \begin{subtable}{.5\textwidth}
% \centering
%    \begin{tabular}{ll}
%    \toprule
%    size& 10.77GB \\
%    programs& 100,000\\
%    total terminals& $8.9 \times 10^7$\\
%    total non-terminals& $8.3 \times 10^7$\\
%    \bottomrule
%    \end{tabular}
% \caption{Training set}
% \end{subtable}% <--- new
% \begin{subtable}{.5\textwidth}
% \centering 
%    \begin{tabular}{ll}
%    \toprule
%    size& 5.15GB \\
%    programs& 50,000\\
%    total terminals& $4.3 \times 10^7$\\
%    total non-terminals& $3.9 \times 10^7$\\
%    \bottomrule
%    \end{tabular}
% \caption{Evalution set}
% \end{subtable}

% \begin{subtable}{.5\textwidth}
% \centering 
%    \begin{tabular}{ll}
%    \toprule
%    size& 15.92GB \\
%    programs& 150,000\\
%    total terminals& $1.3 \times 10^8$\\
%    total non-terminals& $1.2 \times 10^8$\\
%    \bottomrule
%    \end{tabular}
% \caption{Overall}
% \end{subtable}
% \caption{Dataset} \label{tab:dataset}
% \end{table}










From this AST dataset, we generate a mass of training samples for Node2Vec models training: both NT2V and TT2V model. 
There are $8.9 \times 10^7$ training samples for NT2V model and the training set for TT2V model contains $8.3 \times 10^7$ training samples.
We also transform all ASTs in the training dataset to the sequences of training samples for N2V-LSTM integration model to predict next tokens. 
There are 100,000 sequences for models training which is equal to the number of ASTs. And there are $1.6 \times 10^8$ training samples in sequences totally. 
