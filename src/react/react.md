[
  id: react-expand-props
  tags:
  locations:
]: #

# Expand properties

When you have several elements requiring the same properties, you can bundle them and use them like this.

````jsx
const props = {
  className: 'class-name',
  href: '#',
  onClick: () => {},
}

return <>
  <div {...props}></div>
  <div {...props}></div>
  <div {...props}></div>
</>;
````
