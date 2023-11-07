# Odoo Framework Integration for Visual Studio Code

Boost your productivity and make your life easier as an Odoo developer

[Homepage](https://odoo-ide.com) | [Blog](https://odoo-ide.com/blog) | [Issue Tracker](https://github.com/odoo-ide/vscode-odoo/issues)

This extension is in the early stages of development. A lot of features are missing compared to the [PyCharm plugin for Odoo](https://plugins.jetbrains.com/plugin/13499-odoo).

## Features
- Resolve `odoo.addons.*` imports for built-in addons and custom addons.
- Fully understand model inheritance mechanisms.
- Code completion and navigation for module names, model names, field names, XML IDs,...

## Installation
1. Install the Odoo IDE extension from [VSCode Marketplace](https://marketplace.visualstudio.com/items?itemName=trinhanhngoc.vscode-odoo).
2. Install [PyDev.Debugger plugin for Odoo](https://github.com/odoo-ide/pydevd-odoo) to improve Odoo debugging.

## Notes
- As of version 0.6.0, the Odoo plugin has built-in [odoo-stubs](https://github.com/odoo-ide/odoo-stubs), so you don't need to add them manually anymore.
- The Odoo extension will automatically set `Python Language Server` to `None` in settings for Odoo workspaces because this extension uses a custom language server for the Odoo framework. If you have the Pyright extension installed, you should also disable it. Otherwise, you will have multiple language servers running with the same features that waste your system resources.
- The Odoo extension is currently built on top of [Pyright](https://github.com/microsoft/pyright) so it inherits all features of Pyright.
- Depending on how you structure your projects, the Odoo extension may not be able to resolve odoo imports. You can manually add the Odoo source code and your custom addons paths to settings as described in the [import resolution documentation](https://microsoft.github.io/pyright/#/import-resolution).
- Both the Odoo source code and your custom addons must be added to your VSCode workspace for the Odoo extension to work as expected.

## Screenshots
![Model member completion](images/model-member-completion.png)
![Model name completion](images/model-name-completion.png)
![Model name navigation](images/model-name-navigation.png)
![Field name completion](images/field-name-completion.png)
