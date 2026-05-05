# FA-MARL




<br>

Code repository for "Solving Fairness-Aware Heterogeneous Vehicle
Routing Problem with Multi-Agent Reinforcement Learning"





## 🚀 Usage

### Installation

We use [uv](https://docs.astral.sh/uv/getting-started/installation/) for fast installation and dependency management:

```bash
uv venv
source .venv/bin/activate
uv sync --all-extras
```



### Train your own model


```bash
python train.py experiment=hcvrp
```


### Testing

You may run the `test.py` script to evaluate the model, e.g. with greedy decoding:

```bash
python test.py --problem hcvrp --decode_type greedy --batch_size 128
```

(note: we measure time with single instance -- batch size 1, but larger makes the overall evaluation faster), or with sampling:

```bash
python test.py --problem hcvrp --decode_type sampling --batch_size 1 --sample_size 1280
```

### Other scripts

- Data generation: We also include scripts to re-generate data manually (reproducible via random seeds) with `python scripts/generate_data.py`.
