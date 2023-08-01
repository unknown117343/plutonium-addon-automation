# Plutonium Addon: Automation

*Plutonium Addon: Automation* is a module to extend Plutonium, for the purpose of marrying the importation of D&D 5e game material with the automation provided by the 'Midi ecosystem'.

- [Disclaimer](#disclaimer)
- [How it works](#how-it-works)
- [Installation](#installation)
   - [Dependencies and incompatibilities](#dependencies-and-incompatibilities)
   - [**Required** set-up](#required-set-up) (⚠️ **read this!**)
   - [Optional integrations](#optional-integrations)
- [Contributing](#contributing)

---

## Disclaimer

*Plutonium Addon: Automation* is **NOT** supported by any of the modules listed below. If you encounter an issue with your game, disable *Plutonium* and *Plutonium Addon: Automation* and try again.

If an issue persists, consider asking about it in the [Issues section](https://github.com/TheGiddyLimit/plutonium-addon-automation/issues) or in our [Discord](https://discord.gg/5etools) before bringing it to the attention of other module authors.

⚠️ Beware the rules of other spaces when discussing *Plutonium* and/or *Plutonium Addon: Automation* module outwith the above channels! ⚠️

## How it works

*Plutonium Addon: Automation* runs invisibly and mostly silently.

While the module is activated in your world, each time Plutonium would import a document, it will check if any automation data is available for that document. If so, it will import the document with the additional automation data included. If not, it will import the document as Plutonium standard (although sometimes slightly tweaked to better enable the module dependencies outlined below).

As with Plutonium, **all data is included in the module itself**. There's no need to import everything prematurely, 'just in case'.

Some automations don't use effects directly, but rather call item macros. If you, as the GM, wish to allow players to view/edit these macros on items they own, install and configure [Item Macro](https://foundryvtt.com/packages/itemacro) to allow the _Player access_ option.

## Installation

You can install the module using the following manifest URL:

`https://github.com/TheGiddyLimit/plutonium-addon-automation/releases/latest/download/module.json`

### Dependencies and incompatibilities

Besides Plutonium itself, *Plutonium Addon: Automation* **requires**:
- [DFred's Convenient Effects](https://foundryvtt.com/packages/dfreds-convenient-effects) (DFCE)
- [Dynamic Active Effects](https://foundryvtt.com/packages/dae) (DAE)
- [Midi QoL](https://foundryvtt.com/packages/midi-qol)
- [Times Up](https://foundryvtt.com/packages/times-up)

Some specific automations require one or more additional modules:
- [Active-Auras](https://foundryvtt.com/packages/ActiveAuras)
- [Active Token Effects](https://foundryvtt.com/packages/ATL)
- [Item Macro](https://foundryvtt.com/packages/itemacro)
- [Warp Gate](https://foundryvtt.com/packages/warpgate)

If you import a document which requires one of these modules, you will be prompted to install/activate it. The automation is highly unlikely to function as intended if you use it before activating the module.

*Plutonium Addon: Automation* is designed for the extensive automation provided by the 'Midi ecosystem' and, as such, *isn't* designed for modules such as [Whistler's Item Rolls Extended](https://foundryvtt.com/packages/wire), [Ready Set Roll for D&D5e](https://foundryvtt.com/packages/ready-set-roll-5e), [MRE 5e](https://foundryvtt.com/packages/mre-dnd5e), and [Better Rolls](https://foundryvtt.com/packages/betterrolls5e). Using any of these may cause problems. We also don't recommend using this with [Combat Utility Belt](https://foundryvtt.com/packages/combat-utility-belt).

### Required set-up

You **must** configure some modules in a specific way, or the automations won't work. Configure the following:

- _**DFreds Convenient Effects** > Modify Status Effects_ — select either `Replace` (preferred) or `Add`.
- _**Midi QoL** > Midi QoL config > Workflow > Apply Convenient Effects_ — select `Apply Item effects, if absent apply CE`.

If you have [Item Macro](https://foundryvtt.com/packages/itemacro) activated, you also need to configure it as follows:

- _**Item Macro** > Override default macro execution_ — uncheck this.
- _**Item Macro** > Character Sheet Hook_ — uncheck this.
- (If installed) _**[Token Action HUD](https://foundryvtt.com/packages/token-action-hud)** > Item-Macro: item macro, original item, or both_ — select `Show the original item`. (Note this is a user setting, so either ensure that each user configures this or use a module such as [Force Client Settings](https://foundryvtt.com/packages/force-client-settings) to guarantee it.)

### Optional integrations

*Plutonium Addon: Automation* can optionally make use of data provided by other modules. An integration is available for:
- [Chris's Premades](https://foundryvtt.com/packages/chris-premades)
- [Midi SRD](https://foundryvtt.com/packages/midi-srd)

This integration is only active if the above module is installed and active, and can be disabled in *Plutonium Addon: Automation*'s settings.

## Contributing

Please see [`CONTRIBUTING.md`](./CONTRIBUTING.md).
