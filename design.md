# Green Life Food Festa — Design System

> オーガニック＆ナチュラルマルシェのイベントサイト。
> グリーン一色のブランドカラーと、和欧混植タイポグラフィが特徴。
> WordPress テーマ（カスタム）/ font-size ベース: `html { font-size: 62.5% }` → 1rem = 10px

---

## 1. Design Philosophy

| 原則 | 説明 |
|------|------|
| **Green = Brand** | `#4ab134` がロゴ・背景・ボタン・テキストアクセントすべてを貫く唯一のブランドカラー |
| **自然 × 余白** | ホワイト・ライトグリーンの大きな余白でオーガニック感を表現。装飾は最小限 |
| **和欧混植** | 見出しに欧文ディスプレイ体（Renner*）、本文に日本語ゴシック（Kosugi）を組み合わせる |
| **全画面スタック** | 各セクションが 100vh 単位で積み重なり、スクロールで体験が展開する |
| **画像主導** | イベント写真・スライドショーがコンテンツの核。テキストは写真を引き立てる脇役 |

---

## 2. Color Palette

### ブランドカラー

```css
/* Primary */
--green:        #4ab134;   /* ロゴ / ヘッダー背景 / ボタン / テキストアクセント / SVGフィル */
--green-light:  #e6f7e3;   /* Schedule セクション背景 */

/* Neutrals */
--white:        #ffffff;   /* コンテンツ背景 / カード / フッター背景 */
--gray-f5:      #f5f5f6;   /* article note ブロック背景 */
--gray-eb:      #EBEBEC;   /* 区切り線 / Instagram セクション背景 / hr */
--gray-de:      #dedee0;   /* 破線ボーダー */
--gray-dd:      #dddddd;   /* widget リスト境界線 */

/* Text */
--text-dark:    #333333;   /* 本文 / 小見出し */
--text-mid:     #767676;   /* メタ情報 / h5 */
--text-light:   #999999;   /* 日付 / 終了イベント / completed ラベル */
--text-faint:   #cccccc;   /* タイムスタンプ */
--text-muted:   #aaaaaa;   /* エラーメッセージ */

/* Accent */
--orange:       #DB7B00;   /* リンクホバー / PICKUP ラベル / focus border */
--brown-dark:   #3E352E;   /* ページトップボタン（btn-scroll）背景 */

/* Overlays */
--hero-overlay: rgba(255,255,255,0.20);   /* スライド画像オーバーレイ */
--shadow-soft:  rgba(17,17,17,0.05);      /* schedule-item ドロップシャドウ */
--shadow-nav:   rgba(17,17,17,0.10);      /* side-navigation ドロップシャドウ */
--shadow-card:  rgba(0,0,0,0.20);         /* 画像テキストシャドウ */
```

### カラー使用マップ

| 要素 | カラー |
|------|--------|
| `<body>` 背景 | `#4ab134` ← ページ読み込み前の見え方 |
| ヒーロー背景 | `#4ab134` |
| Schedule セクション背景 | `#e6f7e3` |
| News セクション背景 | `#ffffff` |
| Instagram セクション背景 | `#EBEBEC` |
| Footer 背景 | `#ffffff` |
| ナビゲーションパネル背景 | `#ffffff` |
| 区切り線（solid） | `#EBEBEC` (3px solid) |
| 区切り線（dashed） | `#dedee0` (1px dashed) |
| 終了イベントテキスト | `#999999` |
| 終了イベントカテゴリ背景 | `#999999` |

---

## 3. Typography

### フォントスタック

```css
/* 本文・UI */
font-family: "Kosugi", "游ゴシック", YuGothic,
             "ヒラギノ角ゴ ProN W3", "Hiragino Kaku Gothic ProN",
             "メイリオ", Meiryo, sans-serif;

/* 見出し・ボタン・装飾テキスト */
font-family: "Renner*", "Kosugi", "游ゴシック", YuGothic,
             "ヒラギノ角ゴ ProN W3", "Hiragino Kaku Gothic ProN",
             "メイリオ", Meiryo, sans-serif;
```

