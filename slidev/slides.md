---
mdc: true
theme: apple-basic
layout: intro-image
highlighter: shiki
image: 'https://cdn.jsdelivr.net/gh/slidevjs/slidev-covers@main/static/Afyjbfs1rKI.webp'
---

<div class="absolute top-10 shadow">
  <span class="font-700">
    Apple Basic
  </span>
</div>

<div class="absolute bottom-10">
  <h1>Slidev with Claude Code</h1>
  <p>AIと協調してスライドを作成する方法</p>
</div>

---
layout: section
---

# Claude Code

---
layout: statement
---

# AI Agentです！！！

---
layout: fact
---

# 100%
弊社の開発エンジニアの使用率

---
layout: quote
---

<div class="absolute inset-0 z-0">
  <img src="https://cdn.jsdelivr.net/gh/slidevjs/slidev-covers@main/static/fVBWN3_ST0E.webp" class="w-full h-full object-cover" />
  <div class="absolute inset-0 bg-black bg-opacity-30"></div>
</div>

<div class="relative z-10">
  <h1>"最も強い者が生き残るのではなく、最も賢い者が生き延びるのでもない。唯一生き残ることが出来るのは、変化できる者である"</h1>
  <p>ダーウィン</p>
</div>


---

# 2ページ目

2ページ目の内容

---
src: ./pages/imported-slides.md
hide: false
---

---

# クリック内容を見てみます！

<v-click>
   <p>この要素は 1回 Right Arrow や Space キーを押すことで表示されました</p>
</v-click>

<div v-click>
  <p>この要素は 2回 Right Arrow や Space キーを押すことで表示されました</p>
</div>

<div v-click>最初のクリックアニメーション</div> <!-- 1回 Right Arrow や Space キーを押すことで表示 -->
<div v-after>最初のクリックアニメーションが発火することで発火するアニメーション</div> <!-- 1回 Right Arrow や Space キーを押すことで表示（上と同タイミング） -->

---
transition: fade
---

# 別のアイテム表示方法

<v-clicks>

- Item 1
- Item 2
- Item 3

</v-clicks>

---

# コンポーネント埋め込み

<Counter :count="10" m="t-4" />

<MyComponent />

---

# シンタックスハイライトの確認

```ts{4-}
import * from
// ES6のアロー関数
const add = (a, b) => a + b;

// Promise使用例
async function fetchData() {
  try {
    const response = await fetch('/api/data');
    const data = await response.json();
    return data;
  } catch (error) {
    console.error('Error:', error);
  }
}
```


---

# Mermaidによる図の作成

<div class="flex justify-center items-center h-full">

```mermaid
sequenceDiagram
  Alice->John: Hello John, how are you?
  Note over Alice,John: A typical interaction
```

</div>

---

# フローチャート

<div class="flex justify-center items-center h-full">

```mermaid
flowchart TD
    A[開始] --> B{条件分岐}
    B -->|Yes| C[処理A]
    B -->|No| D[処理B]
    C --> E[終了]
    D --> E
```

</div>

---

# クラス図

<div class="flex justify-center items-center h-full">

```mermaid
classDiagram
    class Animal {
        -name: string
        -age: int
        +getName(): string
        +setAge(age: int): void
    }
    class Dog {
        -breed: string
        +bark(): void
    }
    Animal <|-- Dog
```

</div>

---

# ガントチャート

<div class="flex justify-center items-center h-full">

```mermaid
gantt
    title プロジェクトスケジュール
    dateFormat  YYYY-MM-DD
    section 設計
    要件定義           :done,    des1, 2024-01-01,2024-01-05
    システム設計       :active,  des2, 2024-01-06, 3d
    section 開発
    フロントエンド開発 :         dev1, after des2, 5d
    バックエンド開発   :         dev2, after des2, 7d
```

</div>

---

# 円グラフ

<div class="flex justify-center items-center h-full">

```mermaid
pie title プログラミング言語使用率
    "JavaScript" : 35
    "Python" : 25
    "Java" : 20
    "TypeScript" : 15
    "その他" : 5
```

</div>

---

# ER図

<div class="flex justify-center items-center h-full">

```mermaid
erDiagram
    USER ||--o{ ORDER : places
    USER {
        int id PK
        string name
        string email
    }
    ORDER ||--|{ ORDER_ITEM : contains
    ORDER {
        int id PK
        int user_id FK
        date order_date
    }
    PRODUCT ||--o{ ORDER_ITEM : includes
    ORDER_ITEM {
        int order_id FK
        int product_id FK
        int quantity
    }
    PRODUCT {
        int id PK
        string name
        decimal price
    }
```

</div>

---

# PlantUML - アクティビティ図

<div class="flex justify-center items-center h-full">

```plantuml
@startuml
!theme plain
start
:ログイン;
if (認証成功?) then (yes)
  :メインメニュー;
  if (データ処理?) then (yes)
    :データ処理;
    :結果表示;
  else (no)
    :設定変更;
  endif
else (no)
  :エラー表示;
endif
:ログアウト;
stop
@enduml
```

</div>

---

# PlantUML - マインドマップ

<div class="flex justify-center items-center h-full">

```plantuml
@startmindmap
!theme plain
* Web開発
** フロントエンド
*** HTML/CSS
*** JavaScript
**** React
**** Vue.js
** バックエンド
*** Node.js
*** Python
*** Java
** データベース
*** MySQL
*** MongoDB
** DevOps
*** Docker
*** CI/CD
@endmindmap
```

</div>

---

# PlantUML - ワイヤーフレーム

<div class="flex justify-center items-center h-full">

```plantuml
@startsalt
{
Name         | "                 "
Modifiers:   | { (X) public | () default | () private | () protected
                [] abstract | [] final   | [] static }
Superclass:  | { "java.lang.Object " | [Browse...] }
}
@endsalt
```

</div>

---

# Iconify

<uim-rocket class="text-3xl text-orange-400 animate-ping" />

---

# YouTube埋め込み

<div class="flex justify-center items-center h-full">
  <Youtube id="umiJU89tJPs" width="800" height="450" />
</div>

---
