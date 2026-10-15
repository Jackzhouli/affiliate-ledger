# Affiliate Ledger 部署记录

## 站点信息

| 项 | 值 |
|----|-----|
| 品牌 | Affiliate Ledger |
| 用途 | Google Ads API 申请说明壳站（无登录、无真实 API） |
| 参考 | https://buxiban.org/（结构/菜单/排版复刻；配色改为蓝灰青绿） |
| 本地路径 | `website/affiliate-ledger/` |
| 正式域名 | `https://tracker.opportunitiessite.com` |
| 仓库 | https://github.com/Jackzhouli/affiliate-ledger |
| 托管 | GitHub + Vercel Hobby |
| Vercel 预览 | https://affiliate-ledger-delta.vercel.app |
| Vercel CNAME 目标 | `7707e645b613a886.vercel-dns-017.com` |

## 页面路由

- `/` — About / How It Works / Privacy & Terms 卡片
- `/guide/privacy-policy/`
- `/guide/terms-and-conditions/`

## 部署步骤

1. GitHub 新建空仓库 `affiliate-ledger`（不要 README）
2. 推送：

```bash
cd "/Users/jack_zhou/workspace/media buy/website/affiliate-ledger"
git remote add origin git@github.com:Jackzhouli/affiliate-ledger.git
git push -u origin main
```

3. Vercel → Import 该仓库 → Framework: Other / 静态 → Deploy  
4. Domains 添加 `tracker.opportunitiessite.com`，复制 CNAME 目标  
5. Cloudflare DNS：`tracker` CNAME → Vercel 目标，**仅 DNS**  
6. 验收：`https://tracker.opportunitiessite.com` 与 Privacy / Terms 链接

## 申请 Google Ads API 时填写

- Website / company URL: `https://tracker.opportunitiessite.com`
- Privacy Policy URL: `https://tracker.opportunitiessite.com/guide/privacy-policy/`
- 联系邮箱（站内）：`contact@opportunitiessite.com`（可按需修改）
