# useGavis

Sometimes you may want to send event imperatively. For example, the Button component below sends event on click.

```jsx
import { useGavis } from "gavis";

function Button() {
  const log = useGavis();
  return (
    <Gavis category="News" action="expose" label="morning">
      <button onClick={() => log({ action: "click" })}>LOG</button>;
    </Gavis>
  );
}
```

## Supported events(WIP)

- click
