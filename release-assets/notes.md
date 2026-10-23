**A7C II Tools 3.0.3 — 重要修复版 / important fixes**

> [!IMPORTANT]
> **本版本修复了几个重要问题，建议所有人更新。**
> **This release fixes several important bugs. Everyone should update.**

[中文说明](https://github.com/QAQLeonard/a7c2-fl23-research/blob/main/README.zh-CN.md) · [English guide](https://github.com/QAQLeonard/a7c2-fl23-research/blob/main/README.md)

## 修复的问题 / Fixed

- **自定义外观的基础外观不同步**：写入外观、恢复槽位为 ST、一键安装和一键恢复原厂时，会同时同步相机运行中的基础外观和已保存的 ST 设置，不再出现“保存的是 ST、实际运行的是黑白等旧基础外观”。 / **Custom look base out of sync**: LUT writes, slot resets, one-click install and factory restore now sync the running base look with the saved ST setting, so a slot no longer runs on an old base (such as B&W) while ST is saved.
- **机械快门也会响自定义快门声**：现在只有电子快门拍摄时才播放自定义声音；机械快门和电子前帘走原生静音路径。旧版声音补丁会在重新开启或保存时自动升级。 / **Mechanical shutter also played the custom sound**: the custom sound now plays only for electronic-shutter captures; mechanical and EFC captures stay silent. Older sound patches upgrade automatically when you enable or save again.
- **USB 读取出错（“Wrong senser sequence”）**：修正 USB 收包方式，不再在读取过程中吞掉或错读数据。只读操作出错后会自动让相机退出服务模式，通常不必再取电池；日志会写出出错时正在读取的文件。 / **USB read errors ("Wrong senser sequence")**: fixed how USB replies are received; after a read-only failure the app returns the camera from service mode, usually without a battery pull, and logs the file being read.
- **声音操作被旧任务记录拦下**：保存、试听、开启、关闭、恢复原厂音效和核对都不再被之前未完成的任务拦截；保存和试听按当前选择的音频覆盖。 / **Sound actions blocked by old task records**: Save, Audition, On, Off, Restore original sound and Verify are no longer blocked by earlier unfinished tasks; Save and Audition replace the sound with your current selection.
- **Mac 声音保存崩溃**：保存声音时不再运行会在部分 Mac 上崩溃的仿真组件。 / **Mac crash when saving sound**: saving no longer runs the emulator that crashed on some Macs.
- **安装中断后续接**：程序已写完、只差设置的安装可以直接续接设置；旧备份核对按钮误点时会引导到正确的核对。 / Installs interrupted after the programs were written resume at the settings step; the old-backup verify button now redirects a mistaken click.
- 一键恢复原厂写入完成后，旧的声音记录随即停用；声音诊断包附带工作区摘要，问题更好排查。 / After factory restore writes, old sound records are retired; sound diagnostics include a workspace summary.

## 下载 / Downloads

| 文件 / File | 说明 / Description |
| --- | --- |
| `A7C2Tools-Windows-x64.zip` | Windows 10/11 x64。整包解压后运行 `A7C2Tools.exe`。 / Extract everything and run `A7C2Tools.exe`. |
| `A7C2Tools-macOS-arm64.dmg` | macOS 14+ Apple Silicon。未签名，首次需在“隐私与安全性”中允许。 / Unsigned; allow once in Privacy & Security. |
| `A7C2-Looks-and-DCP-3.0.3.zip` | 创意外观与 DCP，与 3.0.0 内容相同。 / Looks and DCPs, same content as 3.0.0. |

更新方法：关闭旧版，解压／安装新版即可；相机里已安装的内容和电脑上的任务记录都会保留。用过电子快门声的，建议更新后在“电子快门声音”页重新点一次“保存当前自定义声音”，让机械快门不再发声。 / To update, close the old version and extract/install the new one; camera contents and task records are kept. If you use the shutter sound, click Save on the shutter sound page once after updating so mechanical captures stay silent.

## 已知问题 / Known issues

- 竖屏创意外观选择页外框仍偏粗；橙色刻度指针朝向尚未修正。 / Portrait Creative Look selection border is still thick; the orange gauge pointer orientation is not yet corrected.

完整更新记录 / Full changelog: [docs/zh-CN/changelog.md](https://github.com/QAQLeonard/a7c2-fl23-research/blob/main/docs/zh-CN/changelog.md) · [docs/en/changelog.md](https://github.com/QAQLeonard/a7c2-fl23-research/blob/main/docs/en/changelog.md)
