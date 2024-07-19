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
    │   └── compass_bench_knowldge_val.json
    ├── language
    │   ├── compass_bench_language_cn_val.json
    │   └── compass_bench_language_en_val.json
    ├── math
    │   └── compass_bench_math.jsonl
    └── reasoning
        ├── compass_bench_reasoning_cn_val.json
        └── compass_bench_reasoning_en_val.json
```

- For subjective evaluation, please refer to [CompassBench Subjective Config](https://github.com/open-compass/opencompass/blob/main/configs/eval_compassbench_v1_3_subjective.py)
- For objective evaluation, please refer to [CompassBench Objective Config](https://github.com/open-compass/opencompass/blob/main/configs/datasets/compassbench_v1_3/compassbench_v1_3_objective_gen_068af0.py)

Performance of the example data will be updated soon.