**Google Fonts ロード:** `Kosugi`  
**外部フォント:** `Renner*` (indestructibletype-fonthosting.github.io/renner.css)

### フォントサイズ基準

```css
html { font-size: 62.5%; }  /* 1rem = 10px */
body { font-size: 100%; }   /* = 16px (browser default) */
```

### Type Scale

| Role | px | rem | Weight | Font | Color | Letter-spacing | Line-height |
|------|----|-----|--------|------|-------|----------------|-------------|
| Section heading (h3) | 92px | 9.2rem | 800 | Renner* | `#4ab134` | `0.5rem` | `1.2` |
| Section heading — mobile | 30px | 3rem | 800 | Renner* | `#4ab134` | — | — |
| Section sub (h3 span) | 24px | 2.4rem | 400 | Kosugi | `#333` | — | — |
| Section sub — mobile | 16px | 1.6rem | 400 | Kosugi | `#333` | — | — |
| Article page H1 | 58px | 5.8rem | 800 | Renner* | `#4ab134` | `0.2rem` | `1.3` |
| Article page H1 — mobile | 30px | 3rem | 800 | Renner* | `#4ab134` | — | — |
| Article inner H1 | 28px | 2.8rem | 600 | Renner* | `#4ab134` | `0.2rem` | — |
| Article inner H2 | 26px | 2.6rem | 600 | Renner* | `#4ab134` | `0.2rem` | — |
| Article inner H3 | 20px | 2rem | 600 | Renner* | `#4ab134` | `0.2rem` | — |
| Home H2 | 34px | 3.4rem | 200 | Renner* | `#333` | `0.2em` | — |
| Home H2 — mobile | 22px | 2.2rem | 200 | Renner* | `#333` | `0.2em` | — |
| Message headline | 26px | 2.6rem | 800 | Kosugi | inherit | `0.34rem` | `1` |
| Message body | 16px | 1.6rem | 400 | Kosugi | `#333` | `0.24rem` | `1.9` |
| Message emphasis | 18px | 1.8rem | 600 | Renner* | inherit | — | — |
| Schedule card title | 24px | 2.4rem | 800 | Renner* | `#4ab134` | `0.15rem` | `1.3` |
| Schedule entry copy | 20px | 2rem | 600 | Renner* | inherit | `0.2rem` | — |
| Schedule entry subcopy | 16px | 1.6rem | 400 | Renner* | inherit | `0.2rem` | — |
| Schedule overview table | 13px | 1.3rem | 400 | Kosugi | `#333` | `0.2rem` | `1.6` |
| Schedule date | 15px | 1.5rem | 600 | Renner* | inherit | `0.16rem` | — |
| Schedule category label | 14px | 1.4rem | 400 | Kosugi | `#fff` | `0.4rem` | — |
| News list item | 15px | 1.5rem | 400 | Kosugi | `#222` | `0.1rem` | `1.3` |
| News date | — | — | 400 | Renner* | `#999` | `0.2rem` | — |
| btn-link | 20px | 2rem | 600 | Renner* | `#4ab134` | `0.1em` | — |
| btn-more | 20px | 2rem | 800 | Renner* | `#4ab134` | `0.2em` | — |
| btn-more — mobile | 14px | 1.4rem | 800 | Renner* | `#4ab134` | `0.2em` | — |
| Side nav links | 24px | 2.4rem | 600 | Renner* | `#4ab134` | `0.1em` | — |
| Side nav sub | 13px | 1.3rem | 100 | Kosugi | `#4ab134` | — | — |
| Logo | — | — | 800 | Renner* | `#4ab134` | `0.04em` | — |
| Footer menu links | 18px | 1.8rem | 400 | Kosugi | `#4ab134` | — | — |
| Footer copy | 12px | 1.2rem | 400 | Renner* | inherit | `0.18em` | — |
| Entry meta | 11px | 0.6875rem | 800 | Kosugi | `#767676` | `0.1818em` | — |
| widget-title | 13px | 0.8125rem | 800 | Kosugi | `#222` | `0.1818em` | — |
| h5 (base) | 13px | 0.8125rem | 800 | Kosugi | `#767676` | `0.15em` | — |
| Body base | 16px | 100% | 400 | Kosugi | `#333` | — | `1.66` |
| Article body | 16px | 1.6rem | 400 | Kosugi | `#333` | `0.12rem` | `1.9` |

