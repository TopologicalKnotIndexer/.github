## 拓扑扭结检索器
- 一些与拓扑扭结检索相关的项目汇集于此。我们旨在实现对小于等于 11-crossing 的扭结的区分。
- 由于 repo 有有很多的 submodule，所以 clone 时要注意使用 `--recursive` 参数。

## 一些列表
- 常见扭结的镜像 HOMFLY-PT 多项式
  - https://github.com/TopologicalKnotIndexer/HOMFLY-PT-polynomial-list/blob/main/data/HOMFLY-PT.txt
- 常见扭结的 khovanov 同调
  - https://github.com/TopologicalKnotIndexer/khovanov-homology-list/blob/main/data/khovanov.txt
- 常见扭结的 volume 列表
  - https://github.com/TopologicalKnotIndexer/volume_list/blob/main/src/volume_info_list.txt
- 常见的 non-hyperbolic 扭结名称序列
  - https://github.com/TopologicalKnotIndexer/non_hyperbolic_knot_list/blob/main/data/non_hyperbolic_knot_list.txt

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
