# Gavis

Inside any component, you can define events and trigger. In the example below, the event `{category: "News", action: "expose", label: "morning", data: {viewCount, commentCount}}` is sent by logger function defined in the previous section on component's mount.

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
