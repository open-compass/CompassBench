# CompassBench

CompassBench is the self-built benchmark for the [CompassRank LLM Leaderboard](https://rank.opencompass.org.cn/leaderboard-llm/), we will provide the example data for the benchmark.

## 202407 V1.3

Please check [CompassBench](https://opencompass.readthedocs.io/zh-cn/latest/advanced_guides/compassbench_intro.html) for more information of the benchmark.


```
v1_3_data
    ├── code
    │   ├── compass_bench_coding_cn_val.json
    │   └── compass_bench_coding_en_val.json
    ├── instruct
    │   ├── compass_bench_instruct_cn_val.json
    │   └── compass_bench_instruct_en_val.json
    ├── knowledge
    │   └── single_choice_cn.jsonl
    ├── language
    │   ├── compass_bench_language_cn_val.json
    │   └── compass_bench_language_en_val.json
    ├── math
    │   └── single_choice_cn.jsonl
    └── reasoning
        ├── compass_bench_reasoning_cn_val.json
        └── compass_bench_reasoning_en_val.json
```

- For subjective evaluation, please refer to [CompassBench Subjective Config](https://github.com/open-compass/opencompass/blob/main/configs/eval_compassbench_v1_3_subjective.py)
- For objective evaluation, please refer to [CompassBench Objective Config](https://github.com/open-compass/opencompass/blob/main/configs/datasets/compassbench_v1_3/compassbench_v1_3_objective_gen_068af0.py)

Performance of the example data will be updated soon.

### Evaluation 

- Please link the `v1_3_data` to `data/compassbench_v1_3` within the opencompass directory


```bash
export HUGGINGFACE_HUB_CACHE=/path-to-hf_hub/
export HF_HUB_CACHE=/path-to-hf_hub/
export HF_EVALUATE_OFFLINE=1
export HF_DATASETS_OFFLINE=1
export TRANSFORMERS_OFFLINE=1
# Objective Evaluation
# We use `perf_4` as the final metric
python run.py --models hf_internlm2_chat_1_8b --datasets compassbench_v1_3_objective_gen

# Subjective Evaluation
python run.py configs/eval_compassbench_v1_3_subjective.py
```
