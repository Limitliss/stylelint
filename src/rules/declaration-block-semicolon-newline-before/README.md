# declaration-block-semicolon-newline-before

Require or disallow a newline before the semicolons of declaration blocks.

```css
    a {
      color: pink
      ; top: 0;
    } ↑
/**   ↑
 * The newline before this semicolon */
```

## Options

`string`: `"always"|"never"|"always-multi-line"|"never-multi-line"`

### `"always"`

There *must always* be a single newline before the semicolons.

The following patterns are considered warnings:

```css
a { color: pink; }
```

```css
a {
  color: pink; top: 0;
}
```

The following patterns are *not* considered warnings:

```css
a { color: pink
; }
```

```css
a {
  color: pink
  ; top: 0;
}
```

### `"never"`

There *must never* be whitespace before the semicolons.

The following patterns are considered warnings:

```css
a { color: pink
; }
```

```css
a {
  color: pink
  ; top: 0;
}
```

The following patterns are *not* considered warnings:

```css
a { color: pink; }
```

```css
a {
  color: pink; top: 0;
}
```

### `"always-multi-line"`

There *must always* be a single newline before the semicolons in multi-line rules.

The following patterns are considered warnings:

```css
a {
  color: pink; top: 0;
}
```

The following patterns are *not* considered warnings:

```css
a { color: pink; }
```

```css
a { color: pink; top: 0; }
```

```css
a {
  color: pink
  ; top: 0;
}
```

### `"never-multi-line"`

There *must never* be whitespace before the semicolons in multi-line rules.

The following patterns are considered warnings:

```css
a {
  color: pink
  ; top: 0;
}
```

The following patterns are *not* considered warnings:

```css
a { color: pink; }
```

```css
a { color: pink; top: 0; }
```

```css
a {
  color: pink;
  top: 0;
}
```