RIME 粵拼輸入法方案
===================


各文件用途：

- jyutping_zeng.schema.yaml RIME 拼字方案
- jyutping_zeng.dict.yaml RIME 編碼方案
- chart.txt 查漏表格（內含非粵字）
- trad2simp.txt 繁簡字對應表
- variants.txt 異體字對應表
- scripts/ 存放輔助文字處理之 BASH 腳本
  - GenDictData 用於產生 Unihan 粵字拼音碼表
  - GenSimpList 用於產生 Unihan 繁簡字對應表
  - GenVariants 用於產生 Unihan 異體字對應表

[Unihan]: http://www.unicode.org/Public/8.0.0/ucd/Unihan.zip


各文件內附註記：

- jyutping_zeng.schema.yaml RIME 拼字方案
  記有特殊功能：輸入中途切換漢語拼音或倉頡（蒼頡）碼模式或反查模式。
  以及說明方便普通用戶自行加入個人詞條或其它自定編碼所需建立的文件。
- jyutping_zeng.dict.yaml RIME 編碼方案
  介紹了好幾個有用的參考資料網站，以及編輯碼表注意事項。
- jyutping_zeng-*.dict.yaml
  拆分好的附屬辭典。

假如你有信心，亦不妨嘗試直接編輯以上文件。
將以上文件放置於用戶配置文件夾，然後重新部署 RIME 即可使用。

請留意調試信息（例如，存在重碼，自動註音時缺音，文件加載失敗）：
- 中州韻 /tmp/rime.ibus.*
- 小狼毫 %TEMP%\rime.weasel.*
- 鼠鬚管 $TMPDIR/rime.squirrel.*
調試時記得清空自動生成的用戶詞典 jyutping_zeng.userdb 清除副作用。

更詳盡的說明請見以下網上文檔：

RIME Wiki
https://github.com/rime/home/wiki
RIME 配置詳解
https://github.com/LEOYoon-Tsaw/Rime_collections/blob/master/Rime_description.md


開發任務：

- [30%] 蒐集詞彙及讀音。
- [70%] 調整常用字字頻。
- [80%] 調整罕用字字頻。
- [99%] 調整簡化字字頻。
- [10%] 調整正讀、異讀、訓讀、破讀、懶音、错音相關字頻。

如發現错音，請先在 chart.txt 做好標記。

若某字於詞彙中有變音，無必要另添單字字音，除非還有更多詞句使用該字音。

絕大部分數據均爲 TSV 格式，稍加編輯後即可以導入至辦公軟件提供的表格編輯工具。

另，在下非專業人士，若有錯漏，敬請多多指正。


本項目之 [Unihan] 數據附帶版權聲明：

COPYRIGHT AND PERMISSION NOTICE

Copyright © 1991-2015 Unicode, Inc. All rights reserved.
Distributed under the Terms of Use in
http://www.unicode.org/copyright.html.

Permission is hereby granted, free of charge, to any person obtaining
a copy of the Unicode data files and any associated documentation
(the "Data Files") or Unicode software and any associated documentation
(the "Software") to deal in the Data Files or Software
without restriction, including without limitation the rights to use,
copy, modify, merge, publish, distribute, and/or sell copies of
the Data Files or Software, and to permit persons to whom the Data Files
or Software are furnished to do so, provided that
(a) this copyright and permission notice appear with all copies
of the Data Files or Software,
(b) this copyright and permission notice appear in associated
documentation, and
(c) there is clear notice in each modified Data File or in the Software
as well as in the documentation associated with the Data File(s) or
Software that the data or software has been modified.

THE DATA FILES AND SOFTWARE ARE PROVIDED "AS IS", WITHOUT WARRANTY OF
ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE
WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT OF THIRD PARTY RIGHTS.
IN NO EVENT SHALL THE COPYRIGHT HOLDER OR HOLDERS INCLUDED IN THIS
NOTICE BE LIABLE FOR ANY CLAIM, OR ANY SPECIAL INDIRECT OR CONSEQUENTIAL
DAMAGES, OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE,
DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER
TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR
PERFORMANCE OF THE DATA FILES OR SOFTWARE.

Except as contained in this notice, the name of a copyright holder
shall not be used in advertising or otherwise to promote the sale,
use or other dealings in these Data Files or Software without prior
written authorization of the copyright holder.
