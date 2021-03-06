---
layout: "v2_fluid/docs_base"
version: "2.0.0-alpha.42"
versionHref: "/docs/v2/2.0.0-alpha.42"
path: ""
category: api
id: "{{Modal | slugify}}"
title: "Modal"
header_sub_title: "Class in module "
doc: "Modal"
docType: "class"
show_preview_device: true
preview_device_url: "/docs/v2/demos/modal/"
angular_controller: APIDemoCtrl 
---




<div class="improve-docs">
<a href='http://github.com/driftyco/ionic2/tree/master/ionic/components/modal/modal.ts#L5'>
View Source
</a>
&nbsp;
<a href='http://github.com/driftyco/ionic2/edit/master/ionic/components/modal/modal.ts#L5'>
Improve this doc
</a>
</div>





<h1 class="api-title">


Modal






</h1>






<!-- description -->
<h2>Description</h2>

<p>The Modal is a content pane that can go over the user&#39;s current page.
Usually used for making a choice or editing an item. A modal can be opened
similar to how NavController#push works, where it is passed a Page component,
along with optional Page params, and options for presenting the modal.</p>

<!-- @usage tag -->

<h2>Usage</h2>

<pre><code class="lang-ts">class MyApp {

 constructor(modal: Modal) {
   this.modal = modal;
 }

 openContactModal() {
   this.modal.open(ContactUs);
 }

 openProfileModal() {
   this.modal.open(Profile, { userId: 8675309 }, {
     enterAnimation: &#39;my-fade-in&#39;,
     leaveAnimation: &#39;my-fade-out&#39;,
     handle: &#39;profile-modal&#39;
   });
 }

}
</code></pre>




<!-- @property tags -->


<!-- methods on the class -->

<h2>Methods</h2>

<div id="open"></div>

<h3>
<code>open(pageComponent,&nbsp;params,&nbsp;opts)</code>
  

</h3>

Opens a new modal using the page component is was pass as the first
argument. This is similar to how NavController's `push` method works.
Currently you must have `<ion-overlay>` in the @App component's template
for the modal to work correctly. (This is something that will
be hopefully be removed in the near future.)


<table class="table" style="margin:0;">
  <thead>
    <tr>
      <th>Param</th>
      <th>Type</th>
      <th>Details</th>
    </tr>
  </thead>
  <tbody>
    
    <tr>
      <td>
        pageComponent
        
        
      </td>
      <td>
        
  
      </td>
      <td>
        <p>The Page component to load in the modal.</p>

        
      </td>
    </tr>
    
    <tr>
      <td>
        params
        
        
      </td>
      <td>
        
  <code>Object</code>
      </td>
      <td>
        <p>Optional data which can be passed to the page
component, which can be read from the constructor&#39;s <code>NavParams</code>.</p>

        
      </td>
    </tr>
    
    <tr>
      <td>
        opts
        
        
      </td>
      <td>
        
  <code>Object</code>
      </td>
      <td>
        <p>Additional options for this one modal instance of.
Options include <code>enterAnimation</code> and <code>leaveAnimation</code>, which
allows customization of which animation to use.</p>

        
      </td>
    </tr>
    
  </tbody>
</table>





* Returns: 
  <code>Promise</code> Returns a promise which resolves when the modal has
loaded and its entering animation has completed. The resolved promise's
value is the instance of the newly created modal.




<div id="get"></div>

<h3>
<code>get(handle)</code>
  

</h3>

Get the instance of a modal. This is usually helpful to getting ahold of a
certain modal, from anywhere within the app, and closing it. By calling
just `get()` without a `handle` argument, it'll return the active modal
on top (it is possible to have multipe modals opened at the same time).
If getting just the active modal isn't enough, when creating
a modal, it's options can be given a `handle`, which is simply a string-based
name for the modal instance. You can later get a reference to that modal's
instance by calling this method with the same handle name.


<table class="table" style="margin:0;">
  <thead>
    <tr>
      <th>Param</th>
      <th>Type</th>
      <th>Details</th>
    </tr>
  </thead>
  <tbody>
    
    <tr>
      <td>
        handle
        
        
      </td>
      <td>
        
  
      </td>
      <td>
        <p>Optional string name given in the modal&#39;s options when it was opened.</p>

        
      </td>
    </tr>
    
  </tbody>
</table>





* Returns: 
   Returns the instance of the modal if it is found, otherwise `null`.




<!-- related link -->

<h2>Related</h2>

<a href='/docs/v2/components#modals'>Modal Component Docs</a><!-- end content block -->


<!-- end body block -->

