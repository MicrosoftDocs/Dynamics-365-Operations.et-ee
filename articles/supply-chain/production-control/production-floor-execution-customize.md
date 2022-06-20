---
title: Tootmisosakonna täideviimisliidese kohandamine
description: See artikkel selgitab, kuidas laiendada praeguseid vorme või luua uusi vorme ja nuppe tootmispinna käivitamise liidesele.
author: johanhoffmann
ms.date: 05/04/2022
ms.topic: article
ms.search.form: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-11-08
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 13fa6c2f3c30a820585d1b5a758f57ec563664d1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845978"
---
# <a name="customize-the-production-floor-execution-interface"></a>Tootmisosakonna täideviimisliidese kohandamine

[!include [banner](../includes/banner.md)]

Arendajad saavad laiendada praegusi vorme või luua tootmispinna käivitamise liidesele oma vorme ja nuppe. Pärast uute elementide koodi lisamist saavad administraatorid või tööde juhatajad standardkonfiguratsiooni juhtelementide abil neid hõlpsasti liidesele lisada.

Näiteks siin on mõned võimalikud lahendused, kui põhivormis on vaja uusi veerge:

- Laiendage `JmgProductionFloorExecutionMainGrid` vormi ja lisage soovitud väljad.
- Looge uus vorm ja lisage see uue põhivaatena (vahekaardil).

## <a name="add-a-new-button-action"></a>Uue nupu lisamine (tegevus)

Uue nupu (tegevuse) lisamiseks järgige neid samme, et luua klassi, mis juurutab teie kohandatud tegevuse.

1. Looge uus klass nimega `<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action`, kus:

    - `<ExtensionPrefix>` identifitseerib teie lahenduse kordumatult, tavaliselt ettevõtte nime kasutades.
    - `<ActionName>` on klassi kordumatu nimi. Tavaliselt määrab see tegevuse laadi.

1. Uus klass peab klassi laiendama `JmgProductionFloorExecutionAction`.
1. Alistage kõik vajalikud meetodid.

Näiteid: vaadake järgmiste klasside koodi:

- `JmgProductionFloorExecutionBreakAction`: klass lihtsa tegevuse jaoks, mis ei vaja ühtegi kirjet.
- `JmgProductionFloorExecutionReportFeedbackAction`– klass, mis pakub keerukamaid funktsioone.

Kui olete lõpetanud, loetletakse uus nupp (tegevus) **automaatselt Microsofti vahekaartide** kujunduste loendis Dynamics 365 Supply Chain Management. Seal saate (või administraatori või korruse halduri) selle hõlpsalt lisada esmasele või teisesele tööriistaribale, samuti nagu saate lisada standardnuppe. Juhiseid vt tootmispinna [käivitamise liidese kujundusest](production-floor-execution-tabs.md).

## <a name="add-a-new-main-view"></a>Lisa uus põhivaade

1. Looge uus vorm, kus on soovitud elemendid ja funktsioonid. Pange tähele, et see vorm on uus vorm, mitte laiend. Vormile nimi `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`, kus:

    - `<ExtensionPrefix>` identifitseerib teie lahenduse kordumatult, tavaliselt ettevõtte nime kasutades.
    - `<FormName>` on vormi kordumatu nimi.

1. Looge menüükäsk nimega .`<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`.
1. Looge laiend nimega, `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension` kus meetodit `getMainMenuItemsList` laiendatakse, lisades loendisse uue menüükäsu. Järgmine kood näitab näidet.

    ```xpp
    [ExtensionOf(classStr(JmgProductionFloorExecutionMenuItemProvider))]
    public final class <ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>_Extension{
        static public List getMainMenuItemsList()
        {
            List menuItemList = next getMainMenuItemsList();
            menuItemList.addEnd(menuItemDisplayStr(<ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>));
            return menuItemList;
        }
    ```

Kui olete lõpetanud, loetletakse **·** **uus põhivaade automaatselt tarneahela halduse vahekaardi Kujundus põhivaate liitboksis.** Seal saate (või administraatori või korruse halduri) selle lihtsalt lisada uutele või olemasolevatele vahekaartidele, samuti nagu saate lisada standardseid põhivaateid. Juhiseid vt tootmispinna [käivitamise liidese kujundusest](production-floor-execution-tabs.md).

## <a name="add-a-details-view"></a>Üksikasjade vaate lisamine

1. Looge uus vorm, kus on soovitud elemendid ja funktsioonid. Pange tähele, et see vorm on uus, mitte laiend. Vormile nimi `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`, kus: 

    - `<ExtensionPrefix>` identifitseerib teie lahenduse kordumatult, tavaliselt ettevõtte nime kasutades.
    - `<FormName>` on vormi kordumatu nimi.

