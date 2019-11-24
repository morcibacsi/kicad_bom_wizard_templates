# KiCAD BOM Wizard plugin templates

## What is it?

These are templates for the KiCAD BOM Wizard plugin. They allow you the generate the bill of materials needed for your PCBs designed with KiCAD.

- The *Mustache* folder contains a html template utilizing the mustache javascript library
- The *DokuWiki* folder contains a text template for inserting the BOM in DokuWiki instances or on GitHub

## How does it looks like?

**The DokuWiki version looks like this:**

| | |
|-|-|
|Total Number of Parts    |    36|
|Total Unique Parts    |    22|

|    Ref    |    Quantity    |    Value    |Footprint    |Fields    |
|-|-|-|-|-|
|    BZ1     |    1    |    Buzzer    |Buzzer_Beeper:MagneticBuzzer_Kingstate_KCG0601    |    |
|    C1 C2     |    2    |    22pF    |Capacitor_SMD:C_1206_3216Metric_Pad1.42x1.75mm_HandSolder    |    |
|    C3     |    1    |    0.33uF    |Capacitor_THT:CP_Radial_D4.0mm_P2.00mm    |    |
|    C4     |    1    |    0.1uF    |Capacitor_THT:CP_Radial_D4.0mm_P2.00mm    |    |

---

**The mustache version looks like this:**

![mustache.png](https://github.com/morcibacsi/kicad_bom_wizard_templates/raw/master/screenshots/mustache.png)

## How to use?
1. Install node.js
2. Install the KiCad BOM Wizard plugin

       npm install -g --production kicad_bom_wizard

3. From the **Tools menu** select **Generate bill of materials**

    - Click on **Add plugin** button
      - Select a file from the dialog (it doesn't really matter what you choose as we will replace the command line later)
      - Add a name to your plugin
      - Replace the command line with one of the following commands (modify the paths as needed):

            node "C:\Users\UserName\AppData\Roaming\npm\node_modules\kicad_bom_wizard\KiCad_BOM_Wizard.js" "%I" "%O.txt" "C:\Users\UserName\Documents\KiCAD\BOM_Templates\DokuWiki"
            node "C:\Users\UserName\AppData\Roaming\npm\node_modules\kicad_bom_wizard\KiCad_BOM_Wizard.js" "%I" "%O.html" "C:\Users\UserName\Documents\KiCAD\BOM_Templates\Mustache"

## Links

- [KiCad BOM Wizard plugin][bom_wizard_github]
- [KiCad BOM Wizard home page][bom_wizard_homepage]
- [mustache.js][mustachejs_github]

[bom_wizard_github]: https://github.com/HashDefineElectronics/KiCad_BOM_Wizard
[bom_wizard_homepage]: https://www.hashdefineelectronics.com/kicad-bom-wizard/
[mustachejs_github]: https://github.com/janl/mustache.js
