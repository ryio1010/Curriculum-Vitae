# 職務経歴書
職務経歴書になります。

## 個人データ
- ID ryio1010
- Web https://ryio1010.github.io/Curriculum-Vitae/

## スキル
### 言語
- Java
- Kotlin
- Go（実務経験なし）

### フレームワーク
- Spring boot
- Gin（実務経験なし）

### インフラ
- AWS
- Azure
- GCP（実務経験なし）

### その他
- PostgreSQL
- Jenkins
- Docker
- Kubernates
- Github Actions（実務経験なし）

## ストロングポイント
- 問題解決能力が高い
- 自走力がある
- 行動力がある
- 好きなことへの熱中度の高さ

## 今後やりたいこと
- Go言語の習得
- ミドルウェアの理解(apatch/ngix)
- RDBのインデックス、設計
- Kubernatesの深い理解
- フロントエンドの習得

## 職務経歴（概要）
### ソフトウェア開発
- 業務系ソフトウェアの運用保守・追加開発
    - 配送システム運用保守・追加開発　1.5年
- パッケージツール導入・技術支援
    - RPAツール（Blue Prism）の導入・技術支援　0.5年
    - 経営管理ツール（Sactona）の導入・技術支援　0.5年

### プログラミングスキル
- Java
現在参画しているプロジェクトのメインの言語としてJava11を使用。通常の業務に必要な読み書きは問題なくできるレベル。

- Kotlin
現在参画しているプロジェクトのAndroidアプリで使用。通常の業務に必要な読み書きは問題なくできるレベル。
業務では読み込み、部分的な改修でのみ使用していたが、趣味の個人開発でAndroid アプリ、バックエンドのメイン言語として使用している。

- Go
個人開発のバックエンドとして使用。調べながら読み書きができるレベル。

## 職務経歴（現職）
### 株式会社B（2020-04〜）
### DX事業部
- 配送システム運用保守・追加開発

## 概要
ネットスーパーの配送業務で使用されているシステムの運用・保守・追加開発

### アプリ概要
- 配送管理アプリ(Webアプリ)
配送業務の状況確認・シフトの登録・マスターの登録などの機能を備えた管理アプリ。
Java(Spring Boot)で実装されている。

- ドライバーアプリ(Androidアプリ)
実際に配送を担当するドライバーさんが配送時に使用するアプリ。
Kotlin(Android)・Spring Boot(バックエンド)で実装されている。

## 自分が担当した業務
### バグ改修
### 概要
私が参画した際、本システムは稼働から半年ほど経過していたが、依然バグが多く存在している状況であった。
システムの安定稼働のための既存バグ改修を担当した。

### 使用技術
- Java(Spring Boot)
- JavaScript
- Kotlin(Android)
- PostgreSQL version11
- Docker
- Azure
- Jenkins

### 工夫した点
- 再度バグを発生させない・デクレを発生させないように、システム・業務観点から可能な限り多くのテストを実施した
- バグ発生箇所のみの改修ではなく、周辺のソースのリファクタができないか考えつつ修正を実施した(アーリーリターンへの書き換え・trywithresourcesへの書き換えなど)
- システム保守の経験を活かし、保守性の高いコードを書くように意識した(適切なログの記述・エラーハンドリング)

### 機能追加
### 概要
お客様からの要望や保守目線でのシステム改善提案を行い、対応を行った。

### 詳細
- 緯度経度情報取得改善
配送先の住所情報取得にはGoogleAPIを使用していたが、Google側の問題でAPI実行に失敗した際、
再実行処理がなされておらず、瞬断などのエラーを回避できない状況であった。
住所情報取得がエラーになると、後続業務に影響が出る状況であり、早急に対応が必要であった。

そこで、APIエラー時の再実行処理の追加を提案し、要件定義・設計・開発・テストまで一気通貫で対応を行った。

