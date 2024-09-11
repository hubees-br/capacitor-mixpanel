<p align="center"><br><img src="https://user-images.githubusercontent.com/236501/85893648-1c92e880-b7a8-11ea-926d-95355b8175c7.png" width="128" height="128" /></p>
<h3 align="center">Capacitor Mixpanel</h3>
<p align="center"><strong><code>@houseninja/capacitor-mixpanel</code></strong></p>
<p align="center">
  Capacitor plugin for Mixpanel
</p>

<p align="center">
  <img src="https://img.shields.io/maintenance/yes/2023?style=flat-square" />
  <a href="https://www.npmjs.com/package/@houseninja/capacitor-mixpanel"><img src="https://img.shields.io/npm/l/@houseninja/capacitor-mixpanel?style=flat-square" /></a>
  <img src="https://img.shields.io/github/last-commit/houseninjadojo/capacitor-mixpanel?style=flat-square"></img>
<br>
  <a href="https://www.npmjs.com/package/@houseninja/capacitor-mixpanel"><img src="https://img.shields.io/npm/dw/@houseninja/capacitor-mixpanel?style=flat-square" /></a>
  <a href="https://www.npmjs.com/package/@houseninja/capacitor-mixpanel"><img src="https://img.shields.io/npm/v/@houseninja/capacitor-mixpanel?style=flat-square" /></a>
  <!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
<a href="#contributors"><img src="https://img.shields.io/badge/all%20contributors-4-orange?style=flat-square" /></a>
<!-- ALL-CONTRIBUTORS-BADGE:END -->
</p>

## Maintainers

