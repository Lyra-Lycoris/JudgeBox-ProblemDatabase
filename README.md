# JudgeBox ProblemDatabase

这个仓库是 [JudgeBox](https://github.com/Lyra-Lycoris/JudgeBox) 的**题库目录**。

- 一道题就是一个 `<id>_<题目名>_.zip` 题包，平铺在本目录下（不进子目录）。
- 题包内 `problem.json` 记录题目元数据：title / difficulty / topic / tags / limits / judgeType / source / statement / samples / groups / modes / function。
- 本仓库只保留目录结构，不提交题包本体（`.gitignore` 忽略了 `*.zip`）；题包通过 JudgeBox 的「导入题包」或 `python tools/problemkit/install.py` 安装到本地。

## 目录约定

```
ProblemDatabase/
  <id>_<题目名>_.zip
```

- `id`：`^[a-z0-9][a-z0-9-]{1,47}$`，全局唯一。
- 题包规范见 JudgeBox 仓库的 `CreateProblemGuide/CreateProblemGuide.md`。
- 批量出题见 JudgeBox 仓库的 `tools/problemkit/`。

## 本地用法

JudgeBox 直接读取 exe 同级的 `ProblemDatabase/`；把题包 zip 拷进来、刷新题单即可。
这个目录本身同时是一个独立 git 仓库（JudgeBox 主仓库已用 `.gitignore` 排除它）。
