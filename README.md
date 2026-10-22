# APA Skill 源 / APA Skill source

本仓库是 APA Skill 源。所有修改均使用已配置的发布分支。

This repository is an APA Skill source. Use the configured publication branch for all changes.

## 仓库格式 / Repository format

`skill-source.json` 声明源格式。每个 Skill 放在 `skills/<name>/` 中，包含自己的 `SKILL.md`、脚本和资源。目录名必须与 Skill 名称一致。

`skill-source.json` declares the source format. Each Skill belongs in `skills/<name>/`, with its own `SKILL.md`, scripts, and resources. The directory name must match the Skill name.

## Skill 版本 / Skill version

在 `SKILL.md` 的 frontmatter 中通过 `metadata.version` 填写发布版本，使用 `major.minor.patch` 格式，例如 `"1.0.0"`。包内任何内容变化（包括描述和元数据）都需要提高版本号。更新版本必须高于发布分支中该 Skill 的当前版本。

Write the published version in the `metadata.version` field of the `SKILL.md` frontmatter, using `major.minor.patch`, for example `"1.0.0"`. Increase the version for any package change, including descriptions and metadata. Updates must be newer than the current version of that Skill on the publication branch.

## 依赖要求 / Dependencies

在 `compatibility` 中注明环境要求。在 Skill 正文或 `references/` 文档中说明依赖的其他 Skill、软件包、命令行工具及登录要求。APA 不会自动安装这些依赖。

Document environment requirements in `compatibility`. Explain other Skills, packages, command-line tools, and login requirements in the Skill body or its `references/` documents. APA does not install these dependencies automatically.

## 维护方式 / Maintenance

使用 APA AI 的发布和删除操作，或通过普通 Git 命令将修改提交并推送到发布分支。读取和安装要求支持匿名 HTTP(S) 访问；写入需要仓库及分支权限。不要将密码和访问令牌放入此仓库。

Use the APA AI publish and delete actions, or ordinary Git commands to commit and push changes to the publication branch. Reading and installation require anonymous HTTP(S) access; writing requires repository and branch permission. Keep passwords and access tokens out of this repository.
