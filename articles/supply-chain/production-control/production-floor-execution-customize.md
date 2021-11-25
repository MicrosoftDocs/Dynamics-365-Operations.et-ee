---
title: Tootmisosakonna täideviimisliidese kohandamine
description: See teema selgitab, kuidas laiendada praegusi vorme või luua uusi vorme ja nuppe tootmispinna käivitamise liidesele.
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
ms.openlocfilehash: 414fe5d6e16ad125bc2b9bb7ed427e5db5180ec9
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790966"
---
# <a name="customize-the-production-floor-execution-interface"></a>Tootmisosakonna täideviimisliidese kohandamine

[!include [banner](../includes/banner.md)]

Arendajad saavad laiendada praegusi vorme või luua tootmispinna käivitamise liidesele oma vorme ja nuppe. Pärast uute elementide koodi lisamist saavad administraatorid või tööde juhatajad standardkonfiguratsiooni juhtelementide abil neid hõlpsasti liidesele lisada.

Näiteks siin on mõned võimalikud lahendused, kui põhivormis on vaja uusi veerge:

- Laiendage `JmgProductionFloorExecutionMainGrid` vormi ja lisage soovitud väljad.
- Looge uus vorm ja lisage see uue põhivaatena (vahekaardil).

## <a name="add-a-new-button-action"></a>Uue nupu lisamine (tegevus)

Uue nupu (tegevuse) lisamiseks järgige neid samme, et luua klassi, mis juurutab teie kohandatud tegevuse.

1. Looge uus klass `<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action` nimega, kus:

    - `<ExtensionPrefix>` identifitseerib teie lahenduse kordumatult, tavaliselt ettevõtte nime kasutades.
    - `<ActionName>` on klassi kordumatu nimi. Tavaliselt määrab see tegevuse laadi.

1. Uus klass peab klassi `JmgProductionFloorExecutionAction` laiendama.
1. Alistage kõik vajalikud meetodid.

Näiteid: vaadake järgmiste klasside koodi:

- `JmgProductionFloorExecutionBreakAction`: klass lihtsa tegevuse jaoks, mis ei vaja ühtegi kirjet.
- `JmgProductionFloorExecutionReportFeedbackAction`– klass, mis pakub keerukamaid funktsioone.

Kui olete lõpetanud, loetletakse uus nupp (tegevus) automaatselt **Microsofti** vahekaartide kujunduste Dynamics 365 Supply Chain Management loendis. Seal saate (või administraatori või korruse halduri) selle hõlpsalt lisada esmasele või teisesele tööriistaribale, samuti nagu saate lisada standardnuppe. Juhiseid vt [tootmispinna käivitamise liidese](production-floor-execution-tabs.md) kujundusest.

## <a name="add-a-new-main-view"></a>Lisa uus põhivaade

1. Looge uus vorm, kus on soovitud elemendid ja funktsioonid. Pange tähele, et see vorm on uus vorm, mitte laiend. Vormile `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>` nimi, kus:

    - `<ExtensionPrefix>` identifitseerib teie lahenduse kordumatult, tavaliselt ettevõtte nime kasutades.
    - `<FormName>` on vormi kordumatu nimi.

1. Looge menüükäsk nimega .`<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`.
1. Looge laiend `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension` nimega, kus meetodit `getMainMenuItemsList` laiendatakse, lisades loendisse uue menüükäsu. Järgmine kood näitab näidet.

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

Kui olete lõpetanud, loetletakse uus põhivaade automaatselt tarneahela halduse vahekaardi Kujundus **·** **·** põhivaate liitboksis. Seal saate (või administraatori või korruse halduri) selle lihtsalt lisada uutele või olemasolevatele vahekaartidele, samuti nagu saate lisada standardseid põhivaateid. Juhiseid vt [tootmispinna käivitamise liidese](production-floor-execution-tabs.md) kujundusest.

## <a name="add-a-details-view"></a>Üksikasjade vaate lisamine

1. Looge uus vorm, kus on soovitud elemendid ja funktsioonid. Pange tähele, et see vorm on uus, mitte laiend. Vormile `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail` nimi, kus: 

    - `<ExtensionPrefix>` identifitseerib teie lahenduse kordumatult, tavaliselt ettevõtte nime kasutades.
    - `<FormName>` on vormi kordumatu nimi.

1. Looge menüükäsk nimega .`<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`.
1. Looge laiend `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension` nimega, kus meetodit `getDetailsMenuItemList` laiendatakse, lisades loendisse uue menüükäsu.

Kui olete lõpetanud, loetletakse uus üksikasjade vaade automaatselt vahekaardi Kujundus ja tarneahela haldus üksikasjade vaate **·** **·** liitboksis. Seal saate (või administraatori või korruse halduri) selle lihtsalt lisada uutele või olemasolevatele vahekaartidele, samuti nagu saate lisada standardseid üksikasju. Juhiseid vt [tootmispinna käivitamise liidese](production-floor-execution-tabs.md) kujundusest.

## <a name="add-a-numeric-keypad-to-a-form-or-dialog"></a>Numbriklahvistiku lisamine vormile või dialoogile

Järgmine näide näitab, kuidas lisada vormile numbrivõtmeid.

1. Numbriklahvistiku kontrollerite arv, mida iga vorm sisaldab, peab olema võrdne arvuliste klahvistike arvuga selles vormis.

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

Järgmises näites on näha üks viis seadistada numbriklahvistiku kontroller hüpikdialoogi jaoks.

```xpp
private void setupNumpadController()
{
    numpadController = new JmgProductionFloorExecutionNumpadController();
    numpadController.parmShouldNumpadShowOkCancelButtons(true);
    numpadController.setNumpadValueToParentFormDelegate += eventhandler(this.setQtyValueFromNumpad);
}
```

Järgmine näide näitab ühte võimalust kutsuda numbriklahvistiku hüpikdialoogi.

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
