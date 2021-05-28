# Context Shadowing

Context shadowing for events is a key concept of Gavis.

With Context shadowing, you can override the event context easily.

```jsx
function Page() {
  return (
    <Gavis category="page" action="page_view" logOnMount>
      <Article index={0} />
      <Gavis action="article1_view">
        <Article index={1} />
      </Gavis>
      <Gavis action="article2_view" label="last">
        <Article index={2} />
      </Gavis>
    </Gavis>
  );
}

function Article({ index }) {
  return (
    <Gavis data={{ index }} logOnMount>
      <p>hello world {index}</p>
    </Gavis>
  );
}
```

In the example above, there will be 4 events sent to the server.

1. `{category: "page", action: "page_view"}` sent on Page mount
2. `{category: "page", action: "page_view" data: {index: 0}}` sent on Article mount
3. `{category: "page", action: "article1_view" data: {index: 1}}` sent on Article mount
4. `{category: "page", action: "article2_view" label:"last" data: {index: 2}}` sent on Article mount
