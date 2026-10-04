# 草野球AI査定 Ver.71 calc復旧修正版

Ver.70の画面診断で表示された
`ReferenceError: Can't find variable: calc`
をコード上で確認し、欠落していた calc(p) を復旧しました。

calc(p) は以下を計算する共通関数です:
- 打率 AVG
- 出塁率 OBP
- 長打率 SLG
- OPS
- 塁打 TB

この関数は打撃成績、AI査定、スカウトコメント、
チーム内ランキング等から共通して呼ばれていたため、
欠落するとrender()途中で停止していました。

Ver.70で直した #number / #name DOM取得、STORAGE修正、
最新成績・守備適性・投手能力・総合値バランスも維持しています。
