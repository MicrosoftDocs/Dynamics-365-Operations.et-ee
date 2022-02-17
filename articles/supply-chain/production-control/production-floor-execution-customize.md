---
title: Tootmisosakonna täideviimisliidese kohandamine
description: Selles teemas selgitatakse, kuidas laiendada praeguseid vorme või luua uusi vorme ja nuppe tootmispõranda täitmise liidese jaoks.
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-11-08
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 67fb381cbef6f1673afcaa834666b4a859bdf4e6
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066542"
---
# <a name="customize-the-production-floor-execution-interface"></a>Tootmisosakonna täideviimisliidese kohandamine

[!include [banner](../includes/banner.md)]

Arendajad saavad laiendada praeguseid vorme või luua oma vormid ja nupud tootmispõranda täitmise liidese jaoks. Pärast nende uute elementide koodi lisamist saavad administraatorid või töökojahaldurid need standardsete konfiguratsiooni juhtelementide abil hõlpsalt liidesesse lisada.

Näiteks siin on mõned võimalikud lahendused, kui põhivormis on vaja uusi veerge:

- Laiendage `JmgProductionFloorExecutionMainGrid` vormi ja lisage soovitud väljad.
- Looge uus vorm ja lisage see uue põhivaatena (vahekaart).

## <a name="add-a-new-button-action"></a>Uue nupu lisamine (toiming)

Uue nupu (toimingu) lisamiseks tehke kohandatud toimingut rakendava klassi loomiseks järgmist.

1. Looge uus klass nimega `<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action`, kus:

    - `<ExtensionPrefix>` tuvastab teie lahenduse ainulaadselt, kasutades tavaliselt teie ettevõtte nime.
    - `<ActionName>` See on klassi unikaalne nimi. Tavaliselt tuvastab see tegevuse liigi.

1. Uus klass peab klassi laiendama `JmgProductionFloorExecutionAction`.
1. Alistage kõik vajalikud meetodid.

Näitena vaadake järgmiste klasside koodi.

- `JmgProductionFloorExecutionBreakAction`– Klass lihtsaks tegevuseks, mis ei vaja kirjeid.
- `JmgProductionFloorExecutionReportFeedbackAction`– Klass, mis pakub keerukamaid funktsioone.

Kui olete lõpetanud, loetletakse **uus nupp (toiming) automaatselt Microsofti** menüüde Dynamics 365 Supply Chain Management Kujundus lehel. Seal saate (või administraatori või põrandahalduri) hõlpsasti lisada esmasele või sekundaarsele tööriistaribale, nagu saate lisada standardseid nuppe. Juhised leiate teemast [Tootmispõranda täitmise liidese](production-floor-execution-tabs.md) kujundamine.

## <a name="add-a-new-main-view"></a>Uue põhivaate lisamine

1. Looge uus vorm, millel on soovitud elemendid ja funktsionaalsus. Pange tähele, et see vorm on uus vorm, mitte laiendus. Nimetage vorm `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`, kus:

    - `<ExtensionPrefix>` tuvastab teie lahenduse ainulaadselt, kasutades tavaliselt teie ettevõtte nime.
    - `<FormName>` See on vormi unikaalne nimi.

1. Looge menüükäsk nimega `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`.
1. Looge nimeline `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension` laiendus, kus `getMainMenuItemsList` meetodit laiendatakse, lisades loendisse uue menüükäsu. Järgmine kood näitab näidet.

    ```xpp
    [ExtensionOf(classStr(JmgProductionFloorExecutionForm))]
    public final class <ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>_Extension{
        static public List getMainMenuItemsList()
        {
            List menuItemList = next getMainMenuItemsList();
            menuItemList.addEnd(menuItemDisplayStr(<ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>));
            return menuItemList;
        }
    ```

Kui olete lõpetanud, loetletakse **uus põhivaade automaatselt tarneahela halduse menüüDe Kujundus väljal** **Põhivaade**. Seal saate (või administraatori või põrandahalduri) hõlpsasti lisada seda uutele või olemasolevatele vahekaartidele, nagu saate lisada standardseid põhivaateid. Juhised leiate teemast [Tootmispõranda täitmise liidese](production-floor-execution-tabs.md) kujundamine.