1. Looge menüükäsk nimega .`<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`.
1. Looge laiend nimega, `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension` kus meetodit `getDetailsMenuItemList` laiendatakse, lisades loendisse uue menüükäsu.

Kui olete lõpetanud, **·** **loetletakse uus üksikasjade vaade automaatselt vahekaardi Kujundus ja tarneahela haldus üksikasjade vaate liitboksis.** Seal saate (või administraatori või korruse halduri) selle lihtsalt lisada uutele või olemasolevatele vahekaartidele, samuti nagu saate lisada standardseid üksikasju. Juhiseid vt tootmispinna [käivitamise liidese kujundusest](production-floor-execution-tabs.md).

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

## <a name="add-a-date-and-time-controls-to-a-form-or-dialog"></a>Kuupäeva ja kellaaja juhtelementide lisamine vormile või dialoogile

See jaotis näitab, kuidas lisada kuupäeva ja kellaaja juhtelemente vormile või dialoogile. Puutetundliku kuupäeva ja kellaaja juhtelemendid võimaldavad töötajatel kuupäevi ja kellaaegu määrata. Järgmised kuvatõmmised näitavad, kuidas juhtelemendid tavaliselt lehel kuvatakse. Ajakontroll annab nii 12-tunnised kui 24-tunnised versioonid. kuvatud versioon järgib selle kasutajakonto eelistuse seadistust, milles liides töötab.

![Kuupäevakontrolli näide.](media/pfe-customize-date-control.png "Kuupäeva kontrolli näide")

![Kellaaja juhtimise näide 12-tunnise kellaga.](media/pfe-customize-time-control-12h.png "12-tunnise kellaga aja juhtimise näide")

![Kellaaja juhtimise näide 24-tunnise kellaga.](media/pfe-customize-time-control-24h.png "24-tunnise kellaga aja juhtimise näide")

Järgmine toiming näitab näidet, kuidas lisada vormile kuupäeva ja kellaaja juhtelemente.

1. Lisage vormile kontroller iga kuupäeva ja kellaaja juhtelemendi jaoks, mida vorm peaks sisaldama. (Kontrollerite arv peab olema võrdne vormi kuupäeva ja kellaaja juhtelementide arvuga.)

    ```xpp
    private JmgProductionFloorExecutionDateTimeController  dateFromController; 
    private JmgProductionFloorExecutionDateTimeController  dateToController; 
    private JmgProductionFloorExecutionDateTimeController  timeFromController; 
    private JmgProductionFloorExecutionDateTimeController  timeToController;
    ```

1. Deklareerida nõutavad muutujad (tüübiga `utcdatetime`).

    ```xpp
    private utcdatetime fromDateTime;
    private utcdatetime toDateTime;
    ```

1. Looge meetodid, kus kuupäeva ja kellaaega värskendatakse kuupäeva ja kellaaja kontrollerite poolt. Järgmine näide näitab üht sellist meetodit.

    ```xpp
    private void setFromDateTime(utcdatetime _value)
        {
            fromDateTime = _value;
        }
    ```

1. Seadistage iga kuupäeva ja kellaaja kontrolleri käitumine ja ühendage iga kontroller vormiosaga. Järgmises näites kirjeldatakse, kuidas seadistada andmeid juhtelementide alguskuupäeva ja -kellaaja jaoks. Võite lisada sarnased koodi kuupäeva kuni ja kellaaja juhtelementide jaoks (ei kuvata).

    ```xpp
    /// <summary>
    /// Initializes all date and time controllers, defines their behavior, and connects them with the form parts.
    /// </summary>
    private void initializeDateControlControllers()
    {
        dateFromController = new JmgProductionFloorExecutionDateTimeController();
        dateFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        dateFromController.parmDateTimeValue(fromDateTime);
    
        timeFromController = new JmgProductionFloorExecutionDateTimeController();
        timeFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        timeFromController.parmDateTimeValue(fromDateTime);
        
        DateFromFormPart.getPartFormRun().setDateControlController(dateFromController, timeFromController);
        TimeFromFormPart.getPartFormRun().setTimeControlController(timeFromController, dateFromController);
        
        ...

    }
    ```

    Kui vajate ainult kuupäevakontrolli, võite aja juhtimise seadistuse vahele jätta ja seadistada kuupäevakontrolli, nagu näidatud järgmises näites.

    ```xpp
    {
        dateFromController = new JmgProductionFloorExecutionDateTimeController();
        dateFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        dateFromController.parmDateTimeValue(fromDateTime);
    
        DateFromFormPart.getPartFormRun().setDateControlController(dateFromController, null);
    }
    ```

## <a name="additional-resources"></a>Lisaressursid

- [Tootmisosakonna täideviimisliidese kujundamine](production-floor-execution-styles.md)
- [Tootmisosakonna täideviimisliidese kujundamine](production-floor-execution-tabs.md)