| Maintainer      | GitHub                                              | Social                                    |
| --------------- | --------------------------------------------------- | ----------------------------------------- |
| Miles Zimmerman | [mileszim](https://github.com/mileszim)             | [@mileszim](https://twitter.com/mileszim) |
| House Ninja     | [houseninjadojo](https://github.com/houseninjadojo) |                                           |

## Install

```bash
npm install @houseninja/capacitor-mixpanel
```

Add the following plugin configuration:

```js
{
  ...
  "Mixpanel": {
    "token": "token-abcdefg1234",
    "trackAutomaticEvents": true, // optional, default: true
    "optOutTrackingByDefault": false, // optional, default: false
    "disableIosIpCollection": true, // optional, default: false
    "serverURL": "https://api-eu.mixpanel.com/", // optional, default: "https://api.mixpanel.com/"
  },
  ...
}
```

Sync capacitor configuration

```bash
npx cap sync
```

## API

<docgen-index>

* [`initialize(...)`](#initialize)
* [`distinctId()`](#distinctid)
* [`track(...)`](#track)
* [`identify(...)`](#identify)
* [`alias(...)`](#alias)
* [`reset()`](#reset)
* [`clearSuperProperties()`](#clearsuperproperties)
* [`currentSuperProperties()`](#currentsuperproperties)
* [`registerSuperProperties(...)`](#registersuperproperties)
* [`setProfile(...)`](#setprofile)
* [`setProfileUnion(...)`](#setprofileunion)
* [`deleteProfile()`](#deleteprofile)
* [`trackCharge(...)`](#trackcharge)
* [`flush()`](#flush)
* [`optInTracking(...)`](#optintracking)
* [`optOutTracking()`](#optouttracking)
* [`hasOptedOutTracking()`](#hasoptedouttracking)
* [Interfaces](#interfaces)

</docgen-index>

<docgen-api>
<!--Update the source file JSDoc comments and rerun docgen to update the docs below-->

### initialize(...)

```typescript
initialize(options: InitializeOptions) => any
```

Initialize the plugin (web only)

| Param         | Type                                                            |
| ------------- | --------------------------------------------------------------- |
| **`options`** | <code><a href="#initializeoptions">InitializeOptions</a></code> |

**Returns:** <code>any</code>

--------------------


### distinctId()

```typescript
distinctId() => any
```

Returns the current distinct id of the user. This is either the id automatically generated by the library or the id that has been passed by a call to identify().

**Returns:** <code>any</code>

--------------------


### track(...)

```typescript
track(options: TrackOptions) => any
```

Tracks an event with properties. Properties are optional and can be added only if needed.

| Param         | Type                                                  |
| ------------- | ----------------------------------------------------- |
| **`options`** | <code><a href="#trackoptions">TrackOptions</a></code> |

**Returns:** <code>any</code>

--------------------


### identify(...)

```typescript
identify(options: IdentifyOptions) => any
```

Identify a user with a unique ID to track user activity across devices, tie a user to their events, and create a user profile. If you never call this method, unique visitors are tracked using a UUID generated the first time they visit the site.

| Param         | Type                                                        |
| ------------- | ----------------------------------------------------------- |
| **`options`** | <code><a href="#identifyoptions">IdentifyOptions</a></code> |

**Returns:** <code>any</code>

--------------------


### alias(...)

```typescript
alias(options: AliasOptions) => any
```

The alias method creates an alias which Mixpanel will use to remap one id to another. Multiple aliases can point to the same identifier.

| Param         | Type                                                  |
| ------------- | ----------------------------------------------------- |
| **`options`** | <code><a href="#aliasoptions">AliasOptions</a></code> |

**Returns:** <code>any</code>

--------------------


### reset()

```typescript
reset() => any
```

Clears super properties and generates a new random distinct_id for this instance. Useful for clearing data when a user logs out.

**Returns:** <code>any</code>

--------------------


### clearSuperProperties()

```typescript
clearSuperProperties() => any
```

Clears all currently set super properties.

**Returns:** <code>any</code>

--------------------


### currentSuperProperties()

```typescript
currentSuperProperties() => any
```

Returns the currently set super properties.

**Returns:** <code>any</code>

--------------------


### registerSuperProperties(...)

```typescript
registerSuperProperties(options: SuperPropertyOptions) => any
```

Register super properties that will be sent with every event.

| Param         | Type                                                                  |
| ------------- | --------------------------------------------------------------------- |
| **`options`** | <code><a href="#superpropertyoptions">SuperPropertyOptions</a></code> |

**Returns:** <code>any</code>

--------------------


### setProfile(...)

```typescript
setProfile(options: ProfileProperties) => any
```

Set properties on the current user in Mixpanel People.

| Param         | Type                                                            |
| ------------- | --------------------------------------------------------------- |
| **`options`** | <code><a href="#profileproperties">ProfileProperties</a></code> |

**Returns:** <code>any</code>

--------------------


### setProfileUnion(...)

```typescript
setProfileUnion(options: ProfileProperties) => any
```

Union list properties.

| Param         | Type                                                            |
| ------------- | --------------------------------------------------------------- |
| **`options`** | <code><a href="#profileproperties">ProfileProperties</a></code> |

**Returns:** <code>any</code>

--------------------


### deleteProfile()

```typescript
deleteProfile() => any
```

Permanently deletes the current people analytics profile from Mixpanel (using the current distinctId).

**Returns:** <code>any</code>

--------------------


### trackCharge(...)

```typescript
trackCharge(options: ChargeOptions) => any
```

Track money spent by the current user for revenue analytics and associate properties with the charge. Properties is optional.

| Param         | Type                                                    |
| ------------- | ------------------------------------------------------- |
| **`options`** | <code><a href="#chargeoptions">ChargeOptions</a></code> |

**Returns:** <code>any</code>

--------------------


### flush()

```typescript
flush() => any
```

Uploads queued data to the Mixpanel server. (only ios, android)

**Returns:** <code>any</code>

--------------------


### optInTracking(...)

```typescript
optInTracking(options: OptInOptions) => any
```

Opt in tracking.

Use this method to opt in an already opted out user from tracking. People updates and track calls will be sent to Mixpanel after using this method.

| Param         | Type                                                  |
| ------------- | ----------------------------------------------------- |
| **`options`** | <code><a href="#optinoptions">OptInOptions</a></code> |

**Returns:** <code>any</code>

--------------------


### optOutTracking()

```typescript
optOutTracking() => any
```

Opt out tracking.

This method is used to opt out tracking. This causes all events and people request no longer to be sent back to the Mixpanel server.

**Returns:** <code>any</code>

--------------------


### hasOptedOutTracking()

```typescript
hasOptedOutTracking() => any
```

Returns the current opt-out status.

**Returns:** <code>any</code>

--------------------


### Interfaces


#### InitializeOptions

| Prop                  | Type                 | Description                                                       | Default            |
| --------------------- | -------------------- | ----------------------------------------------------------------- | ------------------ |
| **`token`**           | <code>string</code>  | Your Mixpanel API token                                           |                    |
| **`autotrack`**       | <code>boolean</code> | Enable or disable autotracking                                    | <code>true</code>  |
| **`optOutByDefault`** | <code>boolean</code> | Opting users out of tracking by this Mixpanel instance by default | <code>false</code> |
| **`debug`**           | <code>boolean</code> | Enable or disable debug mode                                      | <code>false</code> |


#### TrackOptions

| Prop             | Type                                                        | Description                                                                                                                                | Default         |
| ---------------- | ----------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | --------------- |
| **`event`**      | <code>string</code>                                         | The name of the event. This can be anything the user does - 'Button Click', 'Sign Up', 'Item Purchased', etc.                              |                 |
| **`properties`** | <code><a href="#trackproperties">TrackProperties</a></code> | A set of properties to include with the event you're sending. These describe the user who did the event or details about the event itself. | <code>{}</code> |


#### TrackProperties


#### IdentifyOptions

| Prop             | Type                | Description                                                                                                                                         |
| ---------------- | ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`distinctId`** | <code>string</code> | A string that uniquely identifies a user. If not provided, the distinct_id currently in the persistent store (cookie or localStorage) will be used. |


#### AliasOptions

| Prop             | Type                | Description                                                           |
| ---------------- | ------------------- | --------------------------------------------------------------------- |
| **`alias`**      | <code>string</code> | A unique identifier that you want to use for this user in the future. |
| **`distinctId`** | <code>string</code> | The current identifier being used for this user.                      |


#### SuperPropertyOptions

| Prop             | Type             | Description                                                |
| ---------------- | ---------------- | ---------------------------------------------------------- |
| **`properties`** | <code>any</code> | An associative array of properties to store about the user |


#### ProfileProperties

| Prop             | Type             | Description                                                |
| ---------------- | ---------------- | ---------------------------------------------------------- |
| **`properties`** | <code>any</code> | An associative array of properties to store about the user |


#### ChargeOptions

| Prop             | Type                | Description                                                       | Default         |
| ---------------- | ------------------- | ----------------------------------------------------------------- | --------------- |
| **`amount`**     | <code>number</code> | The amount of the transaction                                     |                 |
| **`properties`** | <code>any</code>    | An associative array of properties to store about the transaction | <code>{}</code> |


#### OptInOptions

| Prop             | Type                | Description                                                |
| ---------------- | ------------------- | ---------------------------------------------------------- |
| **`distinctId`** | <code>string</code> | String that uniquely identifies the current user.          |
| **`properties`** | <code>any</code>    | An associative array of properties to store about the user |

</docgen-api>

## Contributors

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tbody>
    <tr>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/mileszim"><img src="https://avatars.githubusercontent.com/u/1849508?v=4?s=75" width="75px;" alt="Miles Zimmerman"/><br /><sub><b>Miles Zimmerman</b></sub></a><br /><a href="https://github.com/houseninjadojo/capacitor-mixpanel/commits?author=mileszim" title="Code">💻</a> <a href="https://github.com/houseninjadojo/capacitor-mixpanel/commits?author=mileszim" title="Documentation">📖</a> <a href="#maintenance-mileszim" title="Maintenance">🚧</a> <a href="#example-mileszim" title="Examples">💡</a> <a href="#platform-mileszim" title="Packaging/porting to new platform">📦</a> <a href="#plugin-mileszim" title="Plugin/utility libraries">🔌</a></td>
      <td align="center" valign="top" width="14.28%"><a href="http://soundtrackcentral.com/"><img src="https://avatars.githubusercontent.com/u/6739666?v=4?s=75" width="75px;" alt="Adam C"/><br /><sub><b>Adam C</b></sub></a><br /><a href="https://github.com/houseninjadojo/capacitor-mixpanel/commits?author=tetsuwanadam" title="Code">💻</a> <a href="https://github.com/houseninjadojo/capacitor-mixpanel/commits?author=tetsuwanadam" title="Documentation">📖</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/chvonrohr"><img src="https://avatars.githubusercontent.com/u/1733057?v=4?s=75" width="75px;" alt="Christian von Rohr"/><br /><sub><b>Christian von Rohr</b></sub></a><br /><a href="https://github.com/houseninjadojo/capacitor-mixpanel/commits?author=chvonrohr" title="Code">💻</a> <a href="https://github.com/houseninjadojo/capacitor-mixpanel/commits?author=chvonrohr" title="Documentation">📖</a></td>
      <td align="center" valign="top" width="14.28%"><a href="https://github.com/mfrey-WELL"><img src="https://avatars.githubusercontent.com/u/99006448?v=4?s=75" width="75px;" alt="Matt"/><br /><sub><b>Matt</b></sub></a><br /><a href="https://github.com/houseninjadojo/capacitor-mixpanel/commits?author=mfrey-WELL" title="Code">💻</a> <a href="https://github.com/houseninjadojo/capacitor-mixpanel/commits?author=mfrey-WELL" title="Documentation">📖</a></td>
    </tr>
  </tbody>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!
