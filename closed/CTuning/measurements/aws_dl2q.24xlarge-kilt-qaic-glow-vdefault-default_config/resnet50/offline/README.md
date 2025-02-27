This experiment is generated using the [MLCommons Collective Mind automation framework (CM)](https://github.com/mlcommons/ck).

*Check [CM MLPerf docs](https://github.com/mlcommons/ck/tree/master/docs/mlperf) for more details.*

## Host platform

* OS version: Linux-5.10.209-198.812.amzn2.x86_64-x86_64-with-glibc2.2.5
* CPU version: x86_64
* Python version: 3.8.16 (default, Aug 30 2023, 23:19:34) 
[GCC 7.3.1 20180712 (Red Hat 7.3.1-15)]
* MLCommons CM version: 1.6.2
* MLCommons Git https://github.com/mlcommons/inference.git (f9a643c0a0e920588da1b51a1d822e1071a9dbec)
* MLCommons Git https://github.com/mlcommons/inference.git (486a629ea4d5c5150f452d0b0a196bf71fd2021e)


## CM Run Command

See [CM installation guide](https://github.com/mlcommons/ck/blob/master/docs/installation.md).

```bash
pip install -U cmind

cm rm cache -f

cm pull repo ctuning@mlcommons-ck --checkout=8fa78bed48f9dc8299789ce5aa27f7dd67c5a3c1

cm run script \
	--tags=generate-run-cmds,inference,_submission,_all-scenarios \
	--model=resnet50 \
	--implementation=qualcomm \
	--device=qaic \
	--backend=glow \
	--category=datacenter \
	--division=closed \
	--quiet \
	--skip_submission_generation=yes \
	--execution-mode=valid \
	--offline_target_qps=153000 \
	--server_target_qps=149000 \
	--adr.mlperf-inference-implementation.tags=_dl2q.24xlarge
```
*Note that if you want to use the [latest automation recipes](https://access.cknowledge.org/playground/?action=scripts) for MLPerf (CM scripts),
 you should simply reload ctuning@mlcommons-ck without checkout and clean CM cache as follows:*

```bash
cm rm repo ctuning@mlcommons-ck
cm pull repo ctuning@mlcommons-ck
cm rm cache -f

```

## Results

Platform: aws_dl2q.24xlarge-kilt-qaic-glow-vdefault-default_config

### Accuracy Results 
`acc`: `75.864`, Required accuracy for closed division `>= 75.6954`

### Performance Results 
`Samples per second`: `153133.0`
