
【フォルダ内容】

このフォルダの中には、以下のファイルが含まれています。

jsem_beta_Adjectives_150902.xml
jsem_beta_Attitudes_150902.xml
jsem_beta_Comparatives_150902.xml
jsem_beta_Ellipsis_150902.xml
jsem_beta_GeneralizedQuantifier_150902.xml
jsem_beta_NominalAnaphora_150902.xml
jsem_beta_Plurals_150902.xml
jsem_beta_TemporalReference_150902.xml
jsem_beta_Verbs_150902.xml
　　日本語意味論テストセットβ版のデータです。(2015/9/2修正済みバージョン）
   現象ごとに分割しています。
jsem.dtd
　　xmlの仕様を定めたdtdファイル
jsem.xsl
　　MultiFraCaSに似た形式でデータを表示するためのxslファイル

【前バージョンからの変更点】
・間違いを修正しました。


【データの概要】

FraCaS test suite（Cooper et al.1996）で扱われている以下の各現象について、対応する日本語のテストを作成し、集めたものを中心に構成したものです。

・一般量化子
・複数性
・照応
・省略
・形容詞
・比較
・テンス
・動詞
・命題的態度

FraCaSの対訳となっているテストが中心ですが、自然な対訳を作れない項目の一部に関しては、同様の現象を含む日本語例を独自に作成しています。また、日本語独自の関連現象も一部扱っています。
FraCaSの項目の対訳ではあるが本質的に異なる現象も存在するため、ここではlink要素のtranslation属性とsame_phenomena属性により、「（リンク先の項目と）対訳レベルで同一視できるか」と「現象レベルで同一視できるか」とを明示的に区別しています。
また、FraCaSのテスト項目の中でも、日本語に対応する現象がないもの、またどのような日本語現象を対応させるかについて議論を要するものは含めていません。

テストセット内のXML要素および属性の説明は以下の通りです。（@が付いたものは属性、その下にあるのは属性値の説明です）

-----------------------------------------------------------------------------
jsem_problems：ルート要素。comment, problemを子要素に取る。
comment：全般的なコメント。
problem ： テスト。link, p, h, noteを子要素に取る。
　　@jsem_id：固有の ID
　　@answer：含意関係の有無（ yes, no, unknown, undef ）。
　　　　yes：前提が仮説を含意する
　　　　no: 前提が仮説の否定を含意する
　　　　unknown：前提が仮説を含意せず、その否定も含意しない
　　　　undef：与えられた情報のみからは判断ができない
　　@phenomena： 現象の種類（複数指定可）
　　@inference_type：推論のタイプ。以下のいずれかの値をとる（*）。
　　　　entailment：含意
　　　　presupposition：前提
　　　　CI：conventional implicature
　　　　GCI：generalized conversational implicature
　　　　PCI：particularized conversational implicature
　　　　（*注：現バージョンでは、entailmentとpresuppositionのみが値に入っています）
　　@jsem_nonsatandard：文の特定の解釈を指定する場合にtrueを取る
link ：他言語リソースとのリンク（FraCaS対応部分のみ）
　　@resource 属性： リンク先リソース名
　　@link id ： リンク先の対応項目 ID
　　@translation ： リンク先の項目と対訳レベルで一致するか（ yes,no,unknown ）
　　@same phenomena ： リンク先の項目と現象レベルで一致するか（ yes,no,unknown ）
p ： 前提。script, englishを子要素に取る。
     @idx：前提につけられた通し番号
h ： 前提（群）から推論可能かどうかが問われる文（仮説）。script, englishを子要素に取る。
script：日本語文
english：対応するFraCaS原文（FraCaSの対訳でない文に関しては指定なし）
note ： コメント

-----------------------------------------------------------------------------


【統計情報】（2015/4/15 更新）

(1) テスト数（<problem>要素数）：790
(2) (1)のうち、FraCaSへのリンクを含むもの：624
(3) (2)のうち、FraCaSの対訳になっているもの：501
(4) 現象タグごとのテスト数（注：現象タグは一つのテストに対して複数指定可です。*のついたものはFraCaSのセクションの見出しに対応しています）
	-dake (toritate particle):6
	-ka (disjunctive particle):3
	-koto (complementizer):9
	-mo (conjunctive particle):1
	-ni (conjunctive particle):2
	-no (complementizer):10
	-sika:1
	-to (complementizer):7
	-to (conjunctive particle):6
	-toiukoto (complementizer):8
	-toiuno (complementizer):2
	-toka (conjunctive particle):1
	-ya (conjunctive particle):1
	*Adjective:71
	*Attitudes:60
	*Comparative:75
	E-type anaphora:5
	*Ellipsis:48
	*Generalized Quantifier:363
	N-no QC:65
	NQC:20
	*Nominal Anaphora:36
	*Plurals:44
	Q-no NC:109
	*Temporal reference:49
	Toritate Particle:2
	VP ellipsis:8
	*Verb:36
	absolute adjective:8
	adverb:7
	adverbs of quantification:2
	affirmative adjective:10
	after:10
	anaphoric dimension:1
	aspectual class:6
	attributive comparative:1
	bare noun:17
	bare plural:5
	before:10
	benefactive:2
	bound variable anaphora:9
	causative:3
	cleft:14
	collective and distributive plural:3
	collective predication:1
	comparative:2
	comparative deletion:2
	complex examples:5
	conjoined noun phrase:16
	conjunction distribution:1
	conservativity:116
	counter-factive:1
	default comparison class:2
	definite plural:8
	degree modifier:6
	dependent plural:2
	differential comparative:3
	disjunction distribution:1
	distributive predication:2
	donkey anaphora:4
	ellipsis and anaphora:22
	ellipsis and quantification:1
	ergative verb:2
	existential instantiation:3
	extensional comparison class:14
	factive:16
	floating quantifier:86
	functional and subsectional anaphora:1
	gapping:5
	if-predicate:4
	implicative verb:3
	indexicals:2
	intensional comparison class:12
	inter-sentential:2
	intra-sentential:12
	kare/kanojo (pronoun):18
	measure phrase:1
	mix reading:2
	modal:10
	monotonicity (downwards on first argument):58
	monotonicity (downwards on second argument):58
	monotonicity (upwards on first argument):59
	monotonicity (upwards on second argument):80
	negated plural:10
	negation:40
	negative implicative:2
	no anaphora:6
	no comparison class:9
	non-affirmative adjective:11
	non-factive:5
	only-if-predicate:4
	opposites:15
	partial predicate:2
	passive:15
	perception verb:11
	phrasal ellipsis:5
	plural anaphora:13
	quantificational adverbials:2
	quantificational morpheme:14
	quantifier:26
	relative adjective:8
	scope ambiguity:1
	simple reflexives:3
	sloppy identity:7
	sluicing:1
	so-series demonstrative:5
	soo su anaphora:21
	sosite (conjunctive particle):2
	standard use of tense:7
	strict identity:7
	stripping:10
	stripping (with case marker):3
	substitution:1
	superlative:4
	temporal adverb:22
	total predicate:4
	veridicality:1
	zibun (reflexive):14
