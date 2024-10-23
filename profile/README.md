## 拓扑扭结检索器
- 一些与拓扑扭结检索相关的项目汇集于此。我们旨在实现对小于等于 11-crossing 的扭结的区分。
- 由于 repo 有有很多的 submodule，所以 clone 时要注意使用 `--recursive` 参数。

## 一些列表
请注意，这些列表中并没有依据 writhe 的正负性对标准 PD_CODE 进行镜像修正。这一修正在 hybrid_indexer 中得到实现。
- 常见扭结（含非素）的 PD_CODE
  - https://github.com/TopologicalKnotIndexer/com_pd_code_list/blob/main/data/com_pd_code_list.txt
- 常见扭结（含非素）的镜像 HOMFLY-PT 多项式
  - https://github.com/TopologicalKnotIndexer/conflict_lab/blob/main/HOMFLY-PT-reg.txt
- 常见扭结（含非素）的 khovanov 同调
  - https://github.com/TopologicalKnotIndexer/conflict_lab/blob/main/khovanov-reg.txt
- 常见扭结（含非素）的 volume 列表
  - https://github.com/TopologicalKnotIndexer/conflict_lab/blob/main/volume_info_list-reg.txt
- 常见的 non-hyperbolic 素扭结名称序列
  - https://github.com/TopologicalKnotIndexer/non_hyperbolic_knot_list/blob/main/data/non_hyperbolic_knot_list.txt

## 一些分析
- khovanov 同调、HOMFLY-PT 多项式以及扭结补空间体积各自对小于等于 11 crossing 扭结的区分能力的比较报告
   - https://github.com/TopologicalKnotIndexer/conflict_lab

## 一些 repo
由于拆分拆得比较细，这里列举几个值得一看的项目：
- (需要 JDK) 基于 khovanov 同调以及 HOMFLYPT 多项式，输入分子信息文件，推测扭结名
  - https://github.com/TopologicalKnotIndexer/hybrid_knot_indexer
- (需要 JDK) 基于 khovanov 同调，输入 PD_CODE，推测扭结名
  - https://github.com/TopologicalKnotIndexer/khovanov-indexer
- (需要 JDK) 基于 khovanov 同调，输入分子信息文件，推测扭结名
  - https://github.com/TopologicalKnotIndexer/khovanov-indexer-pipeline
- (需要 sage) 基于 HOMFLY-PT 多项式，输入 PD_CODE，推测扭结名
  - https://github.com/TopologicalKnotIndexer/HOMFLY-PT-indexer
- (需要 snappy) 基于 non hyperbolic-knot 的补空间体积，输入 PD_CODE，推测扭结名
  - https://github.com/TopologicalKnotIndexer/volume_indexer