---

## 4. Spacing

### ベース単位

`html { font-size: 62.5% }` のため、rem ベースのスペーシング。

### セクション padding

| セクション | Desktop | Mobile |
|-----------|---------|--------|
| 各 section 下部 | `padding-bottom: 10rem` (100px) | `4rem` (40px) |
| Schedule リスト上部 | `padding-top: 12rem` | `7rem` |
| Instagram wrapper 上部 | `padding-top: 6rem` | `2rem` |
| Pickup wrapper 上部 | `margin-top: 6em` | `3em` |
| wrap (コンテンツ幅) | `padding: 0 2em` | `padding: 0 1.8em` |
| wrap ホームトップ | `padding-top: 3em` | `1em` |

### コンポーネントスペーシング

| 要素 | 値 |
|------|---|
| Schedule card margin | `4rem 0` (desktop) / `2rem 0` (mobile) |
| Schedule card padding | `3rem 0` (desktop) / `1.5rem` (mobile) |
| Schedule event-detail gap | `margin: 2.5rem 3rem 0` |
| Schedule left col | `width: 30%` |
| Schedule right col | `width: 70%; padding-left: 2.6rem` |
| News list margin | `15rem 0 6rem` (desktop) / `10rem 0 4rem` (mobile) |
| News list item padding | `0.4rem 3.2rem` |
| Message headline margin | `4rem 0 4.2rem` |
| Message CTA margin-top | `5rem` |
| Footer wrap padding | `3rem 0` |
| Footer left col width | `60%` |
| Footer right col width | `40%` |
| Footer menu margin-right | `6rem` |
| Footer menu margin-bottom | `3rem` |
| Instafeed item width | `240px` |
| Instafeed item margin | `2rem 0` |
| Instafeed thumb height | `240px` |
| Instafeed — mobile item | `width: 45%; max-width: 154px` |

---

## 5. Border Radius

| コンポーネント | 値 |
|--------------|---|
| `btn-link` | `25px` |
| `btn-more` | `45px` |
| `btn-insta` | `35px` |
| `post-thumbnail a` | `14px` |
| `footer-tag-list a` | `30px` |
| `input / select / textarea` | `4px` |
| `footer-sns a` | `50%` (円形) |
| `btn-scroll` | `50%` (円形) |
| Article `tags a` | `0.2rem` |
| Article images | `1em` |
| `label-over` corner ribbon | overflow: hidden でクリッピング |

---

## 6. Shadows & Elevation

| 要素 | Shadow |
|------|--------|
| `.schedule-item` | `drop-shadow(0 2px 5px rgba(17,17,17,0.05))` |
| `#side-navigation` | `drop-shadow(-2px 0 5px rgba(17,17,17,0.1))` |
| `#instafeed .thumb` | `drop-shadow(0 1px 3px rgba(17,17,17,0.1))` |
| Article `.feature-txt` | `drop-shadow(0 2px 3px rgba(17,17,17,0.1))` |
| Article images | `drop-shadow(0 2px 6px rgba(0,0,0,0.2))` |
| `screen-reader-text:focus` | `0 0 2px 2px rgba(0,0,0,0.6)` |
| `.label-over p` | `drop-shadow(0 2px 5px rgba(0,0,0,0.1))` |

---

## 7. Components

### 7.1 Fixed Header (`#main-header`)

```
position: fixed; top: 0; left: 0; width: 100%; z-index: 85
背景: 透明（コンテンツが透けて見える）
transition: .3s
```

