# Loon 訂閱說明

本倉庫託管 Loon 遠端規則集，由 Muse 代理維護，規則永久保留在本倉庫。

## 規則檔

- Muse 規則：`rules/Muse.list`
- 訂閱位址（raw）：https://raw.githubusercontent.com/hyn-cmh/loon-rules1/main/rules/Muse.list

## 方法一：在 Loon 內新增遠端規則（推薦）

1. 打開 Loon → 設定 → 規則 → 遠端規則 → 新增。
2. 標籤填 `Muse`，位址貼上上面的 raw 連結。
3. 策略選擇你要讓 Muse 流量走的策略（例如 `PROXY` 或你自己的策略組名稱）。
4. 儲存後，Loon 會定期自動更新規則，倉庫更新後你的訂閱會同步。

## 方法二：複製一行到 Loon 配置檔

把下面這一行貼到你 Loon 配置檔的 `[Remote Rule]` 段落中（policy 請改成你配置裡實際存在的策略或策略組名稱）：

```
https://raw.githubusercontent.com/hyn-cmh/loon-rules1/main/rules/Muse.list, policy=PROXY, tag=Muse, enabled=true
```

## 注意

- 本倉庫必須保持 Public 公開，Loon 才能在不登入 GitHub 的情況下抓取規則。
- 規則只包含 Muse / Meta AI 相關域名，不含任何私密資訊。
- 若在 Loon 的請求日誌中發現未被命中的 Muse 相關域名，告知 Muse 代理即可更新本倉庫。
