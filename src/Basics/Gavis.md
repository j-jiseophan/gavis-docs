# 〈Gavis/〉

With `<Gavis/>` you can define logger contexts and triggers in a declarative way. `<Gavis/>` works as a Context Provider for their descendents. In the example below, The value `{category: "News", action: "expose", label: "morning", data: {viewCount, commentCount}}` is sent by logger function defined in the previous section on component's mount.

```jsx
import { Gavis } from "gavis";

function Page() {
  return (
    <div>
      <p>hello world</p>​
      <Gavis
        category="News"
        action="expose"
        label="morning"
        data={{ viewCount, commentCount }}
        logOnMount
      >
        <div>message</div>
        <Button />
      </Gavis>
    </div>
  );
}
```

## Supported events(WIP)

- mount
