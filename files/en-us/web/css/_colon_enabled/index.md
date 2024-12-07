---
title: ":enabled"
slug: Web/CSS/:enabled
page-type: css-pseudo-class
browser-compat: css.selectors.enabled
---

{{CSSRef}}

The **`:enabled`** [CSS](/en-US/docs/Web/CSS) [pseudo-class](/en-US/docs/Web/CSS/Pseudo-classes) represents any enabled element. An element is enabled if it can be activated (selected, clicked on, typed into, etc.) or accept focus. The element also has a disabled state, in which it can't be activated or accept focus.

{{EmbedInteractiveExample("pages/tabbed/pseudo-class-enabled.html", "tabbed-standard")}}

## Syntax

```plain
:enabled
```

## Examples

The following example makes the color of text and button {{htmlElement("input")}}s green when enabled, and gray when disabled. This helps the user understand which elements can be interacted with.

### HTML

```html
<form action="url_of_form">
  <label
    >First field (enabled):
    <input type="text" value="Lorem" /> </label
  ><br />

  <label
    >Second field (disabled):
    <input type="text" value="Ipsum" disabled /> </label
  ><br />

  <input type="button" value="Submit" />
</form>
```

### CSS

```css
input:enabled {
  color: #2b2;
}

input:disabled {
  color: #aaa;
}
```

### Result

{{EmbedLiveSample("Examples", 550, 95)}}

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{Cssxref(":disabled")}}
