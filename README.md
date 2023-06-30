# gas comparisons between solady and vyper

`pip install eth-ape`

`ape plugins install .`

`ape test --gas`


# output

```
================================= Gas Profile ==================================
                        SoladyToken Gas                         
                                                                
  Method         Times called    Min.    Max.    Mean   Median  
 ────────────────────────────────────────────────────────────── 
  balanceOf                 6   23974   23974   23974    23974  
  allowance                 3   24521   24521   24521    24521  
  transfer                  2   29500   29500   29500    29500  
  approve                   1   24441   24441   24441    24441  
  transferFrom              1   14112   14112   14112    14112  
                                                                
                         VyperToken Gas                         
                                                                
  Method         Times called    Min.    Max.    Mean   Median  
 ────────────────────────────────────────────────────────────── 
  balanceOf                 6   23840   23840   23840    23840  
  allowance                 3   24340   24340   24340    24340  
  transfer                  2   29669   29669   29669    29669  
  approve                   1   24316   24316   24316    24316  
  transferFrom              1   14471   14471   14471    14471  
                                                                
                          OZToken Gas                           
                                                                
  Method         Times called    Min.    Max.    Mean   Median  
 ────────────────────────────────────────────────────────────── 
  balanceOf                 6   23991   23991   23991    23991  
  allowance                 3   24645   24645   24645    24645  
  transfer                  2   30004   30004   30004    30004  
  approve                   1   24735   24735   24735    24735  
  transferFrom              1   14878   14878   14878    14878  
                                                                

============================== 1 passed in 1.52s ===============================
INFO: Stopping 'anvil' process.
```