- 配送車両速度算出バッチの実装
配送時の速度を算出する処理が機能としては定義されていたものの、実装されていない状況であった。
また実際のデータを分析する中で、要件定義時の要件では正しい速度が算出できないことが判明した。
そこで、実際の業務データを分析し、要件定義からやり直しを実施した。
こちらも設計・開発・テストまで実施した。

### 使用技術
- Java(Spring Boot)
- Kotlin(Android)
- PostgreSQL version11
- Docker
- Azure
- Jenkins

### 工夫した点
- 機能追加で既存機能に影響が出ないように最新の注意を払って開発を実施した。
- 機能追加部分だけではなく、周辺の機能のテストも合わせて行い、バグが出ないように心がけた。
- 適切なコメント・アーリーリターン・適切なログなどを通して、保守性を損なわない開発を行った。

### 既存インフラの複製
### 概要
本システムの対抗システムリプレイスに伴い、
本システムとの疎通テストやシステムテストを実施するための環境が必要となった。

インフラ基盤としてはAzureを使用しており、現行の本番環境および検証環境と
同等スペックのインフラ環境構築を実施した。

### 詳細
既存環境は存在するものの、リソースのパラメータシートなどの資料はない状況であったため、
既存環境の調査から開始した。

### 使用技術
- Azureネットワークリソース全般(仮想ネットワーク・ネットワークセキュリティグループ・VPN等)
- Azureコンピューティングリソース(AKS・関数アプリ・AppService)
- Azureデータベースリソース(RDS(PostgreSQL)/CosmosDB/Redis)
- Azureモニタリングリソース(Application Insights/Log Analytics/ VPCフローログ)

### 工夫した点
- パラメータシート・構築手順書の作成
既存環境を作成した際のパラメータや構築手順書などは全くない状態であった。
そのため今回の構築では作成時にパラメータシート・手順書の作成を行い、現状のリソースの状況を確認できるようにした。
- アラートルールの見直し
既存のアラートルールでは、アプリのエラーなどは検知できるものの、DBやインフラのサービス自体のパフォーマンス悪化を検知できていない状況であった。
そのため、環境構築に伴い、アラートルールの見直しを行った。

具体的にはDB/AppService/RedisなどのCPU応答時間などの監視を追加し、しきい値を下回った場合にアラートを発砲し、メールで検知できるようにした。

### 改善したほうが良かった点
IaaCを導入すべきであった。
今回の環境構築では、すべてAzurePortal(Webコンソール)上からGUIで構築を行った。
IaaCの実績がなかったため、GUIでの構築としたが、ほとんど同じ作業を２回繰り返すこととなり非常に非効率であった。
今後のキャッチアップも兼ねて、IaaCの導入を検討すべきであったと感じている。

### テストコード実装
### 概要
2023下旬に本システムがリプレイスされることとなり、
本システムのリプレイスとして本システムを基にした新システムの開発まで完了している状況であった。

しかし新システムではテストコードが一切作成されておらず、
保守性が非常に低いシステムとなってしまっていた。

そのため保守性向上の一環として、テストコードの刷新を行うこととなった。

### 詳細
本システム構築時に作成されたテストコードは存在していたものの
新システムにリプレイスされたため、現状のテストコードは全く動かない状態であった。

上記より完全に新規でのテストコード作成となったため、技術選定から実施した。
体制としては私ともう１人の二人体制であった。
また、本刷新のリーダーとしてテストコードのレビューやスケジュール管理等も行った。

### 使用技術
- Groovy
- Spock
- H2Database
- JUnit
- DbUnit

### 工夫した点

既存のテストコードではDBのテストを行う際、ローカルのDBにテストデータを挿入してテストを行っていた。
そのため、テスト実行環境によってテスト結果に相違が出る状況であった。
また、今後CIなどで自動テストを行う際に問題になると考え、テスト用のデータベースとしてインメモリデータベースを採用した。

また、テストコード作成で発見されたバグや不明確な命名規則などを開発チームへフィードバックを行い
システムの品質向上に取り組むように努めた。
