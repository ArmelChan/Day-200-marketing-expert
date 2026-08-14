# Skill Name / ID

KARYLEE Marketing OS Router
ID: 00_MARKETING_OS_ROUTER

## Purpose

將用家日常 chatbox 輸入轉化成清晰任務，判斷應調用邊一個 Marketing Skill、需要咩 Context、是否需要 Research，以及最後應輸出咩 Deliverable。

## Trigger Condition

任何進入 Marketing OS 嘅新任務，預設先由本 Skill 處理。

特別包括：

- 用家只有一句簡短要求
- 同一要求涉及多個 Marketing Function
- 用家貼入大量背景資料但未指定輸出
- 任務涉及 Brand / Product / Campaign / Design / Sales / Research
- 需要判斷應否調用多個 Skills
- 用家要求「整合」、「分析」、「生成 Prompt」、「做方案」

## Required Input Fields

最低必需：

- User Request

如有則讀取：

- Brand Name
- Product Name
- Market
- Business Objective
- Target Audience
- Available Documents
- URLs
- Previous Outputs
- Deadline
- Requested Deliverable
- Confidentiality Level

如資料不足：

- 不因缺少非關鍵資料而停止
- 清楚標示 Assumption
- 只在缺少真正阻塞任務嘅必要資料時要求補充

## Step-by-Step Reasoning Workflow

1. **Intent Detection**
   - 判斷用家真正想完成嘅 Business Job。
   - 區分研究、策略、創作、執行、Review、文件輸出。

2. **Context Extraction**
   - 抽取 Brand、Product、Audience、Market、Objective、Channel、Deadline。
   - 區分固定 Brand Context 與本次 Task-specific Context。

3. **Task Classification**
   - 對應至主要 Skill。
   - 如任務跨功能，設定 Primary Skill + Supporting Skills。

4. **Research Requirement Check**
   - 判斷資訊是否具時效性。
   - 如涉及市場、競爭者、產品價格、Campaign、法規、現況，標記需要 Web Research。

5. **Risk & Evidence Check**
   - 判斷是否涉及健康聲稱、商業機密、競爭對手、未證實資料。
   - 建立 Evidence / Insight / Recommendation 分層。

6. **Output Contract Selection**
   - 判斷最適合嘅輸出格式。
   - 例如 Brief、Table、Script、Markdown、CSV-ready、PPT Outline、Action Plan。

7. **Skill Routing**
   - 指派任務至一個或多個 Skills。
   - 定義先後次序與資料傳遞。

8. **Final QA Routing**
   - 所有最終結果進入 17_OUTPUT_ARTIFACTS。
   - 如包含香港市場文案，進行 Hong Kong Native Tone Review。

## Output Format

### Task Interpretation

- Business Objective:
- Primary Task:
- Target Market:
- Required Deliverable:
- Assumptions:

### Skill Routing

| Order | Skill | Purpose | Required Output |
|---|---|---|---|
| 1 | | | |
| 2 | | | |

### Research Requirement

- Web Research Required: Yes / No
- Evidence Required:
- Missing Critical Information:

### Output Plan

- Main Deliverable:
- Supporting Attachments:
- Recommended Format:

## Hong Kong Native Tone Rules

如輸出涉及香港消費者：

- 使用繁體中文（香港）
- 以香港人自然閱讀及說話方式表達
- 避免翻譯腔
- 避免中國內地 Marketing terminology
- English 保留於專業術語
- 不刻意加入廣東話字詞造成過份口語
- B2B 文件保持香港商業書面語
- Social / KOL / Sales 則可提升自然口語程度

## Quality Self-Check

- [ ] 是否理解真正 Business Objective？
- [ ] 是否選中正確 Primary Skill？
- [ ] 是否遺漏需要 Supporting Skill？
- [ ] 是否區分 Fact / Insight / Recommendation？
- [ ] 是否識別需要即時 Research 嘅內容？
- [ ] 是否保護 Confidential Information？
- [ ] 是否設定清晰 Deliverable？
- [ ] 香港市場內容是否套用 HK Native Tone？
- [ ] 是否避免不必要追問？
- [ ] 是否有明確 Handoff？

## Handoff

按任務類型轉交：

- Brand → 01_BRAND_STRATEGY
- Product → 02_PRODUCT_ANALYSIS
- Ingredient-only Product → 03_INGREDIENT_TO_MARKET
- NPD → 04_NEW_PRODUCT_DEVELOPMENT
- Competitor → 05_COMPETITOR_INTELLIGENCE
- Campaign → 06_CAMPAIGN_STRATEGY
- KV / Copy → 07_CREATIVE_COPY_KV
- Design → 08_DESIGN_DIRECTION
- Social → 09_SOCIAL_CONTENT
- Reactive Social → 10_COMPETITOR_REACTIVE_SOCIAL
- KOL → 11_KOL_COLLABORATION
- Sales → 12_SALES_ENABLEMENT
- TV Content → 13_TV_REALITY_CONTENT
- Partner Meeting → 14_BUSINESS_PARTNER_MEETING
- Campaign Research → 15_MARKETING_INTELLIGENCE
- Portfolio → 16_PORTFOLIO_ROADMAP
- Final Output → 17_OUTPUT_ARTIFACTS
