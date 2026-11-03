# GitHub 入门指南：从注册账号到第一次参与项目

写给刚进入 GitHub、打开页面却不知道从哪里开始的你。

你不需要先学会编程，也不需要马上安装软件。这份指南先带你用浏览器完成基本操作，再介绍本地工具和协作流程。

**读完并动手后，你将能够：**

- 看懂一个项目的基本结构，找到说明文档和下载入口。
- 创建自己的仓库，上传文件，修改 README。
- 理解提交、分支、Fork 和 Pull Request。
- 提出一个清楚的问题，或为别人的项目做一次小修改。

> 使用说明：本文面向 GitHub.com 的个人账号，按钮名称以英文为主，并附中文解释。界面会更新，不同设备、权限和项目设置也会影响显示；找不到按钮时，可查看对应章节中的官方文档。
>
> 文档核对日期：2026 年 11 月 3 日。这是一份独立编写的中文教程。

## 阅读路线

| 你现在想做什么 | 从这里开始 |
| --- | --- |
| 先弄清楚 GitHub 是干什么的 | [一、先认识 GitHub](#start) |
| 完善账号、安全和邮箱设置 | [二、注册后先做的事](#account) |
| 找到项目、下载软件或源码 | [三、看懂别人的项目](#explore) |
| 把自己的笔记或项目放上去 | [四、创建第一个仓库](#first-repo) |
| 把项目首页写得清楚一些 | [五、写好 README](#readme) |
| 提问、反馈问题、参与修改 | [六、Issue 和协作](#collaborate) |
| 在电脑上管理和上传修改 | [七、本地工具入门](#local) |
| 了解提交和文件管理的好习惯 | [八、从第一天就养成的习惯](#habits) |
| 操作时遇到报错或困惑 | [九、常见问题](#faq) |
| 想照着练一遍 | [十、入门练习清单](#practice) |
| 查阅更完整的官方教程 | [十一、继续学习](#resources) |

<a id="start"></a>

## 一、先认识 GitHub

### 1. GitHub 能做什么？

GitHub 是一个托管项目、记录修改并开展协作的平台。你可以在这里保存代码，也可以整理学习笔记、编写教程、维护资料清单。

举个例子：你把一份学习笔记放到 GitHub，过几天补充了一章，又改正了一个错误。通过提交记录，你可以查看每次修改的内容；其他人也能提出建议，或者提交修改供你审阅。

### 2. Git 和 GitHub 有什么区别？

| 名称 | 可以怎样理解 |
| --- | --- |
| **Git** | 记录和管理文件版本的工具，可以在自己的电脑上使用 |
| **GitHub** | 托管 Git 仓库，并提供讨论、审阅和协作功能的平台 |
| **GitHub Desktop** | 用图形界面操作 Git、连接 GitHub 的桌面应用 |

**刚入门可以先用 GitHub 网页。** 等你经常修改本地文件，再选择 GitHub Desktop 或命令行。

### 3. 先记住这些词

| 页面上的词 | 中文 | 用一句话理解 |
| --- | --- | --- |
| Repository / Repo | 仓库 | 项目的文件、修改历史和协作信息所在的地方 |
| README | 项目说明 | 通常是进入仓库后首先阅读的介绍文档 |
| Commit | 提交 | 把一组修改记录为一个版本，并附上一句说明 |
| Branch | 分支 | 从某个版本分出去的一条开发路线 |
| main | 常见的默认分支名 | 项目通常把主要内容放在默认分支；名称也可能不同 |
| Issue | 议题 | 用来报告问题、提出建议或跟踪任务 |
| Pull Request / PR | 拉取请求 | 把一组分支修改交给他人审阅，提议合并 |
| Merge | 合并 | 将一个分支的修改并入另一个分支 |
| Fork | 复刻 | 在自己的账号下创建一个与原仓库有关联的仓库 |
| Clone | 克隆 | 把仓库和版本历史取到本地，用 Git 继续管理 |
| Star | 标星 | 收藏项目，也可以表达认可 |
| Watch | 关注通知 | 按所选范围接收仓库动态 |

不用一次背下来，实际用到时回来查就够了。[官方基础练习：Hello World](https://docs.github.com/zh/get-started/using-github/hello-world)。

<a id="account"></a>

## 二、注册后先做的几件事

1. **完成邮箱验证。** 先查看注册邮箱，按 GitHub 的提示完成验证。
2. **补充个人资料。** 在头像菜单的 `Settings`（设置）中填写昵称、简介等信息；只公开你愿意公开的内容。
3. **设置账号保护。** 使用独立密码，配置双重身份验证（2FA），并把恢复代码保存在可靠的位置。具体操作见[配置双重身份验证](https://docs.github.com/zh/authentication/securing-your-account-with-two-factor-authentication-2fa/configuring-two-factor-authentication)。
4. **检查邮箱隐私。** 在 `Settings → Emails` 中查看邮箱可见性和 GitHub 提供的 `noreply` 邮箱。以后配置本地 Git 时，可以使用设置页面给出的完整 `noreply` 地址，减少在提交记录中暴露私人邮箱。[提交邮箱说明](https://docs.github.com/zh/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-email-preferences/setting-your-commit-email-address)。

**用户名和昵称不一定相同。** 仓库地址里的账号部分使用用户名。例如 `https://github.com/octocat/Hello-World` 中，`octocat` 是仓库所有者，`Hello-World` 是仓库名称。

<a id="explore"></a>

## 三、看懂别人的项目：从哪里看，怎么下载？

### 1. 进入仓库后，按这个顺序看

1. **先读 README。** 确认项目用途、适用系统、安装步骤和使用方法。
2. **再看文件列表。** 文件夹用来组织内容，单击文件可以查看支持预览的内容。
3. **需要安装软件时找 Releases。** 看有没有适合自己系统和处理器架构的发布文件。
4. **遇到问题先搜 Issues。** 看是否已有相同问题及解决方法。
5. **准备使用或修改项目时看 LICENSE。** 了解项目采用的许可及相关条件。

常见文件可以这样认：

| 文件或目录 | 常见用途 |
| --- | --- |
| `README.md` | 项目说明，`.md` 表示 Markdown 文档 |
| `LICENSE` / `LICENSE.txt` | 许可证文本 |
| `docs/` | 更详细的文档 |
| `src/` | 源代码 |
| `examples/` | 示例 |
| `CONTRIBUTING.md` | 贡献方式、开发流程和提交要求 |
| `.gitignore` | 告诉 Git 哪些尚未跟踪的文件应被忽略 |

这些是常见约定，每个项目的组织方式可能不同。

### 2. 下载软件和下载源码，入口可能不同

**如果你想直接使用软件：**

1. 先按 README 中的下载说明操作。
2. 如果项目提供 `Releases`（发布版本），进入相应版本，查看 `Assets`（资源）。
3. 选择与你的设备匹配的文件，例如 Windows 安装程序、macOS 安装包，或 Linux 软件包。具体以项目说明为准。

并非每个项目都会提供安装包。发布页中的 `Source code (zip)` 和 `Source code (tar.gz)` 是源码存档，通常需要按项目文档配置环境才能运行。[查看发布版本](https://docs.github.com/zh/repositories/releasing-projects-on-github/viewing-your-repositorys-releases-and-tags)。

**如果你只想下载一份源码或文档：**

在仓库文件列表上方点击 `Code → Download ZIP`，然后解压。下载内容对应当前选中的分支，操作前可以先确认分支名称。

ZIP 是一份快照，不含完整 Git 历史；如果准备长期修改并同步仓库，可以使用 Clone。[下载源代码存档](https://docs.github.com/zh/repositories/working-with-files/using-files/downloading-source-code-archives)。

### 3. 搜索和收藏项目

在 GitHub 顶部搜索框输入关键词，然后选择 `Repositories` 查看仓库。例如：

```text
python tutorial
```

熟悉后可以加入筛选条件：

```text
python tutorial language:Python stars:>100
```

这表示搜索包含相关关键词、主要语言为 Python、Star 数大于 100 的仓库。Star 数只能作为参考，还要结合文档、最近的维护情况和自己的需求判断。[仓库搜索语法](https://docs.github.com/zh/search-github/searching-on-github/searching-for-repositories)。

遇到想以后再看的项目，可以点击 `Star`。需要更新通知时，再根据需要设置 `Watch`。

<a id="first-repo"></a>

## 四、动手：用网页创建第一个仓库

这一章只用浏览器。建议先创建一个练习仓库，放入几句不涉及隐私的文字。

### 第一步：创建仓库

登录后打开[新建仓库页面](https://github.com/new)，也可以从页面右上角的 `+ → New repository` 进入。

按下面的示例填写：

| 选项 | 示例或建议 |
| --- | --- |
| Owner | 选择自己的账号 |
| Repository name | `hello-github` |
| Description | `我的第一个 GitHub 练习仓库` |
| Visibility | 只想自己练习可选 `Private`；想让大家看到可选 `Public` |
| Add README | 开启，生成项目说明文件 |

`Public` 表示公开，任何人都可能看到；`Private` 表示仅允许具有相应访问权限的人查看。公开仓库也不代表别人可以直接修改你的默认分支。

这个文字练习暂时不需要选择 `.gitignore` 模板和许可证。点击 `Create repository` 完成创建。[官方创建教程](https://docs.github.com/zh/get-started/start-your-journey/creating-a-repository-for-your-project-on-github)。

**完成标志：** 浏览器显示你的仓库页面，文件列表里有 `README.md`。

### 第二步：修改 README

1. 点击文件列表中的 `README.md`。
2. 找到铅笔图标或 `Edit this file`（编辑此文件）。
3. 将内容修改为下面的示例。
4. 使用 `Preview`（预览）查看排版。
5. 点击 `Commit changes`（提交更改），填写说明，例如 `补充项目介绍`。
6. 在自己的练习仓库中，选择直接提交到当前分支，再确认提交。

```markdown
# 我的 GitHub 学习记录

这里用来记录我学习 GitHub 的过程。

## 我已经学会

- 创建仓库
- 修改 README
- 保存一次提交

## 下一步

- [ ] 上传一份学习笔记
- [ ] 尝试创建分支
```

**完成标志：** 回到仓库首页，能看到新的介绍和列表。

一次 Commit 可以包含一个或多个文件的修改。提交说明尽量写明做了什么，比如“修正文档中的链接”，方便以后查找。

### 第三步：创建或上传文件

**直接在网页写笔记：** 在仓库的 `Code` 页面找到 `Add file → Create new file`，文件名填写 `notes/day-01.md`，写入内容后提交。文件名中的 `/` 可以用来建立目录层级。

**上传电脑里的文件：** 选择 `Add file → Upload files`，拖入或选取文件，确认内容后填写提交说明，再点击 `Commit changes`。

目前通过浏览器上传时，单个文件上限为 **25 MiB**，一次最多上传 **100 个文件**。普通 Git 仓库阻止超过 **100 MiB** 的单个文件；需要管理大文件时再了解 Git LFS。限制以[官方上传说明](https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository)为准。

### 第四步：查看修改历史

查看文件时，找到 `History`（历史记录），进入某次提交，可以查看它改动了哪些内容。

在文本修改对比中，通常用红色表示删除、绿色表示新增。历史记录的价值就在于：你能追溯“什么时候，改了什么”。

<a id="readme"></a>

## 五、把项目首页写清楚：README 和 Markdown

README 是项目的说明入口。仓库根目录中的 `README.md` 通常会直接展示在仓库首页。

对于第一个项目，先把这几件事说清楚就够了：**它是什么、给谁用、怎么开始、遇到问题去哪里反馈。**

### 常用 Markdown 写法

| 想要的效果 | 写法 |
| --- | --- |
| 一级标题 | `# 标题` |
| 二级标题 | `## 小节标题` |
| 加粗 | `**重点内容**` |
| 无序列表 | `- 一条内容` |
| 链接 | `[显示文字](https://example.com)` |
| 行内代码 | 用一对反引号包住内容，例如：`` `README.md` `` |
| 未完成任务 | `- [ ] 待完成` |
| 已完成任务 | `- [x] 已完成` |

段落之间留一个空行；标题的 `#` 后面要有空格。更完整的语法可以查阅[GitHub Markdown 官方说明](https://docs.github.com/zh/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)。

### 一份可直接修改的 README 模板

把下面的内容复制到你自己项目的 `README.md`，按实际情况替换：

````markdown
# 项目名称

用一两句话说明这个项目能帮助谁、解决什么问题。

## 内容介绍

- 内容或功能一
- 内容或功能二

## 如何开始

1. 说明需要准备什么。
2. 说明从哪里进入、下载或安装。
3. 给出一个最简单的使用示例。

## 使用示例

```text
在这里放示例输入、操作步骤或预期结果。
```

## 问题反馈

请先查看已有 Issues。提出新问题时，请说明操作步骤、预期结果和实际结果。
````

### 想分享项目，还要看许可证

把仓库设为公开，与授予别人使用、修改和分发的许可，是不同的事情。准备发布开源项目时，应了解并选择适合的许可证，在仓库中添加相应的 `LICENSE` 文件；使用别人的内容时，也要检查其许可证条件。[GitHub 许可证说明](https://docs.github.com/zh/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository)。

<a id="collaborate"></a>

## 六、开始交流：Issue、分支和 Pull Request

### 1. 用 Issue 报告问题或提出建议

先阅读 README、贡献指南并搜索已有 Issues。如果没有找到答案，再进入 `Issues → New issue`，按照项目提供的模板填写。有些项目关闭了 Issues，或把提问放在 `Discussions`、论坛等入口，按项目说明操作即可。[创建 Issue](https://docs.github.com/zh/issues/tracking-your-work-with-issues/using-issues/creating-an-issue)。

一个清楚的问题可以这样写：

```markdown
标题：Windows 11 下启动后显示空白窗口

## 环境
- 系统：Windows 11
- 软件版本：填写实际版本

## 复现步骤
1. 从哪个发布版本下载了哪个文件。
2. 如何安装或启动。
3. 执行哪个操作后出现问题。

## 预期结果
我原本希望看到什么。

## 实际结果
实际发生了什么，附上完整报错文本或必要截图。

## 已尝试的方法
列出已经检查过的文档和尝试过的解决方法。
```

发送前检查日志和截图中有没有密码、令牌或私人信息。标题写清楚具体问题，也更方便后来的人搜索。

### 2. 分支和 PR 是怎样配合的？

可以把流程理解为：

```text
从 main 创建分支 → 在分支上修改并提交 → 发起 PR → 审阅和讨论 → 合并回 main
```

分支让一组修改可以先独立进行；PR 则把“准备合并什么、为什么修改”集中展示出来，供协作者审阅。

**先在自己的练习仓库试一次：**

1. 回到 `hello-github` 仓库的 `Code` 页面，打开文件列表上方的分支选择器。
2. 以 `main` 为起点，输入新分支名 `update-readme`，选择创建分支。
3. 确认当前在 `update-readme`，修改 `README.md` 并提交到这个分支。
4. 进入 `Pull requests → New pull request`，设置 `base: main`、`compare: update-readme`。
5. 检查差异，点击 `Create pull request`，写明改动原因。
6. 在自己的练习仓库中确认修改正确后，点击 `Merge pull request` 并确认合并。
7. 返回 `main`，检查改动已经出现。合并后可以删除练习分支。

如果你的默认分支不叫 `main`，请使用实际名称。真实项目可能要求审阅或检查通过后才能合并。[官方分支与 PR 练习](https://docs.github.com/zh/get-started/using-github/hello-world)。

### 3. 想修改别人的项目，通常先 Fork

没有原仓库写入权限时，常见流程是：

1. 阅读原项目的 `CONTRIBUTING.md` 和相关 Issue，确认贡献要求。
2. 点击原仓库右上方的 `Fork`，在自己的账号下创建复刻。
3. 在自己的 Fork 中创建分支，再修改和提交。
4. 向原仓库发起 PR。确认目标是**原仓库的目标分支**，来源是**自己 Fork 中的修改分支**。
5. 根据反馈补充修改，等待维护者决定是否合并。

Fork 后不会自动跟随原项目的所有更新，需要时可以在 Fork 中使用 `Sync fork` 同步。Fork 和 Clone 的详细区别、操作步骤可参考[复刻仓库](https://docs.github.com/zh/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)。

第一次贡献可以从修正错别字、修复链接、补充使用说明开始。寻找任务时，可以关注 `good first issue` 和 `help wanted` 标签；先读任务内容，再决定是否参与。[寻找开源贡献机会](https://docs.github.com/zh/get-started/exploring-projects-on-github/finding-ways-to-contribute-to-open-source-on-github)。

<a id="local"></a>

## 七、选读：在自己的电脑上操作

当你需要经常修改代码或批量管理文件时，再读这一章。下面两种方式选择一种起步即可。

### 方式 A：GitHub Desktop

适合希望先使用图形界面的读者。

1. 从 [GitHub Desktop 官网](https://desktop.github.com/) 下载应用，安装并登录。
2. 使用 `File → Clone repository`，把前面创建的练习仓库克隆到电脑。
3. 用编辑器修改本地 `README.md` 并保存。
4. 回到 Desktop，在 `Changes` 中查看修改差异和待提交文件。
5. 填写提交摘要，点击提交按钮，把修改记录到当前分支。
6. 点击 `Push origin`，将本地提交上传到 GitHub，再打开网页确认。

开始新一轮工作前，可以先 `Fetch origin` 检查远程更新；有更新时按应用提示拉取。完整操作见[GitHub Desktop 入门教程](https://docs.github.com/zh/desktop/overview/creating-your-first-repository-using-github-desktop)。

### 方式 B：Git 命令行

适合准备学习开发流程的读者。先从 [Git 官网](https://git-scm.com/downloads)安装 Git，再在终端执行：

```bash
git --version
```

能显示版本号，说明终端已经能使用 Git。

**首次配置提交身份：** 把下面两项替换成你希望显示的作者名称和自己的提交邮箱。`--global` 表示将其作为当前电脑用户的默认配置。

```bash
git config --global user.name "你的作者名称"
git config --global user.email "你的提交邮箱"
```

作者名称可以与 GitHub 用户名不同。这两项用于提交记录，不会替你登录 GitHub；想保护邮箱隐私，可以从 `Settings → Emails` 复制自己的完整 `noreply` 地址。[提交邮箱设置](https://docs.github.com/zh/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-email-preferences/setting-your-commit-email-address)。

**把已有仓库克隆到本地：** 在仓库网页的 `Code → HTTPS` 复制地址。下面的 `YOUR_USERNAME` 要替换为你的真实用户名。

```bash
git clone https://github.com/YOUR_USERNAME/hello-github.git
cd hello-github
git status
```

在编辑器中修改并保存 `README.md` 后，按顺序执行：

```bash
git diff
git add README.md
git commit -m "补充项目介绍"
git push
```

| 命令 | 作用 |
| --- | --- |
| `git status` | 查看当前分支和文件状态 |
| `git diff` | 查看尚未暂存的修改差异 |
| `git add README.md` | 把这个文件的修改加入暂存区 |
| `git commit -m "说明"` | 将暂存区中的修改记录为本地提交 |
| `git push` | 将本地提交推送到远程仓库 |

上面的命令以你克隆的个人练习仓库、当前分支允许推送为前提。若仓库要求通过 PR 修改，请采用分支流程。

**本地 Commit 以后，还需要 Push，GitHub 网页上才会出现这些提交。** 网页编辑则是在 GitHub 上直接提交，不需要再从电脑推送一次。

**首次推送需要验证身份。** GitHub 的 HTTPS Git 操作已经不支持使用账号登录密码认证。可使用 Git Credential Manager 等凭据工具按提示登录；需要手动填写凭据时，密码位置使用个人访问令牌（PAT），也可以另行配置 SSH。不要把令牌写进仓库地址或提交到文件里。[GitHub 身份验证说明](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/about-authentication-to-github)。

<a id="habits"></a>

## 八、从第一天就养成的习惯

- **提交前查看文件和差异。** 确认上传的是这次要修改的内容，提交说明写清用途。
- **小步提交。** 一次围绕一件事修改，方便自己回顾，也方便别人审阅。
- **上传前检查敏感信息。** 密码、访问令牌、SSH 私钥、带真实密钥的 `.env`、私人证件和未获授权的内部资料，都不应放进仓库。
- **配置忽略规则。** `.gitignore` 可以忽略尚未跟踪的文件，但不会自动删除已提交的内容，更不会清除历史中的秘密。
- **先了解项目约定。** 参与协作前阅读 README 和贡献指南，遇到不确定的需求先在对应议题中讨论。

**如果已经提交了密码或令牌：先撤销或更换它，再处理仓库中的内容和历史。** 仅删除最新版本的文件，历史记录中仍可能保留原内容。清理步骤请参考[从仓库中删除敏感数据](https://docs.github.com/zh/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository)。

<a id="faq"></a>

## 九、常见问题

### 不会编程，也能用 GitHub 吗？

可以。你可以用它管理笔记、教程和资料清单，也可以帮助项目改正文档、反馈问题。

### 别人的仓库没有编辑或上传入口，怎么办？

先确认自己是否有写入权限。希望建议修改时，可以按项目要求 Fork 后发起 PR；只想反馈问题，可以使用项目指定的反馈入口。

### 点了 Star，项目会自动下载或持续通知我吗？

Star 用于收藏和表达认可，不会把文件下载到你的电脑。通知范围由 `Watch` 等通知设置控制。

### 下载 ZIP 后，文件夹里没有能双击启动的程序？

你可能下载了源码。回到 README 查看安装方法，再检查 Releases 是否提供适合你系统的可运行版本。

### 为什么修改后网页上没有变化？

依次检查：文件是否保存、是否 Commit、是否 Push，以及网页当前查看的是不是同一个仓库和分支。网页编辑时，检查是否已在提交对话框中最终确认。

### `git status` 显示 `nothing to commit`？

表示当前没有可提交的修改。确认文件已经保存、终端位于正确的仓库目录，并检查文件是否被忽略或已经提交。

### `git push` 被拒绝怎么办？

先阅读错误信息：

- 认证或权限错误：检查登录账号、令牌权限，以及是否能写入这个仓库。
- 分支受保护：按项目要求创建分支并发起 PR。
- 提示 `non-fast-forward`：远程分支有本地尚未包含的提交。先确保本地工作已妥善保存，再拉取并整合更新；发生冲突时，处理并检查结果后再推送。

不要把强制推送当成通用修复办法。分不清原因时，保留完整错误文本，隐藏敏感信息后再求助。

### 上传时报文件太大怎么办？

先检查是否超过当前上传方式的限制。大文件按项目需要选择 Git LFS 等方式；安装包的分发可以了解 Releases。不要为了上传成功就把不需要版本管理的大文件全部放进仓库。

### 公开仓库就是可以任意复制和使用吗？

使用和分发前先检查项目许可证及相关内容的授权。仓库公开可见，并不等于所有用途都已获得许可。[许可证说明](https://docs.github.com/zh/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository)。

<a id="practice"></a>

## 十、照着做一次：入门练习清单

这份练习可以分几次完成，不必一次学完。

### 第一轮：会看、会找

- [ ] 找到一个自己感兴趣的项目。
- [ ] 读完它的 README，能说出这个项目用来做什么。
- [ ] 分清源码下载入口和可运行版本的下载入口。
- [ ] 给想继续了解的项目点一次 Star。

### 第二轮：拥有自己的仓库

- [ ] 创建 `hello-github`，初始化 README。
- [ ] 修改 README，写一句自己的项目介绍。
- [ ] 新建 `notes/day-01.md`，记录今天学到的内容。
- [ ] 查看一次提交记录，说出它改了什么。

### 第三轮：理解协作

- [ ] 在练习仓库中创建 `update-readme` 分支。
- [ ] 在分支上提交一次修改。
- [ ] 发起并检查自己的 PR，然后合并。
- [ ] 回到默认分支，确认修改已出现。

完成后，你已经走过了 GitHub 的基本使用流程。接下来可以用一个真实的小项目继续练习，例如整理一份读书笔记或课程资料目录。

<a id="resources"></a>

## 十一、继续学习

| 目标 | 官方资源 |
| --- | --- |
| 系统了解 GitHub 基础 | [GitHub 入门路线](https://docs.github.com/zh/get-started/start-your-journey) |
| 再做一遍仓库和 PR 练习 | [Hello World](https://docs.github.com/zh/get-started/using-github/hello-world) |
| 查询排版写法 | [Markdown 基本语法](https://docs.github.com/zh/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) |
| 学习图形界面操作 | [GitHub Desktop 文档](https://docs.github.com/zh/desktop) |
| 寻找适合自己的贡献任务 | [参与开源的方法](https://docs.github.com/zh/get-started/exploring-projects-on-github/finding-ways-to-contribute-to-open-source-on-github) |
| 深入学习 Git | [Pro Git 中文书](https://git-scm.com/book/zh/v2) |

如果你在按本文操作时遇到了不清楚的步骤，欢迎通过本指南所在仓库的 Issues 反馈。请说明对应章节、你进行的操作，以及实际看到的页面或提示，方便一起改进。
