# A17 · B mock 延钟 **隔离核验**授权钉 · tip `37b7aef` · 2026-11-04 Asia/Shanghai

> **状态｜OPEN／产品出令＝开闸** · 2026-11-04 Asia/Shanghai  
> **本令＝隔离核验**（编译／BIND／开 mock 钟显示 120 且超时同源／HOTSEAT=0）。**本令不重跑 H／不空清席／不叫人打。**

| 项 | 内容 |
|---|---|
| 来源 | PM 硬派 B 后「补丁交后立刻出隔离核验令」；写码 auth SHA **`9de86e16b7c976c90ac40f2a5eeb283dae9b13f42d91d44792335c1c83cb5311`**／handoff **`5b187e3`**；Codex 交付 handoff SHA **`bcce36ebc6536153730e728af2875a1d465fe4492a85cd04128af6cbbf08bcf5`**／docs **`9501ddd`** |
| tip／分支 | 父 `6c6b0b0` → 新 tip **`37b7aef`** FULL `37b7aefd25ec67e289097a801e95289b02a39eee`；分支 `codex/mock-shot-clock-120-6c6b0b0`；**未合 main／未升默认 tip** |
| 测机 | `DESKTOP-OQUR45J`／`a8697f40-d1d2-4f9b-a183-5f06c4944b2b` |
| 执行 | **客户端PC**；只核验；**禁改码**（本令不派写码） |
| 环境 | PowerShell 同进程启客户端：`FINDTEAMMATES_API_MODE=mock`；`FINDTEAMMATES_BILLIARDS_HOTSEAT=0`；`FINDTEAMMATES_BILLIARDS_MOCK_SHOT_CLOCK=1` |
| 禁 | **重跑 H**／空清席／叫用户开打／烟测／升头／合 main／真服／黑八胜／换皮；G-ROLL **关**；物理 C **停**；注入宣称 PASS |

## 核验硬序

1. **检出／编译**：tip `37b7aef`（或等价分支头）本地 Release 编译通过；记 exe SHA／size  
2. **BIND**：交 exe SHA／size／tip；与交付候选对照（不匹配 → BLOCKED）  
3. **开关关基线（可选短证）**：未开 `MOCK_SHOT_CLOCK`（或=0）→ 行动钟显示／超时＝**30s** 同源  
4. **开关开**：按上表三环境变量启客户端 → 进入台球对局 UI（**mock／勿人打取证**）→ 行动钟显示 **120** 且倒计时与超时同源（到 0 触发与显示一致）  
5. **HOTSEAT=0**：确认未自动翻「本机代打」充数（短观察即可；**勿空清席循环**）

## 交付清单

1. `…-mock-shot-clock-120-37b7aef-verify.md`：编译结果／exe SHA·size／BIND／关＝30（若做）／开＝120 显示＋超时同源截图或墙钟说明／HOTSEAT=0 观察  
2. 证据帧／短录（可选，够证明钟面即可）＋ SHA  
3. 明文：**未**重跑 H／**未**空清／**未**合 main／**未**升头  
4. 写入 handoff `测试1.1/` 或交产品路径＋SHA；抄产品＋PM

## 产品再裁预告

核验 PASS → 维持 tip 候选 `37b7aef`；再开 H 须 **另令**。核验 FAIL → 维持父 tip `6c6b0b0` 闸，转 PM＋Codex。

## 生效

**本令已生效＝OPEN。** PC 按硬序只做隔离核验；确认前不叫人打／不空清。
