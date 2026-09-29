# Performance Analysis of Virtual Machines and Containers

## Objective

To compare the performance of a Virtual Machine (VM) and a Docker container using CPU, memory, disk, network, and API benchmarks.

## Experimental Environment

- Host OS: Windows
- Hypervisor: VMware Workstation
- Guest OS: Ubuntu 26.04.1 LTS
- VM CPU: 2 vCPUs
- VM Memory: 3.27 GiB
- Docker: 29.1.3
- CPU Benchmark: Sysbench
- Memory Benchmark: Sysbench
- Disk Benchmark: fio
- Network Benchmark: iperf3
- API Benchmark: ApacheBench
- API Framework: FastAPI
- Analysis: Python, Pandas, Matplotlib

## Benchmarks

1. CPU performance
2. Memory performance
3. Sequential disk write performance
4. Network throughput
5. FastAPI request performance

## Results

| Benchmark | Metric | VM | Docker |
|---|---|---:|---:|
| CPU | Events/sec | 1668.10 | 1751.35 |
| Memory | MiB/sec | 23629.16 | 11496.33 |
| Disk | MiB/sec | 449.60 | 553.20 |
| Network | Gbits/sec | 44.0 | 40.5 |
| API | Requests/sec | 3130.57 | 1818.79 |

## Graphs

The comparison graphs are available in the `results/graphs/` directory.

## Result Files

- `results/raw/` contains the raw benchmark outputs.
- `results/processed/` contains processed comparison data.
- `results/graphs/` contains generated performance graphs.

## Conclusion

The experiment demonstrates that VM and container performance varies depending on the workload. The measured results show differences in CPU, memory, disk, network, and API performance. Containers showed higher measured CPU and disk throughput in these tests, while the VM showed higher measured memory, network, and API throughput.

These results are specific to the experimental environment and benchmark configuration used in this project.
