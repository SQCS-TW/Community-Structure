# SQCS Bot Command

```markdown
我也不知道為什麼我要寫在這邊
> by. 小灰灰
```

---

## cadre.py

### +ca apply \<cadre\>
> 權限需求：無

於 `#幹部申請區` 申請幹部用指令
```markdown
<cadre>
資料類型
    str
支援參數
    副召, 網管, 議程, 公關, 美宣, 學術
```

### +ca list
> 權限需求：管理者

列出目前所有的申請列表

### +ca permit \<permit_id\>
> 權限需求：管理者

同意成員 `<permit_id>` 的職位申請
```markdown
<permit_id>
資料類型
    int
支援參數
    成員於Discord中的id
```

### +ca search \<search_id\>
> 權限需求：管理者

尋找成員 `<search_id>` 的申請資訊
```markdown
<search_id>
資料類型
    int
支援參數
    成員於Discord中的id
```

### +ca remove \<delete_id\>
> 權限需求：管理者

刪除成員 `<delete_id>` 的申請資訊
```markdown
<delete_id>
資料類型
    int
支援參數
    成員於Discord中的id
```

---

修改成員`<member_id>` `fluctlight` 中 `deep_freeze` 參數為 `<status>`
```markdown
<member_id>
資料類型
    int
支援參數
    成員於Discord中的id

<status>
資料類型
    int
支援參數
    0, 1
```

### +df list
> 權限需求：管理者

列出所有 `deep_freeze` 參數為 `1` 的成員

---

## kick.py

### +kick list
> 權限需求：管理者

列出在踢除列表中的所有成員

### +kick add \<member_id\>
> 權限需求：管理者

新增成員`<member_id>` 到踢除列表中
```markdown
<member_id>
資料類型
    int
支援參數
    成員於Discord中的id
```

### +kick remove \<member_id\>
> 權限需求：管理者

從踢除列表中將成員`<member_id>` 移除
```markdown
<member_id>
資料類型
    int
支援參數
    成員於Discord中的id
```

### +kick kick_single \<member_id\>
> 權限需求：管理者

正式踢除在踢除列表中的成員`<member_id>`
```markdown
<member_id>
資料類型
    int
支援參數
    成員於Discord中的id
```

### +kick all
> 權限需求：管理者

正式踢除在踢除列表中的所有成員

---

## lecture.py

### +lect list
> 權限需求：管理者

列出目前所有的講座資訊

### +lect add \<lect_week\> \<lect_name\>
> 權限需求：管理者

新增一筆講座資訊
```markdown
<lect_week>
資料類型
    int
支援參數
    講座星期數

<lect_name>
資料類型
    str
支援參數
    講座將使用的語音頻道名稱
```

### +lect remove \<del_lect_week\>
> 權限需求：管理者

刪除一筆講座資訊
```markdown
<del_lect_week>
資料類型
    int
支援參數
    講座星期數
```

### +lect start \<week\>
> 權限需求：管理者

開始星期`<week>` 的講座
```markdown
<week>
資料類型
    int
支援參數
    講座星期數
```

### +lect end \<week\>
> 權限需求：管理者

結束星期`<week>` 的講座
```markdown
<week>
資料類型
    int
支援參數
    講座星期數
```

### +lect ans_check \<msg\>
> 權限需求：管理者

檢查成員回答的答案
```markdown
<msg>
資料類型
    list<str>
支援參數
    正確的答案, 以空格格開
```

---

## main.py

### +ping
> 權限需求：無

基本的機器人測試延遲指令

### +clear \<msg_id\>
> 權限需求：管理者

從目前頻道中的最新訊息一路清除至 `id` 為 `<msg_id>` 的訊息
```markdown
<msg_id>
資料類型
    str
支援參數
    訊息在Discord中的id
```

### +findvname \<search_via_name\>
> 權限需求：管理者

利用成員名字`<search_via_name>` 尋找成員`id`
```markdown
<search_via_name>
資料類型
    str
支援參數
    無限制
```

### +findvnick \<search_via_nick\>
> 權限需求：管理者

利用成員名字`<search_via_nick>` 尋找成員`id`
```markdown
<search_via_nick>
資料類型
    str
支援參數
    無限制
```

### +findvid \<search_via_id\>
> 權限需求：管理者

利用成員id`<search_via_id>` 尋找成員名字
```markdown
<search_via_id>
資料類型
    int
支援參數
    成員在Discord中的id
```

### +mibu \<member_id\> \<delta_value\>
> 權限需求：管理者

將成員`<member_id>` 加上`<delta_value>` 分
```markdown
<member_id>
資料類型
    int
支援參數
    成員在Discord中的id

<delta_value>
資料類型
    float
支援參數
    無限制
```

### +active_query
> 權限需求：管理者

查詢伺服器當週活躍度

---

## manipulate.py

### +mani quiz　\<member_id\> \<alter\>
> 權限需求：管理者

修改成員`<member_id>` 的懸賞題正確與否參數至`alter`
```markdown
<member_id>
資料類型
    int
支援參數
    成員於Discord中的id

<alter>
資料類型
    int
支援參數
    0, 1
```

---

## picture.py

### +pic add \<link\>
> 權限需求：無

增加一張圖片至圖片庫
```markdown
<link>
資料類型
    str
支援參數
    圖片連結
```

### +pic remove \<index\>
> 權限需求：無

移除圖片庫中的第`<index>`(0 base) 張照片
```markdown
<index>
資料類型
    int
支援參數
    圖片位置
```

### +pic list
> 權限需求：無

列出在圖片庫中的所有圖片與其位置

### +pic random
> 權限需求：無

隨機發送一張在圖片庫中的圖片

---

## query.py

### +query quiz
> 權限需求：管理者

列出目前懸賞題的答題狀況

### +query my_data
> 權限需求：無

獲取自己的`fluctlight`資訊

### +query member_data \<target_id\>
> 權限需求：管理者

獲取成員`<target_id>` 的`fluctlight`資訊
```markdown
<target_id>
資料類型
    int
支援參數
    成員在Discord中的id
```

---

## weather.py

### +wea query \<target_county\>
> 權限需求：無

獲取城市`<target_county>` 的天氣資訊
```markdown
<target_country>
資料類型
    str
支援參數
    欲查詢的城市名稱
    如果有領取城市身分組，可以不用輸入此參數
```
