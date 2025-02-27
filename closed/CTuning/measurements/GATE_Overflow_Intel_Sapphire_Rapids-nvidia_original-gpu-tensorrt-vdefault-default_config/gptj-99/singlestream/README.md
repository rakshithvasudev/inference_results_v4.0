This experiment is generated using the [MLCommons Collective Mind automation framework (CM)](https://github.com/mlcommons/ck).

*Check [CM MLPerf docs](https://github.com/mlcommons/ck/tree/master/docs/mlperf) for more details.*

## Host platform

* OS version: Linux-6.2.0-39-generic-x86_64-with-glibc2.29
* CPU version: x86_64
* Python version: 3.8.10 (default, Nov 22 2023, 10:22:35) 
[GCC 9.4.0]
* MLCommons CM version: 1.6.2
* MLCommons Git https://github.com/mlcommons/inference.git (f9a643c0a0e920588da1b51a1d822e1071a9dbec)


## CM Run Command

See [CM installation guide](https://github.com/mlcommons/ck/blob/master/docs/installation.md).

```bash
pip install -U cmind

cm rm cache -f

cm pull repo ctuning@mlcommons-ck --checkout=af65bfb810cb398dc98881568a73c897e3bfd2d7

cm run script \
	--tags=generate-run-cmds,inference,_submission,_all-scenarios \
	--model=gptj-99 \
	--implementation=nvidia-original \
	--device=cuda \
	--backend=tensorrt \
	--category=edge \
	--division=open \
	--quiet \
	--results_dir=/home/cmuser/results_dir \
	--skip_submission_generation=yes \
	--execution-mode=valid
```
*Note that if you want to use the [latest automation recipes](https://access.cknowledge.org/playground/?action=scripts) for MLPerf (CM scripts),
 you should simply reload ctuning@mlcommons-ck without checkout and clean CM cache as follows:*

```bash
cm rm repo ctuning@mlcommons-ck
cm pull repo ctuning@mlcommons-ck
cm rm cache -f

```

## Results

Platform: GATE_Overflow_Intel_Sapphire_Rapids-nvidia_original-gpu-tensorrt-vdefault-default_config

### Accuracy Results 
`ROUGE1`: `43.0133`, Required accuracy for closed division `>= 42.55663`
`ROUGE2`: `20.1143`, Required accuracy for closed division `>= 19.92226`
`ROUGEL`: `29.9807`, Required accuracy for closed division `>= 29.68822`
`GEN_LEN`: `4030164.0`, Required accuracy for closed division `>= 3615190.2`

### Performance Results 
`90th percentile latency (ns)`: `1204944324.0`
