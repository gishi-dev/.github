# 業務×AIの公開デモ集

業務の流れにAIを組み込むと、どこまで任せられて、どこで人が確かめるのか。
架空の会社・データを題材に、実際に動くデモとして公開しています。

- 生成AIを使った業務の自動化（Claude API など）と、ルールやコードで決める部分の分け方
- Python・PHP（Laravel）での業務システム・Webアプリ、API連携
- AWSでの構築と運用

どのデモも、AIが下書きや候補を作り、最終的な確認・判断は人が行う形にしています。
開発には Claude Code と OpenAI Codex を使っています。

## 公開しているデモ

| リポジトリ | 内容 |
|---|---|
| [support-faq-rag](https://github.com/gishi-dev/support-faq-rag) | 製品のマニュアルやFAQをもとに、問い合わせへ根拠付きで答えるAIチャット。資料にないことは推測せず窓口へ案内し、答えられなかった質問をFAQ追加の候補として記録します。 |
| [inquiry-triage](https://github.com/gishi-dev/inquiry-triage) | 問い合わせメールを、AIが分類・緊急度・担当に仕分け、社内の対応方針に沿った返信の下書きまで用意するツール。送信は担当者が確認してから行います。 |
| [rule-evaluation](https://github.com/gishi-dev/rule-evaluation) | 多拠点の実績データを集計し、基準値・例外条件などのルールに沿って評価の算出と対象者の抽出を行う仕組み。ルールは担当者が画面で直せ、すべての評価に算出根拠が残ります。 |
| [procurement-navigator](https://github.com/gishi-dev/procurement-navigator) | 10社の架空の仕入先をブラウザで巡り、価格・在庫・納期を比較する調達ナビ。Jevが次の操作を選び、コードが金額と条件を比較します。発注先の確定は担当者が行い、注文機能は含みません。 |
| [document-reconciliation](https://github.com/gishi-dev/document-reconciliation) | 日本語の請求書・納品書PDFをローカルOCRで読み取り、台帳と照合する書類デモ。元ページを見ながら人が候補を修正・確認し、確認済みの結果だけをExcelへ出力します。生成AIは使っていません。 |
| [suspicious-email-review](https://github.com/gishi-dev/suspicious-email-review) | 架空のメール20通を、AIが付けた分類候補・理由・不足情報と並べ、人の確認待ちに渡すデモ。口座変更や認証コードの要求などを人が原文と業務記録で確かめ、理由を付けて判断履歴に残します。保存済みのAI候補を再生するため、APIキーは不要です。 |
| [incident-notes-review](https://github.com/gishi-dev/incident-notes-review) | 架空の事故の初動メモを、AIの整理候補と原文・照合資料で並べて確かめるデモ。人が数や時刻の訂正を採るか決め、食い違いや確認事項が残るものは次の担当と期限を付けて確認待ちに残します。保存済みのAI候補を再生するため、APIキーは不要です。 |
| [settings-ledger-review](https://github.com/gishi-dev/settings-ledger-review) | 架空の設定台帳を、AIが社内基準と比べて「正常・要確認・情報不足」の候補に分けるデモ。人が原記録と照合して確定・修正・保留を選び、残った行に担当と期限を割り当てます。保存済みのAI候補を再生するため、APIキーは不要です。 |
| [ledger-reconciliation](https://github.com/gishi-dev/ledger-reconciliation) | 架空の作業メモとタスク台帳を突き合わせ、担当・期限・状態の食い違いをAIが候補と質問にまとめるデモ。人が元の記録を見て採用・保留・除外を決め、台帳は書き換えずに変更案と確認待ちを残します。保存済みのAI候補を再生するため、APIキーは不要です。 |
| [daily-notice-review](https://github.com/gishi-dev/daily-notice-review) | 架空の団体から届くお知らせを前日までの話題と比べ、AIが新しい話題・続報・再掲の候補を付けるデモ。人が原文と比較元を確かめて採用した項目だけで翌日の一覧を更新し、「更新なし」と「取得失敗」を分けて扱います。保存済みのAI候補を再生するため、APIキーは不要です。 |
| [monthly-chart-review](https://github.com/gishi-dev/monthly-chart-review) | 架空の月次表から作ったグラフや説明文の数字を、コードが元のセルと式で再計算して並べるデモ。人が期間の定義・分母・単位・予測の根拠を確かめて承認・差し戻し・保留を決め、欠損の月は0として計算せず確認待ちにします。保存済みのAI候補を再生するため、APIキーは不要です。 |
| [company-copy-review](https://github.com/gishi-dev/company-copy-review) | 架空の会社説明・料金の原稿を基準情報と照合するデモ。コードが税込・税別を換算して基準の番号と版に結び付け、AIが食い違いと判断材料不足の候補を示します。人が原文と基準を見て採用・修正依頼・保留を決め、未決定の事項は責任者への確認として残します。保存済みのAI候補を再生するため、APIキーは不要です。 |
| [product-translation-backcheck](https://github.com/gishi-dev/product-translation-backcheck) | 架空の商品紹介文の英語案を、訳し戻しと直接の照合の2通りで仕様と照らし合わせるデモ。コードが数値・単位・仕様の版の違いを示し、人が仕様と英語の該当句を見て採用・差し戻し・保留を決めます。単位は換算せず、訳し戻しで補われた内容も候補として示します。保存済みのAI候補を再生するため、APIキーは不要です。 |
| [sales-rehearsal-review](https://github.com/gishi-dev/sales-rehearsal-review) | 架空の商談練習の発言とAIの講評を、条件表と照らし合わせるデモ。人が元の発言と条件を見て講評を採用・差し戻し・保留し、存在しない番号を指す講評なども確かめて、振り返り票と次の練習を残します。人事評価には使わない前提です。保存済みのAI結果を再生するため、APIキーは不要です。 |
| [overseas-proposal-review](https://github.com/gishi-dev/overseas-proposal-review) | 架空の海外向け提案メール・資料と日本語訳を、仮説と未確定条件の準備表と照らし合わせるデモ。仮説の断定、未確定条件の確約、訳での留保の抜けを候補にし、人が採用・差し戻し・保留して送信前の確認票を作ります。送信の機能はありません。保存済みのAI候補を再生するため、APIキーは不要です。 |
| [paid-leave-review](https://github.com/gishi-dev/paid-leave-review) | 架空の年休明細から、年5日に算入する取得済みと確認待ちをコードで分けるデモ。時間単位は算入せず別記し、空欄や食い違いの行は0日として扱わず確認待ちに残します。人が根拠を見て確認済み・未解決と理由を記録します。法令上の判定は行いません。保存済みのAIの出力例を再生するため、APIキーは不要です。 |
| [operation-permission-review](https://github.com/gishi-dev/operation-permission-review) | 架空の顧客台帳への操作依頼から、AIが作った操作案を許可表と照らし合わせるデモ。項目・宛先・保存先が許可の範囲外や不足のものは保留にし、人が原文と照合し直して確認依頼の下書きを確定します。実際の操作・送信はせず、確定は模擬記録に残すだけです。保存済みのAIの構造化案を再生するため、APIキーは不要です。 |
| [stocktake-quantity-review](https://github.com/gishi-dev/stocktake-quantity-review) | 架空の棚卸しで、帳簿と実数の差を、入出庫の反映時点・保管場所・調整履歴と照らし合わせるデモ。同じ伝票の再掲や推測での補完を確認待ちにし、人が回答・保留して計算し直します。帳簿への書き戻しや調整はしません。保存済みのAIの出力例を再生するため、APIキーは不要です。 |
| [first-ai-workflow-selector](https://github.com/gishi-dev/first-ai-workflow-selector) | 架空の業務カードで、入力・確認・停止の条件と既存機能を照らし合わせ、最初にAIを試す1工程を選ぶデモ。条件が足りない業務は保留、既存機能で足りる業務はその候補とし、人が理由付きで1件だけ採用して試行計画を作ります。保存済みのAIの出力例を再生するため、APIキーは不要です。 |
| [business-table-quality-review](https://github.com/gishi-dev/business-table-quality-review) | 架空の業務表で、欠損・古い記録・単位違い・重複を行ごとの確認理由として残すデモ。0や「日」の意味をコードが決めずに人が元記録で確かめ、比較に使える行だけを確認票に出します。保存済みのAIの出力例を再生するため、APIキーは不要です。 |
| [slide-revision-scope-review](https://github.com/gishi-dev/slide-revision-scope-review) | 架空の資料の修正前後を要素IDで比べ、指示の範囲外の変更やページの追加・削除を確認待ちにするデモ。AIが区分の候補を付け、人が差分を開いて採否と理由を確定し、判断材料が足りない要素は依頼者への質問を残して差し戻し依頼の下書きを作ります。送信の機能はありません。保存済みのAIの出力例を再生するため、APIキーは不要です。 |
| [contract-renewal-clause-review](https://github.com/gishi-dev/contract-renewal-clause-review) | 架空の契約と覚書から、満了日と通知期限の候補を条項の根拠付きで出すデモ。管理表との食い違いは人が原文で確かめて修正案にし、覚書の適用が決まっていない契約は2通りの日付を並べたまま確認待ちにします。法的な判断はしません。保存済みのAIの出力例を再生するため、APIキーは不要です。 |
| [fixed-asset-evidence-review](https://github.com/gishi-dev/fixed-asset-evidence-review) | 架空の設備台帳と、所在・移動・廃棄の記録を資産番号と証拠の種類で照らし合わせるデモ。名前が同じ別の資産や、廃棄の予定・連絡しかない資産を確認待ちにし、人が根拠と足りない資料を確かめて確認票を出します。会計・税務の判断はしません。保存済みのAIの出力例を再生するため、APIキーは不要です。 |
| [food-delivery-condition-review](https://github.com/gishi-dev/food-delivery-condition-review) | 架空の食品の表示期限と、取引先ごとの納品条件を照らし合わせるデモ。条件の版・対象のロット・合意の有無をコードが確かめ、条件が欠けている・合意待ち・別の商品の条件を参照しているものは確認待ちにし、人が原文を見て確認票を出します。出荷の承認や法令・安全性の判断はしません。保存済みのAIの出力例を再生するため、APIキーは不要です。 |
| [return-condition-version-review](https://github.com/gishi-dev/return-condition-version-review) | 架空の通販の返品の申し出を、購入した時点の返品条件の版・商品の種類・申し出の理由で照らし合わせるデモ。版の境目、名入れの例外、破損と品違いの区別、資料が足りない注文を確認待ちにし、人が確認依頼と返信案の下書きを作ります。返信の送信や返金の約束はしません。保存済みのAIの出力例を再生するため、APIキーは不要です。 |
| [employment-certificate-review](https://github.com/gishi-dev/employment-certificate-review) | 架空の社員の就労証明書の下書きを、契約・月ごとの勤怠・制度の利用記録と欄ごとに照らし合わせるデモ。短時間勤務、契約の変更、月のずれ、資料が足りない欄を確認待ちにし、人が根拠を確かめて確認票を出します。資料のない値を0にせず、要件の判断や証明書の発行・提出はしません。保存済みのAIの出力例を再生するため、APIキーは不要です。 |
| [panel-quantity-source-review](https://github.com/gishi-dev/panel-quantity-source-review) | 架空の配置資料と見積依頼の数量を、版・ページ・図面番号・区画・注記で照らし合わせるデモ。区画やページの食い違い、再掲の重複、添付の不足、旧版にしかない記載を確認待ちにし、人が原資料を確かめて引き渡し表と確認依頼の下書きを出します。見積金額の算出や発注・送付はしません。保存済みのAIの出力例を再生するため、APIキーは不要です。 |
| [file-list-completeness-review](https://github.com/gishi-dev/file-list-completeness-review) | 架空の資料一覧を、台帳の件数・資料ID・続き・検索完了・版で照らし合わせるデモ。行数がそろっていても、IDの重複・不足・余分、続きあり、検索未完了、記録不明、版の混在を確認待ちにし、人が原記録を確かめて確認一覧と確認依頼の下書きを出します。資料の取得・取り直し・削除・通知はしません。保存済みのAIの出力例を再生するため、APIキーは不要です。 |
| [field-change-review](https://github.com/gishi-dev/field-change-review) | 架空の二つの商品台帳で同じ項目が変わったとき、変更日時だけで上書きせず、項目別の正本・承認・前回値・反映元IDで照らし合わせるデモ。両側の競合、承認不明、前回値の記録なし、同じ変更の再到着を保留にし、人が確認した変更だけを台帳のコピーへ項目単位で反映して、反映結果と保留の一覧を出します。実際の台帳の更新はしません。保存済みのAIの出力例を再生するため、APIキーは不要です。 |
| [ai-dev-workflow](https://github.com/gishi-dev/ai-dev-workflow) | Claude Code・Codex で開発を回す進め方と、AIに渡すルールファイルの見本。IssueからAIが実装し、自己レビューと人の承認を経てマージするまでの仕組みをまとめています。 |

| サポートAIチャット | 問い合わせメールの仕分け |
|---|---|
| ![サポートAIチャット](https://raw.githubusercontent.com/gishi-dev/support-faq-rag/main/images/chat-answer.png) | ![問い合わせメールの仕分け](https://raw.githubusercontent.com/gishi-dev/inquiry-triage/main/images/inbox.png) |

![調達ナビの比較画面](https://raw.githubusercontent.com/gishi-dev/procurement-navigator/main/images/comparison.png)

デモに登場する会社・製品・人物・メール・仕入先・取引条件は、すべて架空のものです。
