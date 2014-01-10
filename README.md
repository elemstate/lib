elemstate-lib
===

elemstate-lib is a javascript library that uses a simple state machine model to set CSS classes on HTML elements.

The ESMCssRoot attribute is used to apply elemstate functionality to an element, as follows:

  <code>&lt;div esmCssRoot='hello'&gt;hello, i'm the hello tool&lt;/div&gt;</code>

CSS is declared for the applicable states for each root name (root_state), as follows:

<code>
  .hello {..}<br/>
  .hello_focused {..}<br/>
  .hello_toggled {..}<br/>
  .hello_waiting {..}<br/>
</code>

When a state is added or removed on an element (during an event or with a call to ESM.setState), the CSS class is changed to reflect the new combination.

Assuming all the above states are active on the hello element, statetools would set:

  <code>class = 'hello hello_focused hello_toggled hello_waiting'</code>

elemstate.js (in the gh_pages branch) contains more detailed doc.

<a href="http://elemstate.github.io/lib/elemstate/statetools_helloworld.html">Demo page</a>

An application that uses elemstate-lib:
<a href="http://thoughtwallet.github.io/wallet">ThoughtWallet</a>


