# 參考資料

這份文件列出受控技術中文參考的資料。每一筆資料都寫出它和這份規範的關係。

關係分成四種：

- **借用**：這份規範借用了它的做法。
- **一致**：它的做法和這份規範的某條規則相同。
- **分工**：它處理的範圍，這份規範不處理。寫那個範圍的內容時，直接參考它。
- **背景**：它提供白話寫作的原則、受控語言的分類，或受控語言的效果和限制的研究。

## 啟發來源

**ASD-STE100 Simplified Technical English**，Issue 9，2025-01-15。ASD（Aerospace, Security and Defence Industries Association of Europe）。[官方網站](https://www.asd-ste100.org/)

- 借用：一個詞只有一個意思、一句只寫一件事、條件寫在動作前面、寫出動作者。
- 這份規範沒有使用 STE100 的詞表，也沒有翻譯它的規則。STE100 是為英文設計的，它的規格書由 ASD 擁有版權。

## 寫需求的標準

**RFC 2119**：S. Bradner，*Key words for use in RFCs to Indicate Requirement Levels*，1997。[原文](https://www.rfc-editor.org/rfc/rfc2119)
**RFC 8174**：B. Leiba，*Ambiguity of Uppercase vs Lowercase in RFC 2119 Key Words*，2017。[原文](https://www.rfc-editor.org/rfc/rfc8174)

- 一致：規則 2.3 和 RFC 2119 都為指定的情態詞定義固定的意思。
- 不同之處：規則 2.3 限制表示要求時的用詞；RFC 2119 和 RFC 8174 不要求所有的要求都使用這些關鍵詞。
- RFC 8174 補充：只有全大寫的 MUST、SHOULD、MAY 等詞，才有 RFC 2119 定義的意思。

**EARS**：A. Mavin、P. Wilkinson、A. Harwood、M. Novak，*Easy Approach to Requirements Syntax (EARS)*，17th IEEE International Requirements Engineering Conference，2009，頁 317–322。doi:[10.1109/RE.2009.9](https://doi.org/10.1109/RE.2009.9)。[作者的說明頁](https://alistairmavin.com/ears/)

- EARS 用五種固定的句型寫需求，例如 `When <trigger>, the <system> shall <response>`。
- 一致：規則 3.4 要求條件寫在動作前面，和 EARS 的句型相同。
- EARS 提供固定的需求句型。這份規範也限制句子的結構，並另外規定用詞和需求資訊的完整性。兩者可以一起使用。

**ISO/IEC/IEEE 29148:2018**：*Systems and software engineering — Life cycle processes — Requirements engineering*。這份標準要付費才能閱讀，本專案沒有讀過全文。

- 背景：需求工程的國際標準，包含需求規格的範本。

**美國聯邦公路總署（FHWA）**：*Systems Engineering for ITS*，第 3.3.6 節。[原文](https://ops.fhwa.dot.gov/seits/sections/section3/3_3_6.html)

- 這一節列出好的需求具備的品質特性，例如必要、不含糊、完整、可行，並逐項說明怎麼確認。
- 背景：寫需求時，可以用這份清單檢查每一條需求。

**美國聯邦 Plain Language 指引**：*Use “must” to indicate requirements*。原本刊登在 plainlanguage.gov，現在封存在 [GSA/plainlanguage.gov](https://github.com/GSA/plainlanguage.gov/blob/main/_pages/guidelines/conversational/use-must-to-indicate-requirements.md)。

- 這份指引建議用 must 表示義務，不用 shall。理由是 shall 可以表示義務，也可以表示預測。
- 一致：規則 2.3 在規格句裡不用「應」「需」「要」表示要求，理由相同：這些詞同時有好幾種意思。

**ISO 24495-1:2023**：*Plain language — Part 1: Governing principles and guidelines*。要付費才能閱讀。[ISO 的標準頁](https://www.iso.org/standard/78907.html)

- 背景：白話寫作的國際標準。標準寫明，它適用於大多數的書寫語言。

## 寫作指南

**Google developer documentation style guide**：[Writing for a global audience](https://developers.google.com/style/translation)
**Microsoft Writing Style Guide**：[Global communications: Writing tips](https://learn.microsoft.com/en-us/style-guide/global-communications/writing-tips)

- 兩份指南都要求一個概念只用一個詞，而且全文一致。Google 也建議：代名詞有歧義時，換成名詞。
- 一致：規則 1.1（一個東西只用一個名稱）和規則 3.3（指代只能有一個對象）。

**Microsoft 中文（繁體）在地化風格指南**：*Chinese (Traditional) Localization Style Guide*。[PDF](https://aka.ms/chinese-traditional-styleguide)

- 這份指南規定 Microsoft 產品的繁體中文介面文字和錯誤訊息怎麼寫。例如：同一個意思只用一種說法、少用被動句、中文和英文之間加半形空格。
- 分工：這份規範不處理介面文字的語氣和措辭。寫介面文字時，可以參考這份指南。規格引用介面文字時，依規則 1.4，照介面上的文字寫。

## 中文的相關專案

**简明技术中文**（Simplified Technical Chinese）：[mzopedia/simplified-technical-chinese](https://github.com/mzopedia/simplified-technical-chinese)

- 這個專案也借鏡 STE100。它有 40 條規則、約 170 條的受控詞表、一支檢查腳本，以及給 LLM agent 用的技能檔。它的句長上限和自動檢查的規則，依 350 萬字的真實技術文件校準。
- 和這份規範的差別：

  | | 简明技术中文 | 受控技術中文 |
  |---|---|---|
  | 文字 | 簡體中文、中國大陸用語 | 繁體中文、台灣用語 |
  | 主要對象 | 操作手冊、API 文件、AI 的解釋性回答 | 軟體規格和需求文件 |
  | 主要形式 | 規則、詞表和檢查腳本 | 規則和改寫前後的範例 |

**Fenng/Tech-Doc-Style-Chinese** 的「受控中文技术写作」模組：[原文](https://github.com/Fenng/Tech-Doc-Style-Chinese/blob/main/references/controlled-technical-chinese.md)

- 這個模組列出受控寫作的原則，例如一個概念只用一個術語、一步只寫一個主要動作、條件和警告寫在動作前面。它不把句長訂成硬性的規則。
- 這個模組寫明它借鏡 STE100，不是 STE100 的中文版。內容是簡體中文。

## 排版、標點和用詞

這份規範規定名稱、動詞和情態詞的使用方式。排版、標點、字形，以及一般字詞的查考，參考下列資料。

- [中文文案排版指北](https://github.com/sparanoid/chinese-copywriting-guidelines)：中文和英文之間的空格、全形標點、專有名詞的大小寫。
- 教育部，[《重訂標點符號手冊》修訂版](https://language.moe.gov.tw/001/upload/files/site_content/m0001/hau/haushou.htm)：標點符號的用法。
- 教育部，[《重編國語辭典修訂本》](https://dict.revised.moe.edu.tw/)：字詞的意思和寫法。
- 國家教育研究院，[樂詞網](https://terms.naer.edu.tw/)：學術名詞和技術名詞在台灣的譯名。
- [zhtw-mcp](https://github.com/sysprog21/zhtw-mcp)：自動檢查繁體中文的用語、標點和字形，例如把「軟件」改成「軟體」。它檢查字和詞，不檢查句子有沒有兩種讀法。依規則 1.1 為一個東西選定一個名稱後，可以把不用的其他名稱寫進它的設定檔，由它找出這些名稱。

## 受控語言的研究

### 受控語言的分類

**T. Kuhn**，*A Survey and Classification of Controlled Natural Languages*，*Computational Linguistics* 40(1)，2014，頁 121–170。doi:[10.1162/COLI_a_00168](https://doi.org/10.1162/COLI_a_00168)。[arXiv](https://arxiv.org/abs/1507.01701)

- 背景：這篇論文整理了 100 種以英文為基礎的受控語言。

**S. O'Brien**，*Controlling Controlled English: An Analysis of Several Controlled Language Rule Sets*，EAMT-CLAW 2003。[PDF](https://mt-archive.net/00/CLT-2003-Obrien.pdf)

- 背景：這篇論文比較了 8 套受控英文的規則，發現所有規則集都有的規則只有一條。受控語言沒有公認的共同規則，每一套都依自己的用途設計。

### STE 對讀者的效果

下列研究探討維修程序文件，不是軟體規格。研究的情境包括航空維修和小型內燃機的維修。

**S. K. Shubert、J. H. Spyridakis、H. K. Holmback、M. B. Coney**，*The Comprehensibility of Simplified English in Procedures*，*Journal of Technical Writing and Communication* 25(4)，1995，頁 347–369。doi:[10.2190/WG69-D74B-4DLL-2WBK](https://doi.org/10.2190/WG69-D74B-4DLL-2WBK)

- 背景：比較複雜的程序文件，改用 Simplified English 後，讀者理解得比較好。

**S. G. Chervak、C. G. Drury、J. P. Ouellette**，*Simplified English for Aircraft Workcards*，*Proceedings of the Human Factors and Ergonomics Society Annual Meeting* 40(5)，1996，頁 303–307。doi:[10.1177/154193129604000502](https://doi.org/10.1177/154193129604000502)

- 背景：175 位航空維修技師參加。Simplified English 提升了理解度。困難的工作卡和非英語母語的技師，效果比較明顯。

**S. G. Chervak、C. G. Drury**，*Effects of job instruction on maintenance task performance*，*Occupational Ergonomics* 3，2003，頁 121–131。doi:[10.3233/oer-2003-3204](https://doi.org/10.3233/oer-2003-3204)

- 背景：Simplified English 版本的操作錯誤比較少。但一半用 Simplified English、一半用原文的版本，錯誤反而增加。

**J. Ma、C. G. Drury、C. V. Marin**，*Language Error in Aviation Maintenance: Quantifying the Issues and Interventions in Four World Regions*，*The International Journal of Aviation Psychology* 20(1)，2009，頁 25–47。doi:[10.1080/10508410903416136](https://doi.org/10.1080/10508410903416136)

- 背景：研究涵蓋四個地區的 941 位技師。在美國以外，Simplified English 沒有一致的效果。唯一一致有效的做法，是把文件翻譯成讀者的母語。

### 模糊的需求對 LLM 的影響

**J. J. W. Wu、F. H. Fard**，*HumanEvalComm: Benchmarking the Communication Competence of Code Generation for LLMs and LLM Agent*，2024。[arXiv](https://arxiv.org/abs/2406.00215)

- 背景：題目的描述有不一致、模糊或不完整的地方時，Code LLM 超過 60% 的回應仍然直接寫程式，不提出問題。

**Z. Fang 等**，*ClarifyCodeBench: Evaluating LLMs on Clarifying Ambiguous Requirements for Code Generation*，2026。預印本，還沒有經過同儕審查。[arXiv](https://arxiv.org/abs/2607.00711)

- 背景：把需求改成模糊的版本後，七種模型設定的 pass@1 全部下降，降幅是 7.8 到 19.8 個百分點。
- 這兩篇研究說明模糊的需求會讓 LLM 寫出比較差的程式。它們沒有比較受控語言和一般文字的效果。

## 工具

- [AutoCorrect](https://github.com/huacnlee/autocorrect)：自動修正中文的排版，例如中文和英文之間的空格。
- [Vale](https://vale.sh/)：文字檢查工具。可以把術語表寫成「不用的詞 → 改用的詞」的替換規則。
- [textlint-rule-preset-ja-technical-writing](https://github.com/textlint-ja/textlint-rule-preset-ja-technical-writing)：日文技術寫作的檢查規則，例如句長和雙重否定。製作中文的檢查工具時，可以參考它。
