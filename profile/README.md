## 拓扑扭结检索器
- 一些与拓扑扭结检索相关的项目汇集于此。我们旨在实现对小于等于 11-crossing 的扭结的区分。
- 由于 repo 有有很多的 submodule，所以 clone 时要注意使用 `--recursive` 参数。
- 关于 PD Code 的定义请参考：
  - https://katlas.org/wiki/Planar_Diagrams

## 一些开箱即用的 python 包
- 非素链环表示
  - https://pypi.org/project/link-rep/
- 小于等于 10 crossing 素扭结列表以及其组合
  - https://pypi.org/project/prime-link-knot-10/
- K 分图的边组合生成问题
  - https://pypi.org/project/group-diagram-combination/
- 给出链环 pd code 计算所有连通分支
  - https://pypi.org/project/pd-code-components/
- 给一个 list of list，检验他是否是合法的 pd_code （弱合法性）
  - https://pypi.org/project/pd-code-sanity/
- 给定 pd_code 求一个对应的平面布局图
  - https://pypi.org/project/pd-code-to-diagram/
- 给定一个 pd_code 检查他是否是合法的（强合法性）
  - https://pypi.org/project/pd-code-strong-sanity/
- 给定两个链环的 pd_code，求他们的连通和的 pd_code
  - https://pypi.org/project/pd-code-connected-sum/
- 生成所有可能的 composite 链环的序列化表示（使用小于等于 10 crossing 的素扭结与链环）
  - https://pypi.org/project/com-link-gen-10/
- 给定一个 pd_code （link 或者 knot）删除所有 nugatory crossing
  - https://pypi.org/project/pd-code-delete-nugatory/
- 给定一个 pd_code (link 或者 knot) 删除所有能用 r1-move 删除的 crossing
  - https://pypi.org/project/pd-code-de-r1/
- 给定一个 pd_code，对某个特定的连通分支进行定向翻转
  - https://pypi.org/project/pd-code-reverse-component/
- 给定一个扭结或者链环，给出其 pd_code，计算其镜像扭结
  - https://pypi.org/project/pd-code-mirror/

## 一些列表
请注意，这些列表中并没有依据 writhe 的正负性对标准 PD_CODE 进行镜像修正。这一修正在 hybrid_indexer 中得到实现。
- 常见扭结（含非素）的 PD_CODE
  - https://github.com/TopologicalKnotIndexer/com_pd_code_list/blob/main/data/com_pd_code_list.txt
- 小于等于 11 crossing 的素 Link 的 PD_CODE 列表
  - https://github.com/TopologicalKnotIndexer/link_pd_code_list/blob/main/data/pd_code_list.txt
- 常见标准 PD_CODE 的 writhe 列表：
  - https://github.com/TopologicalKnotIndexer/writhe_list/blob/main/data/writhe_list.txt
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
- (网页端) 扭结连通分支计算器：
  - https://ggn-2015.github.io/pd_code_cc_tool/
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
- (纯 C++) 输入扭结或者链环 PD_CODE，输出三维空间表示或者二维布局图
  - https://github.com/TopologicalKnotIndexer/pd_code_to_diagram
- (纯 Python) 对非素扭结或者非素链环进行表示，给出一种序列化的表示方式
  - https://github.com/TopologicalKnotIndexer/LinkRep
