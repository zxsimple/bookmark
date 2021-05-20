### Cerebro
http://www.vldb.org/pvldb/vol13/p2159-nakandala.pdf
https://adalabucsd.github.io/papers/TR_2019_Cerebro.pdf

### Nvidia
https://github.com/NVIDIA/HugeCTR/blob/master/performance.md

### Oneflow
https://github.com/Oneflow-Inc/oneflow-documentation/blob/master/cn/docs/adv_examples/wide_deep.md

### MindSpore
https://www.mindspore.cn/doc/note/en/r1.2/benchmark.html?highlight=benchmarks

** Wide & Deep (data parallel) **

| Network     | Network Type | Dataset | MindSpore Version | Resource                              | Precision | Batch Size | Throughput          | Speedup |
| ----------- | ------------ | ------- | ----------------- | ------------------------------------- | --------- | ---------- | ------------------- | ------- |
| Wide & Deep | Recommend    | Criteo  | 0.6.0-beta        | Ascend: 1 * Ascend 910 CPU: 24 Cores  | Mixed     | 16000      | 796892 samples/sec  | -       |
|             |              |         |                   | Ascend: 8 * Ascend 910 CPU: 192 Cores | Mixed     | 16000*8    | 4872849 samples/sec | `0.76`  |

** Wide & Deep (Host-Device model parallel) **

| Network     | Network Type | Dataset | MindSpore Version | Resource                               | Precision | Batch Size | Throughput         | Speedup |
| ----------- | ------------ | ------- | ----------------- | -------------------------------------- | --------- | ---------- | ------------------ | ------- |
| Wide & Deep | Recommend    | Criteo  | 0.6.0-beta        | Ascend: 1 * Ascend 910 CPU: 24 Cores   | Mixed     | 1000       | 68715 samples/sec  | -       |
|             |              |         |                   | Ascend: 8 * Ascend 910 CPU: 192 Cores  | Mixed     | 8000*8     | 283830 samples/sec | 0.51    |
|             |              |         |                   | Ascend: 16 * Ascend 910 CPU: 384 Cores | Mixed     | 8000*16    | 377848 samples/sec | 0.34    |
|             |              |         |                   | Ascend: 32 * Ascend 910 CPU: 768 Cores | Mixed     | 8000*32    | 433423 samples/sec | 0.20    |
