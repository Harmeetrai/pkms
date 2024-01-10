In the case of [[gaussian elimination]], the [[algorithm]] requires that [[matrix pivot|pivot elements]] not be zero. Interchanging rows or columns in the case of a zero pivot element is necessary. The system below requires the interchange of rows 2 and 3 to perform elimination.
$$
\left[{\begin{array}{ccc|c}1&-1&2&8\\0&0&-1&-11\\0&2&-1&-3\end{array}}\right]
$$
The system that results from pivoting is as follows and will allow the elimination algorithm and backwards substitution to output the solution to the system.
$$
\left[{\begin{array}{ccc|c}1&-1&2&8\\0&2&-1&-3\\0&0&-1&-11\end{array}}\right]
$$