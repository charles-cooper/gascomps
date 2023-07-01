# gas comparisons between solady and vyper

`pip install eth-ape ape-huff`

`ape plugins install .`

`ape test --gas`

# Results (reformatted by ChatGPT lol)
```
====================== Gas Profile: Allowance ======================
  
  Contract        Min     Max     Mean    Median  
 ──────────────────────────────────────────────────────── 
  SoladyToken     24521   24521   24521   24521  
  VyperToken      24318   24318   24318   24318  
  OZToken         24645   24645   24645   24645  
  WETH9           24178   24178   24178   24178  
  

====================== Gas Profile: Approve ======================
  
  Contract        Min     Max     Mean    Median  
 ──────────────────────────────────────────────────────── 
  SoladyToken     24441   24441   24441   24441  
  VyperToken      24294   24294   24294   24294  
  OZToken         24735   24735   24735   24735  
  WETH9           24157   24157   24157   24157  
  

====================== Gas Profile: BalanceOf ======================
  
  Contract        Min     Max     Mean    Median  
 ──────────────────────────────────────────────────────── 
  SoladyToken     23974   23974   23974   23974  
  VyperToken      23818   23818   23818   23818  
  OZToken         23991   23991   23991   23991  
  WETH9           23773   23773   23773   23773  


====================== Gas Profile: Transfer ======================
  
  Contract        Min     Max     Mean    Median  
 ──────────────────────────────────────────────────────── 
  SoladyToken     12400   29500   23800   29500  
  VyperToken      12547   29647   23947   29647  
  OZToken         12904   30004   24304   30004  
  WETH9           12110   29210   23510   29210  
  

====================== Gas Profile: TransferFrom ======================
  
  Contract        Min     Max     Mean    Median  
 ──────────────────────────────────────────────────────── 
  SoladyToken     14112   14112   14112   14112  
  VyperToken      14453   14453   14453   14453  
  OZToken         14878   14878   14878   14878  
  WETH9           15257   15257   15257   15257  

```



# output

```
================================= Gas Profile ==================================
                        SoladyToken Gas                         
                                                                
  Method         Times called    Min.    Max.    Mean   Median  
 ────────────────────────────────────────────────────────────── 
  allowance                 6   24521   24521   24521    24521  
  approve                   2   24441   24441   24441    24441  
  balanceOf                10   23974   23974   23974    23974  
  transfer                  3   12400   29500   23800    29500  
  transferFrom              2   14112   14112   14112    14112  
                                                                
                         VyperToken Gas                         
                                                                
  Method         Times called    Min.    Max.    Mean   Median  
 ────────────────────────────────────────────────────────────── 
  allowance                 6   24318   24318   24318    24318  
  approve                   2   24294   24294   24294    24294  
  balanceOf                10   23818   23818   23818    23818  
  transfer                  3   12547   29647   23947    29647  
  transferFrom              2   14453   14453   14453    14453  
                                                                
                          OZToken Gas                           
                                                                
  Method         Times called    Min.    Max.    Mean   Median  
 ────────────────────────────────────────────────────────────── 
  allowance                 6   24645   24645   24645    24645  
  approve                   2   24735   24735   24735    24735  
  balanceOf                10   23991   23991   23991    23991  
  transfer                  3   12904   30004   24304    30004  
  transferFrom              2   14878   14878   14878    14878  
                                                                
                           WETH9 Gas                            
                                                                
  Method         Times called    Min.    Max.    Mean   Median  
 ────────────────────────────────────────────────────────────── 
  0x                        1   46133   46133   46133    46133  
  allowance                 6   24178   24178   24178    24178  
  approve                   2   24157   24157   24157    24157  
  balanceOf                10   23773   23773   23773    23773  
  transfer                  3   12110   29210   23510    29210  
  transferFrom              2   15257   15257   15257    15257  
                                                                

============================== 1 passed in 2.89s ===============================
INFO: Stopping 'anvil' process.

```
