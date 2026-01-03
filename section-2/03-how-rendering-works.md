# Rendering Works

1. Render is Triggered
   The two situation that trigger renders
   - Intial render of the aplication
   - State is updated in one more componenet instances (re- render)

- Render process is triggerd for the entire application
- in pratice, it looks liaje react only re-renders the components wheere the sate update happens, but thats not how it works behind the scenes
- rander are not triggerd immediately, but scheduled for when the js engine has some "fre tim". Ther is also batching of multiaple setSatet calls in event handlers

[Next: Rendering phase](./04-render-phase.md)
