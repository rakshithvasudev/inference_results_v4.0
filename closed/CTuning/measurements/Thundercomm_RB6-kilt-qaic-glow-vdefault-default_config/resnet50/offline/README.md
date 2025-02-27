This experiment is generated using the [MLCommons Collective Mind automation framework (CM)](https://github.com/mlcommons/ck).

*Check [CM MLPerf docs](https://github.com/mlcommons/ck/tree/master/docs/mlperf) for more details.*

## Host platform

* OS version: Linux-4.19.125-aarch64-with-glibc2.27
* CPU version: aarch64
* Python version: 3.8.0 (default, Dec  9 2021, 17:53:27) 
[GCC 8.4.0]
* MLCommons CM version: 1.5.3
* MLCommons Git https://github.com/mlcommons/inference.git (486a629ea4d5c5150f452d0b0a196bf71fd2021e)
* MLCommons Git https://github.com/mlcommons/inference.git (8219069f83c2396be1c1b4b4c8f80cca756db5ca)
* MLCommons Git https://github.com/mlcommons/power-dev.git (f5ee305a867b24905fea1f04f1b68819d392a731)


## CM Run Command

See [CM installation guide](https://github.com/mlcommons/ck/blob/master/docs/installation.md).

```bash
pip install -U cmind

cm rm cache -f

cm pull repo ctuning@mlcommons-ck --checkout=12d75c17a629ecfbd14ee1b4ff3b6824ea54ffc9

cm run script \
	--tags=generate-run-cmds,_submission \
	--implementation=qualcomm \
	--adr.mlperf-inference-implementation.tags=_rb6 \
	--model=resnet50 \
	--execution-mode=valid \
	--power=yes \
	--adr.mlperf-power-client.power_server=192.168.1.166 \
	--env.CM_MLPERF_SHORT_RANGING_RUN=no \
	--division=closed
```
*Note that if you want to use the [latest automation recipes](https://access.cknowledge.org/playground/?action=scripts) for MLPerf (CM scripts),
 you should simply reload ctuning@mlcommons-ck without checkout and clean CM cache as follows:*

```bash
cm rm repo ctuning@mlcommons-ck
cm pull repo ctuning@mlcommons-ck
cm rm cache -f

```

## Results

Platform: Thundercomm_RB6-kilt-qaic-glow-vdefault-default_config

### Accuracy Results 
`acc`: `75.892`, Required accuracy for closed division `>= 75.6954`

### Performance Results 
`Samples per second`: `6941.64`

### Power Results 
`Power consumed`: `27.713 Watts`, `Power efficiency`: `250482.232 samples per Joule`