# Set Tab Color

Provides the functionality to change the color scheme of the relationship tab of Aras Innovator's tear-off window (item detail screen).
* Relationship tab color setting
* Setting the color of the relationship tab

Aras Innovatorのティアオフウィンドウ（アイテム詳細画面）のリレーションタブの配色を変更する 機能を提供します。
* タブリレーションの配色設定
* タブリレーションの文字色の設定

## History

This project and the following release notes have been migrated from the old Aras Projects page.

Release | Notes
--------|--------
[v3.1.0](https://github.com/ArasLabs/set-tab-color/releases/tag/v3.1.0) | Automatically configures the OnLoad form event for the Ext_SetTabColor method.
[v3.0.0](https://github.com/ArasLabs/set-tab-color/releases/tag/v3.0.0) | Support the tabbed client in Aras 11 SP12-14. May also work in 11 SP8-SP11, but has not been tested.
[v2.0.0](https://github.com/ArasLabs/set-tab-color/releases/tag/v2.0.0) | Support version 11SP6. Instructions are described in the ReadMe.pdf. AKA [v11SP6](https://github.com/ArasLabs/set-tab-color/releases/tag/v11SP6).
[v1.0.0](https://github.com/ArasLabs/set-tab-color/releases/tag/v1.0.0) | Support version 11SP5. Instructions are described in the ReadMe.pdf. AKA [v11SP5](https://github.com/ArasLabs/set-tab-color/releases/tag/v11SP5).

#### Supported Aras Versions

Project | Aras
--------|------
[v3.1.0](https://github.com/ArasLabs/set-tab-color/releases/tag/v3.1.0) | 11.0 SP12-14
[v3.0.0](https://github.com/ArasLabs/set-tab-color/releases/tag/v3.0.0) | 11.0 SP12-14
[v2.0.0](https://github.com/ArasLabs/set-tab-color/releases/tag/v2.0.0) | 11.0 SP6
[v1.0.0](https://github.com/ArasLabs/set-tab-color/releases/tag/v1.0.0) | 11.0 SP5

## Installation

#### Important!
**Always back up your code tree and database before applying an import package or code tree patch!**

### Pre-requisites

1. Aras Innovator installed
2. Aras Package Import tool
3. **SetTabColor** import package

### Install Steps

1. Backup your database and store the BAK file in a safe place.
2. Open up the Aras Package Import tool.
3. Enter your login credentials and click **Login**
  * _Note: You must login as root for the package import to succeed!_
4. Enter the package name in the TargetRelease field.
  * Optional: Enter a description in the Description field.
5. Enter the path to your local `..\SetTabColor\Import\imports.mf` file in the Manifest File field.
6. Select **SetTabColor** in the Available for Import field.
7. Select Type = **Merge** and Mode = **Thorough Mode**.
8. Click **Import** in the top left corner.
9. Close the Aras Package Import tool.

#### _Optional:_
Japanese language settings may be applied using the contents of the Language directory and the LanguagePackManagementUtility.

## Usage

![Screenshot Gif](Screenshots/screenshot.gif)

1. Login to Innovator as admin.
2. Navigate to **Administration > Configuration > Set Tab Color** in the table of contents (TOC).
3. Click **Add New** to create a new tab color setting.
4. Fill out the form:
    * Ext_Item: The parent ItemType of the tab you want to style
    * Ext_tab_name: The RelationshipType of the tab you want to style
    * Ext_tab_color: The background color of the tab
    * Ext_tab_font_color: The font color of the tab
5. Click the green checkmark to save, unlock, and close the tab color setting.
6. Repeat steps 3-5 for all tabs you want to style.

> Note: As of release [v3.1.0](https://github.com/ArasLabs/set-tab-color/releases/tag/v3.1.0), the Ext_SetTabColor method will be automatically added to all forms for the "ext_item" when you create a new tab color setting. If you want to disable this behavior, you can remove the Ext_AddFormEvent server event from the Ext_SetTabColor ItemType. However, this means that you will need to manually add an OnLoad event to every form that should use colored tabs.

Review the [ReadMe(SetTabColor).pdf](./Documentation/ReadMe-SetTabColor.pdf) for additional information on using the project. {[English translation](./Documentation/ReadMe-SetTabColor-English.docx)}

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

## Credits

Created by NEOSYSTEM Co., Ltd.

**Other Contributors:**
* Eli Donahue for Aras Labs (@elijdonahue)
