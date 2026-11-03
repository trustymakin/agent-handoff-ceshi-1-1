# 产品裁 · A17 G3 定向补测（本地机）· tip `6c6b0b0` · 2026-11-03 Asia/Shanghai

| 项 | 内容 |
|---|---|
| 角色 | 产品核验整理；**未改码／未派 Codex／未重测** |
| 授权 | 改令占本地 `DESKTOP-OQUR45J`；钉 `phase1-pc-wave7-a17-g3-targeted-retest-auth-local-desktop-6c6b0b0-20261103.md` SHA `42feab5b…5f6b` |
| Tip／BIND | tip `6c6b0b0` FULL `6c6b0b07…bc65`／exe `7B6B6B1B…DB2E` size **272384** · **BIND_MATCH=True** · mock／HOTSEAT |
| 正式卷宗 | `phase1-pc-wave7-a17-g3-targeted-local-6c6b0b0-win-verify.md` · SHA256 **`B8A6212361B5C2BBA9646EAA574D329910CFCD76975EE507ED9FA6D4AF6F0B64`**（本机核 ✓） |
| pocket-order | SHA **`29E1EEBE62D8916693AF937DD3F9835C9CC3139F97AE0B039054068D8AEB6616`** ✓ |
| primary mp4 | SHA **`1896E52AFC019ACB89FA11B614A6919B1B769AE1DE2A17C9C76191D280508367`** size 11795838 ✓ |
| evidence zip | SHA **`092A335BF73545C792A6DB268D76D0ACDB22EB4220EBB94628BF93A14DFA15BF`** ✓ |
| 机 | `DESKTOP-OQUR45J`／`a8697f40-…`（用户改令授权占用） |

## 产品结论

**G3 定向补测＝FAIL（同局覆盖仍不足）。≠ PASS。≠ 授权改码。**

| 项 | 裁 |
|---|---|
| 同局互异目标球 | **max＝2**（`#5`→`#2`）；最终 `eventBalls=[5,2]`；门槛 ≥3 **未达** |
| rematch／清槽凑数 | **未用**（`rounds=1`／`ALLOW_REMATCH=False`）——合规 |
| inject／预置／强制入袋 | **未用**——合规 |
| 墙钟入袋 | 19:29:10 #5；20:00:24 #2；20:19:28 cue_scratch（Asia/Shanghai）；shots=70／约 72 分钟同局 |
| G1／G2／G4／G5 | **保留**本批结果（本轮未重测） |
| A17 | **继续未关** |
| G-ROLL | **保持关** |
| 改码／升头／合 main | **未授权／未发生** |

### 实现缺陷 vs 覆盖不足

本轮在**诚实同局长猎**（禁 rematch、禁 inject、70 杆）下仍未凑满 ≥3 颗不同目标球入槽，**多球槽展示／覆盖写／换手后状态仍未观察到**。  
维持 RCA 主判方向：**② 场景／覆盖未达** 为主；**① 实现缺陷（槽展示漏／错）尚未被本轮证伪或坐实**——因门槛场景未触发。  
**≠** 已证明收球槽代码坏；**≠** 可关 G3。

### 证据完整度（DOC）

- pocket-order／BIND／帧（after-1／after-2／ge3-fail）／zip：**齐**  
- 连续录屏：primary `-t 1200` 未覆盖两笔入袋墙钟；另有 cont2／cont3 **同局分段连续**、**未拼单卷**——产品记 **DOC-SOFT**（单文件无缝全窗未交），**不**因此翻成 PASS，也**不**单独作废 FAIL 结论（入袋有帧＋日志＋order 表）

## 禁项钉

不派修复／不改码／不升头／不合 main／不接真服／不黑八胜／不换皮；G-ROLL 关；PC 本项停手。

## 请用户择下一步（经 PM）

1. **维持 G3 FAIL／A17 开**：接受覆盖未达记录，另排或挂起  
2. **再授权一轮同局长猎**（仍不改码；可加长／人工助打说明）  
3. **开改码闸**（须另明确授权 → 再经 Codex工具人＋本机 CLI sol·Ultra）——仅当认定要修实现或加测辅助  

**≠ 自派 Codex；等用户定。**