## <a name="add-a-details-view"></a>Üksikasjade vaate lisamine

1. Looge uus vorm, millel on soovitud elemendid ja funktsionaalsus. Pange tähele, et see vorm on uus, mitte laiendus. Nimetage vorm `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`, kus: 

    - `<ExtensionPrefix>` tuvastab teie lahenduse ainulaadselt, kasutades tavaliselt teie ettevõtte nime.
    - `<FormName>` See on vormi unikaalne nimi.

1. Looge menüükäsk nimega `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`.
1. Looge nimeline `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension` laiendus, kus `getDetailsMenuItemList` meetodit laiendatakse, lisades loendisse uue menüükäsu.

Kui olete lõpetanud, loetletakse **uus üksikasjade vaade automaatselt tarneahela halduse menüüDe Kujundus väljal** **Üksikasjad.** Seal saate (või administraatori või põrandahalduri) hõlpsasti lisada uutele või olemasolevatele vahekaartidele, nagu saate lisada standardseid üksikasjade vaateid. Juhised leiate teemast [Tootmispõranda täitmise liidese](production-floor-execution-tabs.md) kujundamine.

## <a name="add-a-numeric-keypad-to-a-form-or-dialog"></a>Numbriklahvistiku lisamine vormi või dialoogi

Järgmises näites kirjeldatakse, kuidas vormile numbrilisi klaviatuure lisada.

1. Numbriklahvistiku kontrollerite arv, mida iga vorm sisaldab, peab võrduma numbriklahvistiku arvuga sellel kujul.

    ```xpp
    private JmgProductionFloorExecutionNumpadController   numpadController1;
    private JmgProductionFloorExecutionNumpadController   numpadController2;
    private JmgProductionFloorExecutionNumpadController   numpadController3;
    ```

1. Seadistage iga numbriklahvistiku kontrolleri käitumine ja ühendage iga numbriklahvistiku kontroller numbriklahvistiku vormiosaga.

    ```xpp
    /// <summary>
    /// Initializes all numpad controllers, defines their behavior and connects them with numpad form parts.
    /// </summary>
    public void initializeNumpadController()
    {
        numpadController1 = new JmgProductionFloorExecutionNumpadController();
        numpadController1.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_1);
        QuantityNumpad1.getPartFormRun().setNumpadController(numpadController1);
    
        numpadController2 = new JmgProductionFloorExecutionNumpadController();
        numpadController2.parmNumpadEnabled(false);
        numpadController2.parmNumpadValue(333.56);
        numpadController2.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_2);
        QuantityNumpad2.getPartFormRun().setNumpadController(numpadController2);
    }
    ```

## <a name="use-a-numeric-keypad-as-a-pop-up-dialog"></a>Numbriklahvistiku kasutamine hüpikdialoogina

Järgmises näites on üks võimalus seadistada hüpikdialoogi jaoks numbriklahvistiku kontroller.

```xpp
private void setupNumpadController()
{
    numpadController = new JmgProductionFloorExecutionNumpadController();
    numpadController.parmShouldNumpadShowOkCancelButtons(true);
    numpadController.setNumpadValueToParentFormDelegate += eventhandler(this.setQtyValueFromNumpad);
}
```

Järgmises näites on üks viis numbriklahvistiku hüpikdialoogiks helistamiseks.

```xpp
Args args = new Args();
args.name(formstr(JmgProductionFloorExecutionNumpad));
args.menuItemName(menuItemDisplayStr(JmgProductionFloorExecutionNumpad));
args.caller(element);
Object formRun = classfactory.formRunClass(args);
formRun.init();
formRun.setNumpadController(numpadController);
numpadController.setValueToNumpad(333.56);
formRun.run();
```

## <a name="additional-resources"></a>Lisaressursid

- [Tootmisosakonna täideviimisliidese kujundamine](production-floor-execution-styles.md)
- [Tootmisosakonna täideviimisliidese kujundamine](production-floor-execution-tabs.md)
