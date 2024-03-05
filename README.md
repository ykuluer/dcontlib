# dcontlib
Dal Control Library

$`u(s)=K_p*e_p(s)+\frac{K_i}{s}*e(s)+\frac{K_t}{s}*e_u(s)+\frac{N}{1+N/s}*K_d*e_d(s)`$

Convert PID Controller from Standard to Parallel Form

$K_p = Gain$ , $K_i = Gain/T_i$ , $K_d = Gain*T_d$ , $`N = T_d/T_f`$

$`u(s)=Gain*(e(s)+\frac{1}{T_i*s}*e(s)+\frac{1}{T_t*s}*e_u(s)+\frac{T_d*N}{1+N/s}*e(s))`$

$`a_1=\frac{2+NT_s}{1+NT_s}`$ ,
$`a_2=-\frac{1}{1+NT_s}`$ ,

$`b_1=Gain`$ ,
$`b_2=-Gain*a_1`$ ,
$`b_3=-Gain*a_2`$ ,

$`c_1=Gain*T_s/T_i`$ ,
$`c_2=a_2c_1`$ ,

$`c_3=Gain*T_s/T_t`$ ,
$`c_4=a_2c_3`$ ,

$`d_1=-Gain*T_dN*a_2`$ ,
$`d_2=-2*d_1`$ ,
$`d_3=d_1`$ ,

$`u(n)=a_1u(n-1)+a_2u(n-2)+b_1e(n)+b_2e(n-1)+b_3e(n-2)+c_1e(n)+c_2e(n-1)+c_3e_u(n)+c_4e_u(n-1)+d_1e(n)+d_2e(n-1)+d_3e(n-2)`$
