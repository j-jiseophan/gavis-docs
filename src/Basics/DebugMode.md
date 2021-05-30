# Debug mode

Gavis supports debug mode to help you test whether logs contain correct data.
If debug mode is enabled, the debugger component will be show in the screen as below.

<img src="../resources/DebugMode.png" alt="screenshot" width="400" style="margin: 10px 0; border: 1px solid black"/>

To enable debug mode, all you need to do is passing `debug` prop to `<GavisConfig/>`

```jsx
<GavisConfig logger={logger} debug={process.env.APPLICATON_STAGE === "LOCAL"}>
```