- **ロゴ** (`#header-logo`): `position: absolute; top: 1.4rem; left: 2rem` / Renner* / weight 800 / `#4ab134` / letter-spacing 0.04em
- **ハンバーガー** (`#hamburger`): `top: 2.5rem; right: 3.2rem; width: 3.5rem; height: 3rem` / 2本のスパン（緑 `#4ab134`）

### 7.2 Side Navigation (`#side-navigation`)

```
width: 300px; height: 100vh
background: #fff
position: fixed; top: 0; right: -300px  ← 閉じた状態
z-index: 90
.nav-open: right: 0; transition: .3s
.body-slide: margin-left: -300px; transition: .3s  ← body 押し出し
```

- **メニューリンク**: 24px / weight 600 / Renner* / `#4ab134` / hover: opacity 0.7
- **SNSアイコン**: 30×30px / fill `#4ab134` / 画面下部に固定

### 7.3 ヒーローエリア (`#featured-area`)

```
width: 100%; height: 100vh (JS: calc(var(--vh,1vh)*100))
background: #4ab134
position: fixed; top: 0; left: 0; z-index: 20
```

**レイアウト（デスクトップ）：**
```
┌─────────────────────────────┐
│ ロゴ画像 (46%, 85vh)  │ スライドショー (48%) │
│ z-index: 40           │ z-index: 25          │
│                       │ + rgba(255,255,255,0.20) overlay │
└─────────────────────────────┘
```

**スライドショー:**
- スライド要素: `background-position: center; background-size: cover`
- アクティブクラス: `.slide-active`
- アニメーション: `"mainImg"` 5s ease 0.5s 1回 fill-mode: both

**レイアウト（モバイル）：**
- `position: relative`（固定解除）
- ロゴ: `width: 80%; height: 50vh; margin: 25% 0 0 5%`
- スライドショー: `width: 100%; height: 50vh` 下半分

### 7.4 Buttons

#### `.btn-link`（主要CTA）

```css
display: inline-block;
width: 300px;
padding: 1rem;
border: solid 1px #4ab134;
border-radius: 25px;
font-size: 20px; font-weight: 600;
font-family: Renner*;
color: #4ab134;
letter-spacing: .1em;

/* ::after 矢印 */
width: 9px; height: 9px;
border-right: solid 2px #4ab134;
border-bottom: solid 2px #4ab134;
transform: rotate(-45deg);
position: absolute; top: 50%; right: 2rem;
transition: .3s;

/* hover */
background: #4ab134; color: #fff;
hover::after: border-color #fff; right: 1.5rem;
```

#### `.btn-more`（もっと見る）

```css
display: inline-block;
padding: 1rem;
border: solid 1px #4ab134;
border-radius: 45px;
font-size: 20px; font-weight: 800;
color: #4ab134;
letter-spacing: .2em;

/* ::after 矢印 */
width: 10px; height: 10px;
border-right: solid 2px #4ab134;
border-bottom: solid 2px #4ab134;
position: absolute; top: 50%; right: 1.8em;

/* hover */
background: #4ab134; color: #fff;
hover::after: border-color #fff; right: 1.2em;
hover svg: fill #fff;
```

#### `.btn-insta`（Instagram）

```css
display: inline-block;
padding: .6em 1.8em;
background: #fff; border: solid 1px #fff;
border-radius: 35px;
font-size: 15px; font-style: italic;
font-family: Renner*; letter-spacing: .18em;

/* hover */
border-color: #DB7B00; color: #DB7B00;
hover svg: fill #DB7B00;
```

### 7.5 Schedule Card (`.schedule-item`)

```
background: #fff
margin: 4rem 0; padding: 3rem 0
filter: drop-shadow(0 2px 5px rgba(17,17,17,0.05))
transition: .3s
position: relative
```

**カテゴリラベル (`.entry-cat a`):**
```css
padding: .6rem 3rem;
background: #4ab134;
font-size: 14px; color: #fff; letter-spacing: .4rem;
/* ::after 矢印ノッチ */
border-width: 16px 10px; border-color: transparent #fff transparent transparent;
```

