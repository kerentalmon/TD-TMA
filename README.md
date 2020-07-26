# TD-TMA
This is a simulation code to demonstrate localization of underwater target, moving in a uniform motion, by an observer without communication synchronization . It is base on  Time Difference of Arrival receptions of the target's emissions by the observer and utilizing Target Motion Analysis. 
This program runs the Time Difference of Arrival Target Motion Analysis (TD-TMA) algorithm. For convenience, all functions run under the same notebook. The key function is LMM (Levenberg–Marquardt Method) to find the least squares solution of the target. After which a basing hopping algorithm is used to find the global minima from all possible solutions. To compare results to traditional multilateration the class Benchmark is used, which uses 3 TDOA isolines to localize the target. In case the isoline do not intersect at a single point, the Fermat point is chosen. The main variables are:
Xo, Yo - observer coordinates 
RealXt, RealYt - target's true coordinates 
Xt, Yt - target's estimated coordinates (solution of the TD-TMA) 
c - actual speed of sound 
c1 - default speed of sound (1500) 
Ceff - sound velocity a perceived by the target's solution Cbasin - sound velocity found by the TD-TMA algorithm
