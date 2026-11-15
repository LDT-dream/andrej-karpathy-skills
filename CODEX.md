# Codex 外置能力接入

本仓库是 `multica-ai/andrej-karpathy-skills` 的个人 Fork。技能正文唯一维护在 [skills/karpathy-guidelines/SKILL.md](skills/karpathy-guidelines/SKILL.md)；各运行端引用同一文件，不再复制一份正文到 AGENTS.md。

## AGENTS.md 引用

将以下内容并入运行端实际加载的全局或项目 AGENTS.md：

> 编写、审查或重构代码前，读取并遵循 `LDT-dream/andrej-karpathy-skills` 仓库 `main` 分支的 `skills/karpathy-guidelines/SKILL.md`：澄清影响实现的假设，简单优先，只改当前任务所需内容，以明确的验收标准完成工作。小改动按实际需要执行，不额外增加流程。当前用户的授权、安全、测试和停止规则优先。

## 本地

克隆本仓库，将当前 Codex 配置目录下的 `skills/karpathy-guidelines` 映射到工作树的 `skills/karpathy-guidelines`。Windows 可使用目录联接，其他系统使用其支持的目录链接。映射前检查现有入口，不覆盖已有目录。

本地更新通过 Git 拉取；映射读取的是当前检出的文件，不会自动跟随远端更新。

## 远端

支持安装技能的环境，可克隆或安装本仓库中的技能目录；支持读取 GitHub 的环境，可按上述仓库、分支和完整路径直接读取技能正文。

只有链接不会自动加载正文：运行端必须实际读取文件，并配置其支持的指令入口。没有 GitHub 读取能力时，需要在该环境提供仓库或安装技能，不能声称引用已经生效。

## 维护与验证边界

本仓库维护技能及公共接入说明；私人规则和设备目录保留在各端配置中。Fork 保留 `upstream` 作为上游来源，按需审阅上游变更后同步。

2026-11-16：已核验 Windows 本地 Codex 的目录映射与正文读取，并核对 Fork 远端正文和本地一致。远端运行端接入方式已说明，尚未验证特定远端环境的实际加载。
