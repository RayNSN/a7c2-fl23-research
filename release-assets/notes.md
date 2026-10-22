**A7C II Tools 3.0.4 — 恢复与声音修复 / recovery and sound fixes**

[中文说明](https://github.com/QAQLeonard/a7c2-fl23-research/blob/main/README.zh-CN.md) · [English guide](https://github.com/QAQLeonard/a7c2-fl23-research/blob/main/README.md)

## 修复的问题 / Fixed

- **恢复中途 USB 写入失败**：修正 CP 参数读取后的收包边界，避免随后的参数写入只接收 512 字节。文件和名称读取保留已通过用户测试的收包路径。 / **USB write failure during recovery**: finish direct CP parameter responses before the next parameter write; file/name reads retain the recipient-tested framing.
- **声音操作被旧任务拦下**：保存、试听、开启、关闭、恢复原厂音效、核对及音量操作使用当前选择／机身状态，不再要求旧试听报告或断电证明。 / **Sound actions blocked by old tasks**: Save, Audition, On, Off, Restore, Verify and volume controls use the current selection/body, without old audition reports or reboot-proof prerequisites.
- **恢复原厂音效**：从当前受支持的声音程序字节恢复，保留声音开关、创意外观和机身校准，不再依赖旧安装记录。 / **Restore original sound** plans from current supported sound-code bytes, preserving the switch, looks and calibration without a saved install job.
- 包含 3.0.3 的自定义外观 ST 运行值同步、电子快门专用音效路由、Mac 保存声音崩溃及中断安装续接修复。 / Includes the 3.0.3 fixes for live ST synchronization, electronic-only sound routing, the Mac sound-save crash and interrupted-install continuation.

## 下载 / Downloads

| 文件 / File | 说明 / Description |
| --- | --- |
| `A7C2Tools-Windows-x64.zip` | Windows 10/11 x64。整包解压后运行 `A7C2Tools.exe`。 / Extract everything and run `A7C2Tools.exe`. |
| `A7C2Tools-macOS-arm64.dmg` | macOS 14+ Apple Silicon。未签名，首次需在“隐私与安全性”中允许。 / Unsigned; allow once in Privacy & Security. |
| `A7C2-Looks-and-DCP-3.0.4.zip` | 创意外观与 DCP，与 3.0.0 内容相同；两个应用包也内置全部 15 组彩色 DCP／A7Look 配对。 / Looks and DCPs, unchanged from 3.0.0; both app packages also include all 15 color DCP/A7Look pairs. |

更新方法：关闭旧版，解压／安装新版即可；相机内容和电脑任务记录保留。使用旧版电子快门声音补丁的用户，重新保存一次可更新机械／电子快门路由。 / Close the old version and extract/install the new one; camera contents and task records are kept. Re-save once to upgrade an older shutter-sound routing patch.

## 验证与已知问题 / Validation and known issues

- 作者已在一台机身确认恢复及最新本地测试版可用；序号错位机身已通过 v2 只读测试，新限定版本目前有捕获元数据重放与离线回归证据，尚未在该机身复测。 / The owner accepted recovery and the local test build on one camera. The affected sequence-error camera passed the v2 read-only probe; the scoped revision has metadata replay and offline regression evidence, pending a retest on that body.
- 名称文件报告中的两种尺寸已通过真实 ARM64 worker 的模拟数据测试；没有失败文件内容可供比对，本版不承诺修复既有文件系统损坏。 / The reported resource sizes pass synthetic tests of the actual ARM64 worker; failed-file contents were unavailable, and this version does not claim to repair existing filesystem damage.
- 竖屏创意外观选择页外框仍偏粗；橙色刻度指针朝向尚未修正。 / Portrait Creative Look selection border is still thick; the orange gauge pointer orientation is not yet corrected.
- 云端打包与离线测试不等于 Mac 实机／所有机身测试。 / Cloud packaging and offline tests do not establish physical Mac or all-body camera compatibility.

完整更新记录 / Full changelog: [中文](https://github.com/QAQLeonard/a7c2-fl23-research/blob/main/docs/zh-CN/changelog.md) · [English](https://github.com/QAQLeonard/a7c2-fl23-research/blob/main/docs/en/changelog.md)
