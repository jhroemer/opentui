# Docs

- [Components](#components)
  - [`<text>`](#text)
  - [`<box>`](#box)
  - [`<span>`](#span)
  - [`<input>`](#input)
  - [`<select>`](#select)
  - [`<tab_select>`](#tab_select)
  - [`<ASCIIFont>`](#asciifont)
  - [`<scrollbox>`](#scrollbox)
  - [`<code>`](#code)
  - [`<textarea>`](#textarea)
  - [`<b>`](#b)
  - [`<strong>`](#strong)
  - [`<i>`](#i)
  - [`<em>`](#em)
  - [`<u>`](#u)
  - [`<br>`](#br)
  - [`<a>`](#a)

## Components

### `text`

A simple text component for rendering text,

<details>
<summary>Example</summary>

```jsx
<text>Hello world</text>
```

</details>

### `box`

Layout component useful for grouping and rendering content.
Supports flex-box properties for laying out its content.

<details>
<summary>Example</summary>

```jsx
<box title="My Box" border>
  <text>Content inside a box</text>
</box>
```

</details>

### `span`

In-line layout component.

<details>
<summary>Example</summary>

<!-- TODO improve -->

```jsx
<span>I'm a span</span>
```

</details>

### `input`

Element for capturing user input.
Has to be focused to capture user input.

<details>
<summary>Example</summary>

```jsx
<input placeholder="Enter your name..." onSubmit={(value) => console.log(value)} focused />
```

</details>

### `select`

Basic select component that lets you select an option out of a list of options.
Has to be focused to capture user input.
The list is navigated with up/down or k/j.

<details>
<summary>Example</summary>

```jsx
<select
  options={[
    { label: "Option 1", value: "1" },
    { label: "Option 2", value: "2" },
  ]}
  onSelect={(index, option) => console.log(option)}
  focused
/>
```

</details>

### `tab_select`

Component for rendering selectable tabs.
Tabs are rendered horizontally by default.

 <!-- double-check this -->

Use tab to cycle between tabs.

<details>
<summary>Example</summary>

```jsx
<tab_select
  options={[{ label: "Tab 1" }, { label: "Tab 2" }, { label: "Tab 3" }]}
  onChange={(index) => setActiveTab(index)}
  focused
/>
```

</details>

### `ASCIIFont`

<!-- TODO -->

<details>
<summary>Example</summary>

```jsx
<ASCIIFont text="Hello" />
```

</details>

### `scrollbox`

<!-- TODO -->

<details>
<summary>Example</summary>

```jsx
<scrollbox style={{ width: "100%", height: "100%" }} focused>
  <For each={items()}>{(item) => <text>{item.name}</text>}</For>
</scrollbox>
```

</details>

### `code`

<!-- TODO -->

<details>
<summary>Example</summary>

```jsx
<code
  content={`function hello() {
  return "world"
}`}
  filetype="javascript"
/>
```

</details>

### `textarea`

<!-- TODO -->

<details>
<summary>Example</summary>

```jsx
<textarea initialValue="Edit me!" placeholder="Enter text here..." wrapMode="word" showCursor focused />
```

</details>

### `b`

<!-- TODO -->

<details>
<summary>Example</summary>

```jsx
<text>
  This is <b>bold</b> text
</text>
```

</details>

### `strong`

<!-- TODO -->

<details>
<summary>Example</summary>

```jsx
<text>
  This is <strong>strong</strong> text
</text>
```

</details>

### `i`

<!-- TODO -->

<details>
<summary>Example</summary>

```jsx
<text>
  This is <i>italic</i> text
</text>
```

</details>

### `em`

<!-- TODO -->

<details>
<summary>Example</summary>

```jsx
<text>
  This is <em>emphasized</em> text
</text>
```

</details>

### `u`

<!-- TODO -->

<details>
<summary>Example</summary>

```jsx
<text>
  This is <u>underlined</u> text
</text>
```

</details>

### `br`

<!-- TODO -->

<details>
<summary>Example</summary>

```jsx
<text>
  Line one
  <br />
  Line two
</text>
```

</details>

### `a`

<!-- TODO -->

<details>
<summary>Example</summary>

```jsx
<text>
  Visit{" "}
  <a href="https://opentui.com" style={{ fg: "blue" }}>
    opentui.com
  </a>
</text>
```

</details>

## Next steps

Go check out some of the more advanced components in [examples](../examples).
