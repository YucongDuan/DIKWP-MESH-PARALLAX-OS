# DIKWP-MESH PARALLAX OS 交付说明

## 1. 系统定位

PARALLAX不是再增加一个主题仓库，而是为段玉聪当前GitHub生态补上一层“科学判别平面”：把仓库编译为PCMER理论基因组，区分重复、互补、依赖、范围张力与欠决定，发现Residual交叉形成的未知未知，并优先生成能够区分竞争解释的判别实验。

核心命题：**真正稀缺的不是下一个仓库名称，而是最可能改变现有信念排序的下一项观测。**

## 2. 当前冻结快照

- GitHub公开页面实时显示：220个source repositories。
- 本交付逐名闭合：218项。
- 未能逐名恢复的差额：2项，明确保留为Residual，不通过猜测补齐。
- 参考运行：218个理论基因组、519条候选主张、603条理论关系边、20个未知未知热点、24份判别实验合同、4项启发式最小生成基、16项跨域重组候选。
- Mesh 4.0闭包：0.92243，`S4-stable-candidate`。

## 3. 五分钟运行

```bash
unzip DIKWP-MESH-PARALLAX-OS_Source_0.1.0-alpha.zip
cd DIKWP-MESH-PARALLAX-OS

python -m venv .venv
. .venv/bin/activate
python -m pip install -e .

python -m dikwp_parallax.cli demo \
  --data data \
  --output artifacts/demo

python -m dikwp_parallax.cli verify \
  --artifacts artifacts/demo

python -m unittest discover -s tests -t . -v
```

核心运行没有强制第三方依赖，不联网，不调用外部模型API，也不自动修改GitHub仓库。

## 4. 主要命令

```bash
# 打印参考指标
python -m dikwp_parallax.cli metrics --artifacts artifacts/demo

# 检索理论基因组
python -m dikwp_parallax.cli inspect CREDENCE --artifacts artifacts/demo

# 检索判别实验
python -m dikwp_parallax.cli experiments --query schema --artifacts artifacts/demo

# 记录观测回执并更新两个竞争假设的后验
python -m dikwp_parallax.cli record <experiment_id> <outcome> \
  --independent \
  --measurements '{"metric": 0.73}' \
  --artifacts artifacts/demo
```

可选只读API：

```bash
python -m pip install -e '.[api]'
python -m dikwp_parallax.cli serve --artifacts artifacts/demo
```

只读端点包括 `/v1/health`、`/v1/metrics`、`/v1/theories`、`/v1/experiments`、`/v1/hotspots` 与 `/v1/closure`。参考冒烟测试确认GET返回200、写入型POST返回405。

## 5. 协议对象

- `RSX/1.0` Repository Snapshot
- `TGX/1.0` Theory Genome
- `THX/1.0` Theory Hypergraph
- `UUX/1.0` Unknown-Unknown Hotspot
- `DEX/1.0` Discriminating Experiment Contract
- `ORX/1.0` Observation Receipt
- `M4X/1.0` Mesh 4.0 Closure
- `RMX/1.0` Release Manifest

协议包包含8类JSON Schema及代表性示例。

## 6. Mesh 4.0 SemanticClosure

每轮编译检查：Three-No预检、Purpose冻结、锚点与来源、单位与范围、反向追溯、Residual诚实性、Kill条件、Recovery证据和哈希发布。系统不按30/60/90日自动升级，而采用证据门。

## 7. 证据门

- G1：本次可运行参考实现。
- G2：两个无实现依赖团队从干净归档复现。
- G3：对全部公开仓库进行源级README、代码、测试和Release抽取。
- G4：判别实验在低风险合成/离线条件下得到稳定结果。
- G5：真实领域数据、具名责任人、伦理与安全审查、独立复现。
- G6：与CREDENCE、RealityLoop、NEXUS-FORGE和RUNTIME形成双向运行接口。
- G7：多维护者协议治理与公开失败案例库。

任一硬门失败，不因时间经过而自动升级。

## 8. 交付边界

本系统没有宣称：218个项目都代表相互独立的科学理论；603条关系都是已证实冲突；24项实验已经在真实领域实施；启发式最小生成基可以据此删除其他仓库；项目得到段玉聪本人、政府部门、GitHub或科研机构正式批准。所有关系与优先级均是可审查、可替换的参考计算。
