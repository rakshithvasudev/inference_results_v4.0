This experiment is generated using the [MLCommons Collective Mind automation framework (CM)](https://github.com/mlcommons/ck).

*Check [CM MLPerf docs](https://github.com/mlcommons/ck/tree/master/docs/mlperf) for more details.*

## Host platform

* OS version: Linux-6.2.0-1017-aws-x86_64-with-glibc2.35
* CPU version: x86_64
* Python version: 3.10.12 (main, Nov 20 2023, 15:14:05) [GCC 11.4.0]
* MLCommons CM version: 2.0.0
* MLCommons Git https://github.com/mlcommons/inference.git (486a629ea4d5c5150f452d0b0a196bf71fd2021e)
* MLCommons Git https://github.com/mlcommons/inference.git (8219069f83c2396be1c1b4b4c8f80cca756db5ca)
* MLCommons Git https://github.com/neuralmagic/inference (2927a1c2c55bb680a78fdbd78bdd4080f37d0628)


## CM Run Command

See [CM installation guide](https://github.com/mlcommons/ck/blob/master/docs/installation.md).

```bash
pip install -U cmind

cm rm cache -f

cm pull repo ctuning@mlcommons-ck --checkout=12d75c17a629ecfbd14ee1b4ff3b6824ea54ffc9

cm run script \
	--tags=run,mlperf,inference,generate-run-cmds,_submission \
	--adr.python.version_min=3.8 \
	--adr.compiler.tags=gcc \
	--implementation=reference \
	--model=bert-99 \
	--precision=int8 \
	--backend=deepsparse \
	--device=cpu \
	--scenario=Offline \
	--run_submission_checker=no \
	--execution_mode=valid \
	--adr.mlperf-inference-implementation.max_batchsize=128 \
	--results_dir=/home/ubuntu/results_dir \
	--env.CM_MLPERF_NEURALMAGIC_MODEL_ZOO_STUB=zoo:nlp/question_answering/bert-large/pytorch/huggingface/squad/pruned80_quant-none-vnni \
	--quiet
```
*Note that if you want to use the [latest automation recipes](https://access.cknowledge.org/playground/?action=scripts) for MLPerf (CM scripts),
 you should simply reload ctuning@mlcommons-ck without checkout and clean CM cache as follows:*

```bash
cm rm repo ctuning@mlcommons-ck
cm pull repo ctuning@mlcommons-ck
cm rm cache -f

```

## Results

Platform: t3.2xlarge-reference-cpu-deepsparse-vdefault-default_config

### Accuracy Results 
`F1`: `90.26942`, Required accuracy for closed division `>= 89.96526`

### Performance Results 
`Samples per second`: `5.47764`
