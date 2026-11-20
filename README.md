# Open-source church website CMS

A multilingual church website your staff can update without a developer: sermons, events, bulletins, articles, prayer requests, and a block page builder.

This repository is the **Website** edition of [Church4Christ](https://github.com/leveo/church4christ), an open-source
church management system and website. It contains no separate code: the quick start below
installs Church4Christ v1.7.0 with only the Website features switched on (Bulletins, Sermons, Prayer Sheets, Prayer Wall, Events, Articles, Fellowships, Page Builder).
Everything else stays off until you turn it on.

**[Try the live demo](https://demo.church4christ.org/en/sandbox)** · [Main repository](https://github.com/leveo/church4christ) · [Setup guide](https://github.com/leveo/church4christ/blob/v1.7.0/docs/setup.md)

## What you get

- **Sermon archive** with search, speakers, and series.
- **Events and announcements** on a public calendar.
- **Weekly bulletins** built and published from the admin area.
- **Bilingual articles** and printable **prayer sheets**.
- **Prayer wall.** Visitors send prayer requests; staff receive and care for them in the admin area.
- **Fellowship directory.**
- **Block page builder** for custom pages, with images stored in Cloudflare R2.
- **12 interface languages**, including English and Simplified Chinese; each church turns on the ones it needs, and readers can switch Chinese text to Traditional with one tap.
- **Three themes with light and dark modes,** all from design tokens, so your colors stay consistent.
- **Staff sign in by magic link,** with no passwords to manage.

## Screenshots

![The English home page](https://raw.githubusercontent.com/leveo/church4christ/v1.7.0/docs/images/public/home-en.png)

![The public sermon archive](https://raw.githubusercontent.com/leveo/church4christ/v1.7.0/docs/images/public/sermons.png)

![The block page builder](https://raw.githubusercontent.com/leveo/church4christ/v1.7.0/docs/images/admin/page-builder.png)

![The public events calendar](https://raw.githubusercontent.com/leveo/church4christ/v1.7.0/docs/images/public/events.png)

## Try the live demo

Open the [public sandbox](https://demo.church4christ.org/en/sandbox). Choose **Visit the church website** to browse the public pages, or choose **Content editor** to try updating content. All data is fictional and resets every night.

## Quick start

You need [Git](https://git-scm.com/) and [Node.js](https://nodejs.org/) 22.22.1 or newer.
These commands work in macOS and Linux terminals and in Windows PowerShell.

```bash
git clone --depth 1 --branch v1.7.0 https://github.com/leveo/church4christ.git my-church
cd my-church
npm ci
npm run onboard -- --preset website
```

`npm run onboard` opens a local form in your browser for your church's name, colors, logo,
and first administrator, with the Website features already checked. Save the form, press
Ctrl+C in the terminal, then apply it and start the site:

```bash
node scripts/setup/index.mjs --preferences .church/preferences.json --yes --dry-run
node scripts/setup/index.mjs --preferences .church/preferences.json --yes
npm run dev
```

Prefer the terminal only? Run `npm run setup -- --mode local --preset website`
instead of the form and answer the prompts.

Open the address the installer prints (usually `http://localhost:4321`). On your own
computer, sign-in links print to the terminal instead of being emailed.

## Good to know

- Production email (sign-in links, prayer request notices) needs an email provider; see the main repo's cost notes before deploying.
- This edition starts with website features only. Membership, volunteers, groups, and check-in are part of Church4Christ too and can be turned on later in **Settings → Modules**.

## Grow into the full system

This is the complete Church4Christ codebase with a focused starting point. When you are
ready, an administrator can turn on more features (sermons, events, volunteers, groups,
check-in, and more) in **Settings → Modules**, without reinstalling. Upgrades follow the
main repository's [upgrade guide](https://github.com/leveo/church4christ/blob/v1.7.0/docs/upgrade.md).

## Learn more

- [Public site and themes](https://github.com/leveo/church4christ/blob/v1.7.0/docs/features/public-site-and-themes.md)
- [Sermons](https://github.com/leveo/church4christ/blob/v1.7.0/docs/features/sermons.md)
- [Bulletins](https://github.com/leveo/church4christ/blob/v1.7.0/docs/features/bulletins.md)
- [Page builder](https://github.com/leveo/church4christ/blob/v1.7.0/docs/features/page-builder.md)
- [Prayer wall](https://github.com/leveo/church4christ/blob/v1.7.0/docs/features/prayer-wall.md)
- [Putting it online with Cloudflare](https://github.com/leveo/church4christ/blob/v1.7.0/docs/setup.md)

## 中文简介

### 开源教会网站内容管理系统

同工不用写代码就能更新的多语言教会网站：讲道、活动、周报、文章、祷告事项和区块页面编辑器。

- 可搜索的讲道资料库，活动日历与公告。
- 每周周报、双语文章、祷告单。
- 祷告墙：访客提交代祷事项，同工在后台跟进。
- 区块页面编辑器，自由建立页面。
- 12 种界面语言，中文可一键切换繁体；三套主题，支持深色模式。
- 同工用邮件链接登录，无需密码。

本仓库是 [Church4Christ](https://github.com/leveo/church4christ) 的单一功能版本，不包含另外的代码。按上面的快速开始安装后，
得到的是完整的 Church4Christ v1.7.0，只预先开启了这一组功能；以后可以在「设置 → 模块」里开启更多功能。

## Questions and issues

Please open issues and questions in the [main repository](https://github.com/leveo/church4christ/issues), where all the code
lives. Report security problems privately through its
[security advisories](https://github.com/leveo/church4christ/security/advisories/new).

## License

[GNU GPL v3](LICENSE), the same license as Church4Christ.
