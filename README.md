[![logo](./website/public/aholo-logo.svg)](https://aholojs.dev/)

# Aholo Viewer

Monorepo for the Aholo Viewer package and its documentation website.

## What is Aholo Viewer

Aholo Viewer is a high performance Renderer for 3DGS and Mesh. It uses `Chunked Steaming Lod` schema to handle huge 3DGS.

## Usage

Follow the [Manual](https://aholojs.dev/en-US/manual/getting-started/).

If everything goes well you will see [this](https://jsfiddle.net/q93yx8sr/2/)

## Build Requirements

- Node: >= 22.22.1
- pnpm(corepack preferred)

## Clone this repository

This repository has some submodule as it's dependencies, use following command to clone the repository.

```bash
git clone --recurse-submodules https://github.com/manycoretech/aholo-viewer.git
```

## Structure

```text
aholo-viewer/
  AGENTS.md             Agent-facing project guide
  website/              Astro website: home, manual, examples, API docs, playground
  packages/renderer/    Renderer TypeScript source package
  scripts/              Shared build and documentation scripts
  docs/                 Architecture and AI collaboration notes
  external/             Required upstream and workspace dependency sources
  .codex/skills/        Project-local Codex skills
```
<div align="center">
注册一键对接
【aiyiwei.vip】开发者和AI爱好者调用中转：100ms响应，1元开票，30+工具零改造
<p>claude code推荐特价 Claude Code分组。 gpt推荐codex专属分组和纯az分组。gemini使用gemini-cli分组 新增claude code4.7</p>
<p>限时特价分组，1毛到2毛每百万token gpt-5-nano-2025-08-07 专属养虾</p>
<p>看过来 👉https://aiyiwei.vip/register?aff=9RDC（尾部带个人邀请码，介意可删除尾部字母）</p>
<p>-官网 1-2折，534个全球模型统一管控。</p>
<p>-0.5元到0.7元人民币每刀</p>
<p>-最低1元起充，按需使用无现金流压力</p>
<p>-💼 财务合规无忧</p>
<p>-每笔充值均可开电子发票，最低 1元 起开</p>
<p>-注册就送 $0.2，每天签到领 $0.2-$1</p>
<p>-告别代充灰色渠道，审计直接过	</p>
<p>-🛠️ 30+企业工具一键接入，现有系统零改造</p>
<p>-Claude Code/Cline/Cursor企业部署 → 文档已备</p>
<p>常用龙虾文档:https://vuc9cuve6c.apifox.cn/doc-8779250</p>
<p>-Claude Code → https://vuc9cuve6c.apifox.cn/doc-8779254</p>
<p>-Codex→ https://vuc9cuve6c.apifox.cn/doc-8779249</p>
<p>-Cline → https://vuc9cuve6c.apifox.cn/doc-8779261</p>
<p>-等30多个代码和开发工具适配文档已备齐</p>
<p>-一个接口自动适配，标准OpenAI格式，现有代码改个base_url直接跑，1小时完成接入</p>
<p>-5分钟配通工具，满意再规模化——让AI基础设施像水电一样即开即用</p>
<p>-推广有邀请奖励：推广奖励支持支付宝提现</p>

</div>
<p>QQ用户公告群2：642105456(推荐) QQ用户公告群1：642105456   QQ用户公告群3：247037992</p>

## Commands

Run workspace commands from the repository root:

```bash
pnpm install
pnpm dev
pnpm check
pnpm build
pnpm preview
```

Targeted root commands:

```bash
pnpm build:renderer
pnpm build:website
pnpm check:content
pnpm check:renderer
pnpm check:website
pnpm docs:api
```

## Project Docs

- `AGENTS.md`: quick guide for AI agents and future coding sessions
- `docs/architecture.md`: current workspace structure and dependency flow
- `docs/ai/vibe-coding-guide.md`: detailed guide for future AI-assisted changes, writing style, and handoffs
- `.codex/skills/`: local Codex skills split by repo area

## Codex Skills

Project-local skills live in `.codex/skills/`. Use `AGENTS.md` for the current skill map.

## External Source

`external/egs-core` is a required upstream submodule. `external/splat-transform` is a required workspace package and must stay in the repo. Treat upstream code under `external/` as read-only unless a task explicitly targets that package.

## API Docs

API docs are generated from `packages/renderer/src/index.ts` into an ignored local directory:

```text
website/.generated/api/
```

`pnpm dev`, `pnpm build`, and `pnpm check` regenerate them automatically. Run the generator directly when you want to refresh the local TypeDoc HTML and manifest without starting the site:

```bash
pnpm docs:api
```

## Content Checks

`pnpm check:content` validates manual locale parity, empty pages, example source pairs, manual image references, orphan manual images, and internal-only documentation links. It is also part of `pnpm check` and `pnpm check:website`.

## Playground URLs

The Playground keeps edited code in the URL with `lz-string`:

```text
/zh-CN/playground/?example=basic-scene&code=<compressed-source>
```

Opening a URL with `code` restores the editor content automatically.

Examples are stored in `website/src/content/examples/` as paired `<slug>.json` metadata and `<slug>.ts` source files. The same slug powers the Examples pages and Playground `example` query parameter.

## Contributors

<a href="https://github.com/manycoretech/aholo-viewer/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=manycoretech/aholo-viewer" />
</a>

Made with [contrib.rocks](https://contrib.rocks).

## Useful Links

- [Discussions](https://github.com/manycoretech/aholo-viewer/discussions)
- [Official website](https://aholojs.dev/)
- [CHANGELOG](./packages//CHANGELOG.md)
