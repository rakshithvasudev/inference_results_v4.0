
# MLPerf Inference v4.0 - closed - Dell

To run experiments individually, use the following commands.

## r760_q4_ultra - bert-99 - offline

### Accuracy  

```
axs byquery loadgen_output,task=bert,sut_name=r760_q4_ultra,model_name=bert-99,framework=kilt,device=qaic,collection_name=experiments_submission,loadgen_mode=AccuracyOnly,loadgen_scenario=Offline,vc:=1:3:3:3:1:3:3:3:1:3:3:3:1:3:3:3
```

### Performance 

```
axs byquery loadgen_output,task=bert,sut_name=r760_q4_ultra,model_name=bert-99,framework=kilt,device=qaic,collection_name=experiments_submission,loadgen_mode=PerformanceOnly,loadgen_compliance_test-,loadgen_scenario=Offline,vc:=1:3:3:3:1:3:3:3:1:3:3:3:1:3:3:3,loadgen_target_qps=7500
```

### Compliance TEST01

```
axs byquery loadgen_output,task=bert,sut_name=r760_q4_ultra,model_name=bert-99,framework=kilt,device=qaic,collection_name=experiments_submission,loadgen_mode=PerformanceOnly,loadgen_compliance_test=TEST01,loadgen_scenario=Offline,vc:=1:3:3:3:1:3:3:3:1:3:3:3:1:3:3:3,loadgen_target_qps=7500
```

### Compliance TEST05

```
axs byquery loadgen_output,task=bert,sut_name=r760_q4_ultra,model_name=bert-99,framework=kilt,device=qaic,collection_name=experiments_submission,loadgen_mode=PerformanceOnly,loadgen_compliance_test=TEST05,loadgen_scenario=Offline,vc:=1:3:3:3:1:3:3:3:1:3:3:3:1:3:3:3,loadgen_target_qps=7500
```

