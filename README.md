## Alerting the user audibly
Audible hints can be provided to screen reader users through an accessibility technique called a live region used to indicate the status of the change audibly to the screen reader. When content is added to it, the new content is communicated through to the screen reader which announces it so it’s a very convenient way to alert the user that something has changed in a non-visual way.

**Use the [WCAG 2.1 live region roles](https://www.w3.org/WAI/WCAG21/Understanding/status-messages.html) for defined message types**
Role | Urgency | What is announced?
--- | --- | ---
`role="log"` | Polite | New Content
`role="status"` | Polite | Old & New Content
`role="alert"` | Assertive | New Content

## Reusable Components
Creating reusable components makes the design consistently repeatable. A component can be created which has a range of parameters that can be set when developing, developers aren’t having to directly code the attributes they're simply setting what type of message to display.

Taking the responsibility away from the developer to have to worry and think about these sorts of things means a stronger likelihood accessibility is being maintained and is being implemented consistently.

## React usage
The `isCustomLiveRegion` parameter allows all aria attributes to be independently set

```html
<AlertComponent isCustomLiveRegion={true} ariaLive="polite" ariaAtomic={false} ariaRelevant="additions" 
message={this.state.error}/>
```

The `messageType` parameter accepts one of 3 defined roles **status, log, alert**

```html
<AlertComponent messageType="alert" message={this.state.error}/>
```
