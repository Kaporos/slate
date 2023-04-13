# Slate Component

## `Slate(prop: SlateProps)`

The `Slate` component must include somewhere in its `children` the `Editable` component.

```typescript
type SlateProps = {
  editor: ReactEditor
  value: Descendant[]
  children: React.ReactNode
  onChange?: (value: Descendant[]) => void
}
```

### Slate Props

#### `props.editor: ReactEditor`

An instance of `ReactEditor`

#### `props.value: Descendant[]`

The initial value of the Editor.

This prop is deceptively named.

Slate once was a controlled component (i.e. it's contents were strictly controlled by the `value` prop) but due to features like its edit history which would be corrupted by direct editing of the `value` it is no longer a controlled component.

#### `children: React.ReactNode`

The `children` which must contain an `Editable` component.

#### `onChange: (value: Descendant[]) => void`

An optional callback function which you can use to be notified of changes in the editor's value.