**イベントタイトル (`.article-title a`):**
```css
font-size: 24px; font-weight: 800; font-family: Renner*;
color: #4ab134; letter-spacing: .15rem; line-height: 1.3;
hover: opacity .8;
```

**詳細テーブル (`.entry-overview`):**
```
border-top: solid 3px #EBEBEC; border-bottom: solid 3px #EBEBEC;
行境界: dashed 1px #dedee0
padding: .8rem; font-size: 13px; line-height: 1.6; letter-spacing: .2rem;
th width: 110px;
```

**「READ MORE」リンク:**
```css
font-size: 16px; font-weight: 600; font-family: Renner*;
color: #4ab134; letter-spacing: .2rem;
::after 矢印: 8×8px; border-right/bottom: 2px solid #4ab134;
hover: opacity .8; right: .5rem;
```

**終了イベント (`.event-over`):**
```css
.entry-title a: color #999;
.title-logo: fill #999;
.entry-cat a: background #999;
```

**終了ラベル (`.label-over`):**
```css
/* コーナーリボン */
position: absolute; top: -.4rem; right: -.4rem;
width: 250px; height: 252px; overflow: hidden;

p: background #999; color #fff; letter-spacing .3rem;
   transform: rotate(45deg); font-size: 12px;
   drop-shadow(0 2px 5px rgba(0,0,0,0.1));
```

### 7.6 Post Thumbnail (`.post-thumbnail`)

```css
a: display block; height 270px; border-radius 14px; overflow hidden;
figure: height 270px; background-size cover; transition .3s;

/* hover */
figure: scale(1.05) opacity .9;
figure::after: content 'READ MORE';
  display flex; justify-content center; align-items center;
  width 88%; height 86%; border: 1px solid #fff; border-radius 14px;
  font-size 16px; font-family Renner*; font-style italic; color #fff;
  letter-spacing .2em; text-shadow 0 2px 3px rgba(34,34,34,0.3);
```

### 7.7 News List (`.list-news`)

```
border-top: solid 3px #EBEBEC; border-bottom: solid 3px #EBEBEC;
li border-bottom: dashed 1px #dedee0;

a: padding .4rem 3.2rem; font-size 15px; letter-spacing .1rem; line-height 1.3;
   hover: color #4ab134;

time: width 105px; color #999; font-family Renner*; letter-spacing .2rem;
```

### 7.8 Instagram Feed (`#instafeed`)

```
display: flex; justify-content: space-around; flex-flow: row wrap;
li: width 240px; margin 2rem 0;
.thumb: height 240px; overflow hidden; drop-shadow(0 1px 3px rgba(17,17,17,0.1));

/* hover */
figure: scale(1.1) opacity .9;
figure::after: 'VIEW MORE'; border 1px solid #fff; font-weight 800; letter-spacing .2em;

/* フォローエリア */
.follow-area: width 240px; height 240px; background #fff;
.follow-area span: 28px / weight 800 / Renner* / #4ab134 / letter-spacing .4rem;
.follow-area svg: 40×40px; fill #4ab134;
hover: background #4ab134; span color #fff; svg fill #fff; span scale(1.1);
```

### 7.9 PICKUP ラベル (`.label-pickup`)

```css
width: 85px; height: 85px;
background-image: linear-gradient(135deg, #DB7B00 60px, transparent 0);
position: absolute; top: -2px; left: -2px; z-index: 20;

em: transform rotate(-45deg); font-size 13px; font-family Renner*;
    color #fff; letter-spacing .25em; text-shadow 0 1px 3px rgba(34,34,34,0.1);
```

### 7.10 Footer (`.site-footer`)

```
background: #fff; color: #4ab134; z-index: 20;
.wrap: display flex; padding 3rem 0;
cols-left: width 60%; cols-right: width 40%;
```

**フッターロゴ:** SVG `380×30px` / fill `#4ab134` / hover opacity 0.8

