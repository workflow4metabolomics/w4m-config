# Memory usages of the W4M tools

## 27/08/2018
```bash
qacct -o w4m -d 365 -j > /tmp/qacct-w4m
cat /tmp/qacct-w4m | grep -e maxvmem -e jobname | tr "\n" "|" | sed "s/jobname/\njobname/g" | sed -r "s/jobname +g[0-9]+_//" | sed -r "s/\|maxvmem/\t/" | sed -r "s/\|//" | grep "G$" | sort | less

```

| Tools | Total | >4G | >8G | >10G | >20G | >100G | maxmem
|  - | -: | -: | -: | -: | -: | -: | -:
| abims_CAMERA_annotateDiffreport | 820 | 173 | 11 | 50 | 34 | 10 | 231.761G
| abims_corr_analysis | 200 | 3 | 0 | | | |
| abims_hclustering | 66 | 1 | 0 | | | |
| abims_xcms_fillPeaks | 1131 | 29 | 11 | 9 | 2 | | 30.022G
| abims_xcms_group | 3778 | 15 | 6 | 3 | 1 | | 20.364G
| abims_xcms_retcor | 1384 | 66 | 16 | 14 | 6 | | 37.327G
| abims_xcms_xcmsSet | 31171 | 872 | 121 | 89 | 29 | | 32.627G
| bank_inhouse | 619 | 1 | 0 | | | |  
| Batch_correction | 1094 | 2 | 2 | 1 | | | 19.855G
| biosigner | 276 | 1 | 0 | | | |
| checkFormat | 928 | 1 | 0 | | | |
| generic_filter | 2513 | 4 | 3 | 2 | 1 | | 29.539G
| Heatmap | 348 | 12 | 5 | 3 | 3| | 28.510G
| hr2 | 76 | 1 | 0 | | | |
| metams_runGC | 427 | 5 | 3 | 2 | 2 | | 40.425G
| Multivariate | 4682 | 7 | 7 | 2 | 2 | | 31.113G
| NmrAnnotation | 24 | 1 | 1 | | | |
| NmrBucketing | 161 | 1 | 1 | | | |
| NmrNormalization | 21 | 1 | 1 | | | |
| NMR_Read | 308 | 1 | 1 | | | |
| profia | 20 | 12 | 12 | 12 | 1 | | 28.717G
| Probmetab | 39 | 3 | 1 | | | |
| quality_metrics | 1928 | 6 | 2 | 2 | 1 | | 29.568G
| Univariate | 1869 | 6 | 6 | 3 | | | 19.832G
| wsdl_chemspider | 71 | 64 | 64 | 64 | 64 | | 35.547G
| wsdl_kegg | 158 | 132 | 132 | 132 | 132 | | 35.606G
| wsdl_massbank | 88 | 75 | 75 | 74 | 132 | | 35.545G
