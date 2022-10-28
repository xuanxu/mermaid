# Module: config

## Variables

### <a id="defaultconfig" name="defaultconfig"></a> defaultConfig

• `Const` **defaultConfig**: `MermaidConfig`

#### Defined in

config.ts:7

## Functions

### <a id="adddirective" name="adddirective"></a> addDirective

▸ **addDirective**(`directive`): `void`

Pushes in a directive to the configuration

#### Parameters

| Name        | Type  | Description              |
| :---------- | :---- | :----------------------- |
| `directive` | `any` | The directive to push in |

#### Returns

`void`

#### Defined in

config.ts:191

---

### <a id="getconfig" name="getconfig"></a> getConfig

▸ **getConfig**(): `MermaidConfig`

## getConfig

| Function  | Description               | Type        | Return Values                  |
| --------- | ------------------------- | ----------- | ------------------------------ |
| getConfig | Obtains the currentConfig | Get Request | Any Values from current Config |

**Notes**: Returns **any** the currentConfig

#### Returns

`MermaidConfig`

The currentConfig

#### Defined in

config.ts:136

---

### <a id="getsiteconfig" name="getsiteconfig"></a> getSiteConfig

▸ **getSiteConfig**(): `MermaidConfig`

## getSiteConfig

| Function      | Description                                       | Type        | Values                           |
| ------------- | ------------------------------------------------- | ----------- | -------------------------------- |
| setSiteConfig | Returns the current siteConfig base configuration | Get Request | Returns Any Values in siteConfig |

**Notes**: Returns **any** values in siteConfig.

#### Returns

`MermaidConfig`

The siteConfig

#### Defined in

config.ts:96

---

### <a id="reset" name="reset"></a> reset

▸ **reset**(`config?`): `void`

## reset

| Function | Description                  | Type        | Required | Values |
| -------- | ---------------------------- | ----------- | -------- | ------ |
| reset    | Resets currentConfig to conf | Put Request | Required | None   |

## conf

| Parameter | Description                                                    | Type       | Required | Values                                       |
| --------- | -------------------------------------------------------------- | ---------- | -------- | -------------------------------------------- |
| conf      | base set of values, which currentConfig could be **reset** to. | Dictionary | Required | Any Values, with respect to the secure Array |

**Notes**: (default: current siteConfig ) (optional, default `getSiteConfig()`)

#### Parameters

| Name     | Type            | Default value | Description                                                                                                                                                   |
| :------- | :-------------- | :------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `config` | `MermaidConfig` | `siteConfig`  | base set of values, which currentConfig could be **reset** to. Defaults to the current siteConfig (e.g returned by [getSiteConfig](config.md#getsiteconfig)). |

#### Returns

`void`

#### Defined in

config.ts:223

---

### <a id="sanitize" name="sanitize"></a> sanitize

▸ **sanitize**(`options`): `void`

## sanitize

| Function | Description                            | Type        | Values |
| -------- | -------------------------------------- | ----------- | ------ |
| sanitize | Sets the siteConfig to desired values. | Put Request | None   |

Ensures options parameter does not attempt to override siteConfig secure keys **Notes**: modifies
options in-place

#### Parameters

| Name      | Type  | Description                       |
| :-------- | :---- | :-------------------------------- |
| `options` | `any` | The potential setConfig parameter |

#### Returns

`void`

#### Defined in

config.ts:151

---

### <a id="saveconfigfrominitialize" name="saveconfigfrominitialize"></a> saveConfigFromInitialize

▸ **saveConfigFromInitialize**(`conf`): `void`

#### Parameters

| Name   | Type            |
| :----- | :-------------- |
| `conf` | `MermaidConfig` |

#### Returns

`void`

#### Defined in

config.ts:75

---

### <a id="setconfig" name="setconfig"></a> setConfig

▸ **setConfig**(`conf`): `MermaidConfig`

## setConfig

| Function      | Description                           | Type        | Values                                  |
| ------------- | ------------------------------------- | ----------- | --------------------------------------- |
| setSiteConfig | Sets the siteConfig to desired values | Put Request | Any Values, except ones in secure array |

**Notes**: Sets the currentConfig. The parameter conf is sanitized based on the siteConfig.secure
keys. Any values found in conf with key found in siteConfig.secure will be replaced with the
corresponding siteConfig value.

#### Parameters

| Name   | Type            | Description                 |
| :----- | :-------------- | :-------------------------- |
| `conf` | `MermaidConfig` | The potential currentConfig |

#### Returns

`MermaidConfig`

The currentConfig merged with the sanitized conf

#### Defined in

config.ts:113

---

### <a id="setsiteconfig" name="setsiteconfig"></a> setSiteConfig

▸ **setSiteConfig**(`conf`): `MermaidConfig`

## setSiteConfig

| Function      | Description                           | Type        | Values                                  |
| ------------- | ------------------------------------- | ----------- | --------------------------------------- |
| setSiteConfig | Sets the siteConfig to desired values | Put Request | Any Values, except ones in secure array |

**Notes:** Sets the siteConfig. The siteConfig is a protected configuration for repeat use. Calls
to reset() will reset the currentConfig to siteConfig. Calls to reset(configApi.defaultConfig)
will reset siteConfig and currentConfig to the defaultConfig Note: currentConfig is set in this
function _Default value: At default, will mirror Global Config_

#### Parameters

| Name   | Type            | Description                                 |
| :----- | :-------------- | :------------------------------------------ |
| `conf` | `MermaidConfig` | The base currentConfig to use as siteConfig |

#### Returns

`MermaidConfig`

The new siteConfig

#### Defined in

config.ts:61

---

### <a id="updatecurrentconfig" name="updatecurrentconfig"></a> updateCurrentConfig

▸ **updateCurrentConfig**(`siteCfg`, `_directives`): `MermaidConfig`

#### Parameters

| Name          | Type            |
| :------------ | :-------------- |
| `siteCfg`     | `MermaidConfig` |
| `_directives` | `any`[]         |

#### Returns

`MermaidConfig`

#### Defined in

config.ts:14

---

### <a id="updatesiteconfig" name="updatesiteconfig"></a> updateSiteConfig

▸ **updateSiteConfig**(`conf`): `MermaidConfig`

#### Parameters

| Name   | Type            |
| :----- | :-------------- |
| `conf` | `MermaidConfig` |

#### Returns

`MermaidConfig`

#### Defined in

config.ts:79