---
mdc: true
---

# MDC Syntax

frontmatter に `mdc: true` を追加することで、MDC Syntax を使用できます。

This is a [red text]{style="color:red"} :inline-component{prop="value"}

---

# 1ページ目

1ページ目の内容

<!--
このコメントアウト部分がスピーカーノートとして表示されます
-->

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

```js {none|1|2}
1; // 1回 Right Arrow や Space キーを押すことでハイライト
2; // 2回 Right Arrow や Space キーを押すことでハイライト
```

---

# コンポーネント埋め込み

<Counter :count="10" m="t-4" />

<MyComponent />

---
