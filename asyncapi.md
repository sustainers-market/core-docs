# Core | Sustainer&#39;s Market 1.0.0 documentation



The core services for the Sustainer's Market.

### Check out its awesome features:

* Turn a specific streetlight on/off
* Receive real-time information about environmental lighting conditions


## Table of Contents



* [Servers](#servers)


* [Channels](#channels)





<a name="servers"></a>
## Servers

<table>
  <thead>
    <tr>
      <th>URL</th>
      <th>Protocol</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
  <tr>
      <td>core.sustainers.market</td>
      <td>https</td>
      <td>Production server</td>
    </tr>
    <tr>
      <td colspan="3">
        <details>
          <summary>URL Variables</summary>
          <table>
            <thead>
              <tr>
                <th>Name</th>
                <th>Default value</th>
                <th>Possible values</th>
                <th>Description</th>
              </tr>
            </thead>
            <tbody>
              </tbody>
          </table>
        </details>
      </td>
    </tr>
    <tr>
      <td colspan="3">
        <details>
          <summary>Security Requirements</summary>
          <table>
            <thead>
              <tr>
                <th>Type</th>
                <th>In</th>
                <th>Name</th>
                <th>Scheme</th>
                <th>Format</th>
                <th>Description</th>
              </tr>
            </thead>
            <tbody><tr>
                <td>apiKey</td>
                <td>user</td>
                <td></td>
                <td></td>
                <td></td>
                <td><p>Provide your API key as the user and leave the password empty.</p>
</td>
              </tr><tr>
                <td>oauth2</td>
                <td></td>
                <td></td>
                <td></td>
                <td></td>
                <td><p>Flows to support OAuth 2.0</p>
</td>
              </tr></tbody>
          </table>
        </details>
      </td>
    </tr>
    </tbody>
</table>






## Channels



<a name="channel-create.auth-token"></a>





#### Channel Parameters







###  `subscribe` create.auth-token

#### Message



Inform about environmental lighting conditions for a particular streetlight.







##### Payload




<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
    
      
<tr>
  <td>lumens </td>
  <td>
    integer</td>
  <td><p>Light intensity measured in lumens.</p>
</td>
  <td><em>Any</em></td>
</tr>






    
      
<tr>
  <td>sentAt </td>
  <td>
    string</td>
  <td><p>Date and time when the message was sent.</p>
</td>
  <td><em>Any</em></td>
</tr>






    
  </tbody>
</table>



###### Example of payload _(generated)_

```json
{
  "lumens": 0,
  "sentAt": "2019-09-02T21:07:39Z"
}
```








<a name="channel-edit.auth-token"></a>





#### Channel Parameters



##### 0


The ID of the streetlight.



<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
    
      
<tr>
  <td>0 </td>
  <td>
    string</td>
  <td></td>
  <td><em>Any</em></td>
</tr>






    
  </tbody>
</table>





###  `publish` edit.auth-token

#### Message



Command a particular streetlight to turn the lights on or off.







##### Payload




<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
    
      
<tr>
  <td>command </td>
  <td>
    string</td>
  <td><p>Whether to turn on or off the light.</p>
</td>
  <td><code>on</code>, <code>off</code></td>
</tr>






    
      
<tr>
  <td>sentAt </td>
  <td>
    string</td>
  <td><p>Date and time when the message was sent.</p>
</td>
  <td><em>Any</em></td>
</tr>






    
  </tbody>
</table>



###### Example of payload _(generated)_

```json
{
  "command": "on",
  "sentAt": "2019-09-02T21:07:39Z"
}
```








<a name="channel-some-other.auth-token"></a>





#### Channel Parameters



##### 0


The ID of the streetlight.



<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
    
      
<tr>
  <td>0 </td>
  <td>
    string</td>
  <td></td>
  <td><em>Any</em></td>
</tr>






    
  </tbody>
</table>





###  `publish` some-other.auth-token

#### Message



Command a particular streetlight to turn the lights on or off.







##### Payload




<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
    
      
<tr>
  <td>command </td>
  <td>
    string</td>
  <td><p>Whether to turn on or off the light.</p>
</td>
  <td><code>on</code>, <code>off</code></td>
</tr>






    
      
<tr>
  <td>sentAt </td>
  <td>
    string</td>
  <td><p>Date and time when the message was sent.</p>
</td>
  <td><em>Any</em></td>
</tr>






    
  </tbody>
</table>



###### Example of payload _(generated)_

```json
{
  "command": "on",
  "sentAt": "2019-09-02T21:07:39Z"
}
```








<a name="channel-eat.auth-token"></a>





#### Channel Parameters



##### 0


The ID of the streetlight.



<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
    
      
<tr>
  <td>0 </td>
  <td>
    string</td>
  <td></td>
  <td><em>Any</em></td>
</tr>






    
  </tbody>
</table>





###  `publish` eat.auth-token

#### Message



Command a particular streetlight to dim the lights.







##### Payload




<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
    
      
<tr>
  <td>percentage </td>
  <td>
    integer</td>
  <td><p>Percentage to which the light should be dimmed to.</p>
</td>
  <td><em>Any</em></td>
</tr>






    
      
<tr>
  <td>sentAt </td>
  <td>
    string</td>
  <td><p>Date and time when the message was sent.</p>
</td>
  <td><em>Any</em></td>
</tr>






    
  </tbody>
</table>



###### Example of payload _(generated)_

```json
{
  "percentage": 0,
  "sentAt": "2019-09-02T21:07:39Z"
}
```










