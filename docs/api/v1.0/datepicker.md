---
title: 'Date Picker'
sidebarDepth: 2
---

::: tip
`v-date-picker` supports all props, events and slots that are supported by `v-calendar` in addition to those listed below.
:::


## Props

### `is-inline`

**Type:** Boolean

**Description:** Displays the calendar picker only (not as a popover).

**Default:** `false`

:::danger
**`is-inline` deprecated in [`v2.0`](../v2.0)**
:::

### `mode`

**Type:** String

**Description:** Selection mode: `"single"`, `"multiple"`, `"range"`

**Default Value:** `"single"`

:::warning
**`mode` modified in [`v2.0`](../v2.0)**
:::

### `value`

**Type:** Date, Array[Date], Object

**Description:** Selected date, dates or date range.

**Default Value:** `null`

:::warning
**`value` modified in [`v2.0`](../v2.0)**
:::

### `is-required`

**Type:** Boolean

**Description:** Prevents the **user** from clearing the selected value.

**Default Value:** `false`

::: tip
Setting `value = null` still allowed through code.
:::

### `input-props`

**Type:** Object

**Description:** Props to apply to the input DOM element.

**Default Value:** [Reference code]()

:::danger
**`input-props` deprecated in [`v2.0`](../v2.0)**
:::

### `update-on-input`

**Type:** Boolean

**Description:** Update the picker value after every `input` event. Otherwise, value is just updated on `change` event.

**Default Value:** `true`

### `input-debounce`

**Type:** Number

**Description:** If `update-on-input` is enabled, the duration in milliseconds at which the `input` event is debounced before updating the date value.

**Default Value:** `1000`

### `drag-attribute`

**Type:** Object

**Description:** Attribute to use for the dragged selection in "range" mode. The `dates` property is ignored.

**Default Value:** [Reference code]()

### `select-attribute`

**Type:** Object

**Description:** Attribute to use for the value selection in all modes. The `dates` property is ignored.

**Default Value:** [Reference code]()

### `popover`

**Type:** Object

**Description:** Properties of the popover to apply for the calendar component.

**Default Value:** [Reference code](./defaults.md)

| Property | Type | Description |
| --- | --- | --- |
| `visibility` | String | Visibility mode for the input/slot popover (`"hover-focus"`, `"hover"`, `"focus"`, `"visible"`, `"hidden"`) |
| `placement` | String | Default or suggested placement of the popover. This may change as the browser window dimensions change. [Valid placements](https://popper.js.org/docs/v2/constructors/#placement) include `auto`, `top`, `right`, `bottom`, `left`. Each placement can have suffixed variations `-start` or `-end`. |
| `positionFixed` | Boolean | Display the popover in `fixed` mode. Reference [`popper.js`](https://popper.js.org/docs/v2/constructors/#strategy) for more details. |
| `modifiers` | Array | Modifiers used to modify the behavior of [`popper.js`](https://popper.js.org/docs/v2/modifiers). |
| `keepVisibleOnInput` | Boolean | Keep the popover visible after a date is selected, until the `visibility` determines. |

<!-- 
### 

**Type:** 

**Description:** 

**Default Value:** 
-->

## Events

### `input`

**Description:** New date was selected.

**Params:** `value: Date, Array[Date], Object`

### `drag`

**Description:** Dragged selection was updated. Only valid when `mode === "range"`

**Params:** `range: Object`

### `popoverWillShow`

**Description:** Called just before picker popover transitions into view

**Params:** `Object`: Popover content root HTML element.

### `popoverDidShow`

**Description:** Called just after picker popover has transitioned into view

**Params:** `Object`: Popover content root HTML element.

### `popoverWillHide`

**Description:** Called just before picker popover transitions out of view

**Params:** `Object`: Popover content root HTML element.

### `popoverDidHide`

**Description:** Called just after picker popover has transitioned out of view

**Params:** `Object`: Popover content root HTML element.

<!-- 
### 

**Description:** 

**Params:** 
-->

## Scoped Slots

### *`default`*

**Description:** Default slot to use as the popover anchor for v-date-picker. <sup>[[1]](#dp-slots-note-1)</sup> Not applicable to inline date pickers.

**Props:**

Reference the section on using [custom slots](../datepicker.md#use-custom-slot) for available props.
