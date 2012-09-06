cnvk
====

Python で全角・半角・ひらがな・カタカナ等を変換する

 変換マップを指定して、文字列を変換します。
追加の変換マップを dict や tuple で簡単に利用できます。
処理をスキップする文字を指定することが出来ます。

args:
	text: 変換元のテキスト。unicode を必要とします。
	maps: 変換マップの指定。tuple, dict または tuple を返す関数（callable オブジェクト）で指定。
			マップは指定された順序に実行されます。
	skip: 変換しない除外文字の指定。tuple または文字列で指定
			tuple で指定すると各要素を除外。文字列で指定すると含まれる全ての文字を除外。
return:
	converted unicode string

built-in maps:
	H_SPACE (HS): スペースを半角に統一
	H_NUM (HN): 数字を半角に統一
	H_ALPHA (HA): 英字を半角に統一
	H_KIGO (HKG): ASCII記号を半角に統一
	H_KATA (HK): カタカナを半角カタカナに統一
	H_ASCII (HAC): アスキー文字を半角に統一（スペースを除く）（＝H_NUM + H_ALPHA + H_KIGO）
	Z_SPACE (ZS): スペースを全角に統一
	Z_NUM (ZN): 数字を全角に統一
	Z_ALPHA (ZA): 英字を全角に統一
	Z_KIGO (ZKG): ASCII記号を全角に統一
	Z_KATA (ZK): カタカナを全角に統一
	Z_ASCII (ZAC): アスキー文字を全角に統一（スペースを除く）（＝Z_NUM + Z_ALPHA + Z_KIGO）
	HIRA2KATA (H2K): ひらがなをカタカナに変換
	KATA2HIRA (K2H): カタカナをひらがなに変換
	
