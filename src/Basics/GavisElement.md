# 〈GavisElement/〉

`<Gavis/>` component is basically a context provider. It does not create a DOM element. However, many events such as click, keydown and intersection need a real DOM element to be catched. Using `<GavisElement>` you can create any kind of element with the functionality of `<Gavis/>`.

```jsx
import { Gavis } from "gavis";

function Page() {
  return (
    <div>
      <p>hello world</p>​
      <GavisElement
        type="div"
        className="message-black"
        category="News"
        action="expose"
        label="morning"
        data={{ viewCount, commentCount }}
        logOnMount
      >
        Hello
      </GavisElement>
      </Gavis>
    </div>
  );
}
```

In the example above, the `<GavisElement/>` creates `<div/>` element with className "message-black" wrapping 'Hello'. The Element will send log on mount.

## Supported events(WIP)

- mount
- unmount
- click
- firstObserve(using IntersectionObserver)
