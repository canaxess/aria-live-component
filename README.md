# aria live component
The WCAG 2.1 status message component hides the complexity of how to render an aria live region. Optional parameters give developers flexibility to create a customised aria live region or use 1 of 3 [WCAG 2.1 status messages](https://www.w3.org/WAI/WCAG21/Understanding/status-messages.html) values **status, log, alert**.

## React usage
* The `isCustomLiveRegion` parameter allows all aria attributes to be independently set

`<AlertComponent isCustomLiveRegion={true} ariaLive="polite" ariaAtomic={false} ariaRelevant="additions" message={this.state.error}/>`

* The `messageType` parameter accepts one of 3 defined roles **status, log, alert**

`<AlertComponent messageType="alert" message={this.state.error}/>`
