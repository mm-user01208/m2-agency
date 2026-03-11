# M2 Agency サイト移行メモ

## 概要
- **旧環境:** Wix（年3万円、毎年3/17更新）
- **新環境:** GitHub Pages（無料）
- **ドメイン:** お名前.com で管理（m2-agency.net）
- **方針:** noindex の会社紹介サイトなので無料ホスティングで十分

## 移行作業（2026-03-11）

### 1. HTML作成
- Wixサイトの内容をシンプルな静的HTML 1ページに再構築
- CSS内蔵（外部ファイルなし）
- `<meta name="robots" content="noindex, nofollow">` 設定済み
- コンタクトフォームは Formspree プレースホルダー（要設定 or mailto に変更）

### 2. GitHub Pages デプロイ
- リポジトリ: https://github.com/mm-user01208/m2-agency
- GitHub Pages ON（source: main / root）
- CNAME ファイルで `www.m2-agency.net` 設定

### 3. DNS設定（お名前.com）
追加したレコード:
- `www` / CNAME / `mm-user01208.github.io`
- (空) / A / `185.199.108.153`
- (空) / A / `185.199.109.153`
- (空) / A / `185.199.110.153`
- (空) / A / `185.199.111.153`
- 既存の NS, MX レコードはそのまま維持

### 4. 残タスク
- [ ] DNS反映確認
- [ ] HTTPS強制有効化（DNS反映後）
- [ ] Wix解約（3/17前に！）
- [ ] コンタクトフォームの送信先設定（Formspree登録 or mailto化）

## サイト構成
- ナビ: Home / Service / Company / Contact
- Services: ウェブサイト事業、記事制作
- Company: 株式会社M2 Agency / 代表取締役 森實将 / 2023年6月13日設立 / 東京都目黒区中目黒4-8-25
- Contact: フォーム + info@m2-agency.net