**SNS アイコン (`.footer-sns a`):**
```css
width: 45px; height: 45px; border-radius: 50%;
svg: 26×26px; fill #4ab134;
hover: background #4ab134; svg fill #fff;
```

**フッターリンク (`.footer-links`):**
```
border-left: solid 3px #fff;
a hover: color #DB7B00;
```

**タグリスト (`.footer-tag-list a:not(.link-all)):**
```css
border: solid 1px #fff; border-radius: 30px;
font-size: 12px; letter-spacing: .18em;
::before: content '#';
hover: border-color #DB7B00; color #DB7B00;
```

### 7.11 ページトップボタン (`#btn-scroll`)

```css
width: 6em; height: 6em; border-radius: 50%;
background: #3E352E; opacity: .8;
position: fixed; right: 2em; bottom: -20em;  /* 初期: 非表示 */
.btn-fade: bottom 2em;  /* 表示状態 */
```

---

## 8. Animations & Transitions

### グローバル transition

```css
a, img, button, input, textarea, #hamburger, #hamburger span,
#header-logo, .nav-top svg, .btn-insta svg, .btn-more:after,
.usecase-list svg, .footer-sns svg, #footer-menu a svg,
#btn-scroll, .entry-meta svg, .btn-top svg {
  transition: .3s;
}
```

### ヒーロースライドショー

```css
@keyframes mainImg {
  0%   { transform: scale(1, 1); }
  100% { transform: scale(1.2, 1.2); }
}
/* duration: 5s  easing: ease  delay: 0.5s  iteration: 1  fill-mode: both */
/* JS でスライド切り替え、.slide-active クラスで発火 */
```

### スクロール出現アニメーション

```css
/* 初期状態 */
.elm-fadeup {
  opacity: 0;
  transform: translateY(50px);
  transition: all 1s;
}
/* 発火状態（JS で付与） */
.fadein-up {
  opacity: 1;
  transform: translateY(0);
}
```

### サムネイルホバー

```css
/* 画像ズーム */
figure: transform scale(1.05) opacity .9;  duration .3s

/* オーバーレイ文字（::after） */
content: 'READ MORE';  /* Instafeed は 'VIEW MORE' */
```

### サイドナビ開閉

```css
/* 開く */
#side-navigation { right: 0; transition: .3s; }
body { margin-left: -300px; transition: .3s; }

/* 閉じる */
#side-navigation { right: -300px; }
body { margin-left: 0; }
```

---

## 9. Page Layout Structure

```
┌─────────────────────────────────────┐
│ HERO (#featured-area)               │  100vh, position: fixed, z-index 20
│  左: ロゴ画像 (46%)                  │  bg: #4ab134
│  右: スライドショー (48%)            │  + rgba(255,255,255,0.20) overlay
├─────────────────────────────────────┤
│ MESSAGE (#sec-message)              │  100vh, position: relative, z-index 30
│  margin-top: 100vh (Heroの下に配置)  │  bg: white + 画像
│  ロゴSVG / 本文 / CTA               │
├─────────────────────────────────────┤
│ SCHEDULE (#sec-schedule)            │  min-height 100vh, z-index 30
│  イベントカード一覧                  │  bg: #e6f7e3
│  （30%画像 + 70%詳細）              │
├─────────────────────────────────────┤
│ NEWS (#sec-news)                    │  z-index 30
│  リスト形式ニュース                  │  bg: #ffffff
├─────────────────────────────────────┤
│ GALLERY (#sec-gallery)              │  z-index 30
│  Instagram フィード                  │  bg: #EBEBEC
├─────────────────────────────────────┤
│ FOOTER (.site-footer)               │  z-index 20
│  左60%: ロゴ + 説明 / 右40%: SNS+リンク │  bg: #ffffff
└─────────────────────────────────────┘
```

**z-index スタック:**
```
ページトップボタン: 60
サイドナビ: 90
ハンバーガー: 80
メインヘッダー: 85
スライドオーバーレイ: 30
スライドアクティブ: 25
スライドリスト: 25
スライド背景ロゴ: 25
ヒーローロゴ: 40
hero section: 20
コンテンツセクション: 30
フッター: 20
```

---

## 10. Grid & Breakpoints

### コンテンツ最大幅

| 要素 | Max-width |
|------|-----------|
| `.wrap` | `700px` |
| `#content-inner` | `900px` |
| `#recommend-area > div` | `900px` |
| Instagram 各アイテム | `240px` (desktop) / `154px` (mobile) |

### レスポンシブブレークポイント

```
単一ブレークポイント: max-width: 798px
```

| 要素 | Desktop | Mobile |
|------|---------|--------|
| `#featured-area` | `position: fixed` | `position: relative` |
| ロゴ画像 | `width: 46%, height: 85vh` | `width: 80%, height: 50vh` |
| スライドショー | `width: 48%` | `width: 100%, height: 50vh` |
| section padding-bottom | `10rem` | `4rem` |
| section h3 (見出し) | `92px` | `30px` |
| `.wrap` padding | `0 2em` | `0 1.8em` |
| Schedule card padding | `3rem 0` | `1.5rem` |
| Schedule event-detail | `display: flex` | `display: block` |
| Schedule event left | `width: 30%` | `width: 100%` |
| Schedule event right | `width: 70%` | `width: 100%` |
| footer .wrap | `display: flex` | `display: block` |
| footer cols-left/right | `60% / 40%` | `100%` |
| .footer-links / tag-list | `inline-block` | `display: block, width: 100%` |
| Instafeed item | `240px` | `45%, max-width 154px` |
| Instafeed thumb | `240px` | `154px` |
| btn-more | `font-size: 20px` | `width: 100%, font-size: 14px` |
| #btn-scroll | `right: 2em` | `right: 1em` |

---

## 11. Interaction States

| 要素 | 状態 | 変化 |
|------|------|------|
| nav links | hover | `opacity: 0.7` |
| `.btn-link` | hover | `background #4ab134; color #fff; ::after right 1.5rem` |
| `.btn-more` | hover | `background #4ab134; color #fff; ::after right 1.2em` |
| `.btn-insta` | hover | `border-color #DB7B00; color #DB7B00; svg fill #DB7B00` |
| Schedule card title | hover | `opacity: 0.8` |
| Schedule category | hover | `opacity: 0.8` |
| Schedule "READ MORE" | hover | `opacity: 0.8; ::after right .5rem` |
| News list `a` | hover | `color: #4ab134` |
| Post thumbnail | hover | `scale(1.05) opacity .9 + "READ MORE" overlay` |
| Instafeed thumb | hover | `scale(1.1) opacity .9 + "VIEW MORE" overlay` |
| Instafeed follow-area | hover | `background #4ab134; span/svg: white; span: scale(1.1)` |
| footer SNS icon | hover | `background #4ab134; svg fill #fff` |
| footer links | hover | `color: #DB7B00` |
| footer tag | hover | `border-color #DB7B00; color #DB7B00` |
| `#btn-scroll` | hover | `opacity: 1` |
| article tag | hover | `border-color #4ab134; color #4ab134` |
| `input:focus` | focus | `border-color: #DB7B00` |

---

## 12. Voice & Tone (Copy Patterns)

| パターン | 例 |
|---------|---|
| タグライン | `健康で持続可能なライフスタイルを考えよう` |
| イベント分類 | `オーガニック＆ナチュラルマルシェ` / `ワークショップ` |
| 地名見出し | 都市名のみ（東京・奈良・名古屋・広島・京都） |
| 終了表示 | `終了しました`（グレーアウト + コーナーリボン） |
| CTA | `READ MESSAGE` / `READ MORE` / `VIEW MORE` |
| nav ラベル | 英語大文字 `HOME` / `MESSAGE` / `NEWS` / `CONTACT` |
| フッタータグ | `#オーガニック` `#ナチュラル` `#マルシェ` など `#` プレフィックス付き |
