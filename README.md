# sharpness_aware_minimization
https://arxiv.org/pdf/2010.01412.pdf 을 구현

코드는 https://github.com/davda54/sam를 참고했음. official code https://github.com/google-research/sam 

Main idea:

sharpness + loss 를 minimize한다 -> $L_S^{SAM}$을 minimize하기 위해서, 먼저 sharpness의 정의에서 사용된 epsilon을 구하는데,  max안에 들어가서 grad 방향임, 근데 w+epsilon에서의 loss가  $L_S^{SAM}$으로 근사되기 때문에 원래 자리 + epsilon을 해서 그 자리에서 grad 구하면 원하는 grad

그래서 원래 자리로 다시 가서 그렇게 구한 grad 더해주면 원하는 update가 된거!

sam_exp 확인할것.
