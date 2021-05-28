# Configuration

First, you need to wrap the root component with `GavisConfig` and define `logger` function. The `logger` function is the actual function that receives log `event` from components and makes requests to the server.

```jsx
//App.tsx
import { GavisConfig } from "gavis";

const logger = (category: string, action: string, label: string, data: any) => {
  const value = data.viewCount;
  ga(category, action, label, value);
};

function App() {
  return (
    <GavisConfig logger={logger}>
      <Page />
    </GavisConfig>
  );
}
```

> The word 'event' in this document means any object with category, action, label(optional) and data(optional) which is sent to the server.
