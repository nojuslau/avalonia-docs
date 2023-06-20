---
description: REFERENCE - Styles
---

# Pseudo Classes

Pseudo classes are generated by a control, usually as a response to some sort of state.

For example `:pointerover` pseudo class indicates that the pointer input is currently over (inside the bounds of) a control. &#x20;

Pseudo classes are not set in the `Classes` attributes of a control (unlike style classes).

Common pseudo classes include:

&#x20;`:focus`, `:disabled`, `:pressed` for buttons, and `:checked` for checkboxes.

A control can have more than one pseudo class active at a time.

You can target one or more pseudo classes in a style selector.  For example:

```
<Style Selector="Button.red:focus:pointover">
```

This selector targets button controls with the red class set, and that are in the `:focus` and the `:pointover` pseudo class state.

Some common pseudo classes:

<table><thead><tr><th width="187">Pseudo Class</th><th>Description</th></tr></thead><tbody><tr><td><code>:pointerover</code></td><td>The pointer input is currently over (inside the bounds of) a control</td></tr><tr><td><code>:focus</code></td><td>A control has the input focus.</td></tr><tr><td><code>:disabled</code></td><td>A control is unable to respond to user interaction.</td></tr><tr><td><code>:pressed</code></td><td>A button control is in the down position.</td></tr><tr><td><code>:checked</code></td><td>A checkbox control is selected (check mark is showing).</td></tr></tbody></table>

### Custom Pseudo Classes <a href="#custom-pseudoclasses" id="custom-pseudoclasses"></a>

You can create your own pseudo classes for custom controls based on `CustomControl` or `TemplatedControl`. The function below adds or remove a pseudo class depending on a Boolean value on a `StyledElement`.

```csharp
PseudoClasses.Set(":className", bool);
```