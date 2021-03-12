---
title: Varude toimingute tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada varude toimingutega töötamisel tekkivaid probleeme.
author: sherry-zheng
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3a22229106753d265a90f0ef05f5ac82dc745bbd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967151"
---
# <a name="troubleshoot-inventory-operations"></a>Varude toimingute tõrkeotsing

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lahendada varude toimingutega töötamisel tekkivaid probleeme.

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>Ma ei leia varude töölehel ripploendi välja „Töövoog”.

### <a name="issue-description"></a>Probleemi kirjeldus

Te ei leia töölehelt ripploendi välja **Töövoog** või ei ole seotud töövoo toimingud saadaval.

See probleem võib esineda kolmel põhjusel, nagu kirjeldatud järgmistes alamjaotistes.

### <a name="issue-resolution-1"></a>Probleemi lahendus 1

Kui see probleem tekib kõigil kasutajatel, võib selle põhjuseks olla, et kinnitamise töövoog pole töölehe nimele määratud. Probleemi lahendamiseks tehke järgmist.

1. Avage **Varude haldus &gt; Seadistus &gt; Töölehtede nimed &gt; Varud**.
1. Valige sellel paanil töölehe nimi, et avada selle sätted.
1. Määrake kiirkaardi **Üldine** suvandi **Kinnituse töövoog** väärtuseks *Jah*. Kui teil palutakse muudatus kinnitada, klõpsake valikut **Jah**.
1. Väljal **Töövoog** valige töövoog, mida soovite valitud töölehe nime jaoks kasutada.

### <a name="issue-resolution-2"></a>Probleemi lahendus 2

Kui teie töövoog kasutab kohandatud koodi, võivad ilmneda probleemid pärast süsteemi täiendamist. Näiteks võidakse töölehe töövoos nupp **Esita** muutuda halliks, nii et te ei saa seda esitamise kinnitamiseks valida.

Kui nupp **Esita** on hall, on võimalik, et teie töövoog on kohandatud, mis tähendab, et töövoo meetodit `canSubmitToWorkflow()` atribuudis `FormDataUtil` laiendati. Selle probleemi lahendamiseks muutke viisi, kuidas te atribuudi `canSubmitToWorkflow()` meetodit laiendate, et kasutada järgmises näites.

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a>Probleemi lahendus 3

Kui probleem esineb vaid teatud kindlatel kasutajatel, ei pruugi nendel kasutajatel olla turvaõigusi, mis on vajalikud varude töölehtedel töövoo toimingute käivitamiseks. Veenduge, et igal mõjutatud kasutajal oleks turvalisuse privileeg *Varude töölehe töövoo haldamine*. Vaikimisi määratakse see privileeg kohustusele, mis on sama nimega, ja see kohustus rakendatakse rollidele *Laotöötaja* ja *Lao juhataja*.

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a>Minu varude tööleht jääb süsteemis lukus olekusse ja töövoo pakett-töö ei tööta.

### <a name="issue-description"></a>Probleemi kirjeldus

Üks teie varude töölehtedest on mingi toimingu poolt lukustatud ja seda ei vabastata. Näiteks kui sisestamisel (mis on süsteemi lukustustoiming) ilmneb tundmatu tõrge, võib tööleht jääda süsteemis lukus olekusse. Sel juhul kuvab töövoo tööüksuse ohjur tõrke, tehes samal ajal lukustuse kinnitamise.

### <a name="issue-resolution"></a>Probleemi lahendamine

Logige sisse Supply Chain Managementi SQL-serveri eksemplari ja kontrollige, kas **InventJournalTable.SystemBlocked** väärtuseks on määratud *1*. Kui on, siis veenduge, et tööleht ei oleks lukustatud olekus, ja lähtestage atribuut **inventJournalTable.SystemBlocked** väärtusele *0*.

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a>Minu varude töölehe töövoog ei ole kunagi lõpetatud ja töölehte ei saa redigeerida ega sisestada.

### <a name="issue-description"></a>Probleemi kirjeldus

Pärast töölehe kinnitamise töövoogu esitamist lõpetab töövoo töötlemine vastamise ja te ei saa oma töölehti redigeerida ega töödelda.

### <a name="issue-resolution"></a>Probleemi lahendamine

On mitu põhjust, miks töövoo töötlemine ei pruugi olla lõpule viidud. Kontrollige järgmiste probleemide suhtes.

- Avage **Laohaldus &gt; Seadistus &gt; Varude halduse töövood** ja vaadake üle mõjutatud töövoo konfiguratsioon. Lisateavet vt [Varude töölehe kinnitamise töövood](inventory-journal-workflow.md).
- Töövoos võib tekkida erand või tõrge. Vaadake üle mõjutatud töövoo tööüksuse ajalugu, et näha, kas see sisaldab rakenduse tõrget, mis lõpetab töövoo.
- Varude töölehte saab uuendada või redigeerida ainult siis, kui see on kinnitatud. Kui tagasikutsumine on aktiivne, võite proovida töölehte tagasi kutsuda. Töövoo pakett-töö käivitamine võib olla peatatud mitmel põhjusel. Mõned neist põhjustest võivad olla põhjustatud töövoo raamistiku probleemist.

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a>Varude töölehe töövoo tingimused kehtivad ainult töölehe tasemel, mitte rea tasemel

### <a name="issue-description"></a>Probleemi kirjeldus

Teil võib tekkida selline probleem, kui proovite näiteks seadistada varude töölehe töövoo tingimust kulusummale. Seadistate tingimuse nii, et 1. etappi käitatakse ainult siis, kui omahind on väiksem kui 100. Seejärel seadistate teise tingimuse nii, et 2. etappi käitatakse ainult siis, kui omahind on suurem või võrdne kui 100. Töövoo käivitamisel kuvatakse töövoo ajaloos ainult üks rida ja esimene tingimus hinnatakse alati *tõesena*, sõltumata edastatud väärtusest.

### <a name="issue-workaround"></a>Probleemi lahendus

Praeguses versioonis kehtivad varude töövoo tingimused ainult töölehe tasemel, mitte rea tasemel. Selline käitumine on nii kavandatud. Soovitame seada tingimuse kriteeriumiks ainult töölehe taseme atribuudid.

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a>Vaba kaubavaru loendilehe filtripaan ei filtreeri tulemusi nii, nagu ma eeldan.

### <a name="issue-description"></a>Probleemi kirjeldus

**Vaba kaubavaru** loendilehe filtripaani filtrid ei filtreeri tulemusi nii, nagu te eeldate.

### <a name="issue-resolution"></a>Probleemi lahendamine

Selline käitumine on nii kavandatud.

Leht  **Vaba kaubavaru** loend koostatakse üksikasjalikust vaba kaubavaru tabelist, mis sisaldab kõiki saadaolevaid dimensioone. Sellel lehel olev loend on aga vaid kokkuvõte. Seetõttu võidakse selles kombineerida lähtetabeli ridu, koondades väärtuseid kuvatud dimensioonide järgi.

Filtripaanil häälestatud filtrid rakenduvad lähtetabelile, mitte koondatud loendile. Selline käitumine võib mõnikord anda ootamatuid tulemusi, nagu näha [nendes näidetes](inventory-on-hand-list.md#examples).

Ruudustikus  [ruudustikus esitatud filtrid](inventory-on-hand-list.md#grid-filters) *siiski* rakenduvad koondatud loendile. Need filtrid hõlmavad nii kiirfiltrit ruudustiku ülaosas kui ka iga veerupäise filtrit.

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>Ühik ja ühiku kogus ei tööta varude töölehel õigesti.

### <a name="issue-description"></a>Probleemi kirjeldus

Varude töölehel üksuste ja kogustega töötades võite puutuda kokku ühe või mõlema probleemiga.

- Te ei näe varude töölehel ühikuid ega ühiku koguseid, kui väljastatud tootele on seadistatud teisendusühik, ja te ei saa ühikut varude töölehel muuta.
- Näete varude töölehel väljasid **Kogus** ja **Ühik**, kuid te ei näe välja **Ühiku kogus**. Kui muudate ühikut, sisestate koguse ja sisestate töölehe, kuvatakse töölehel siiski selle koguse algne mõõtühik.

### <a name="issue-resolution"></a>Probleemi lahendamine

Selle probleemi lahendamiseks tehke järgmist.

1. Kontrollige **funktsioonihalduse** tööruumis, et funktsioon *Mõõtühiku ja ühiku koguse kasutamine varude töölehtedel* oleks sisse lülitatud. See funktsioon lisab töölehele väljad **Ühik** ja **Ühiku kogus**.
1. Kui funktsioon on sisse lülitatud, kasutage välju **Kogus**, **Ühiku kogus** ja **Ühik** järgmisel viisil.

    - **Kogus** – määrake kogus, kasutades vaikeühikut, mis on vabastatud toote jaoks määratletud. Samas vaikeühikut ennast siin ei kuvata. Kui vaikeühiku ja väljal **Ühik** valitud ühiku vahel on häälestatud teisendus, uuendatakse välja **Kogus** väljade **Ühiku kogus** ja **Ühik** valikute alusel automaatselt.
    - **Ühiku kogus** – määrake kogus, kasutades ühikut, mis on valitud väljal **Ühik**.
    - **Ühik** – valige ühik, mida rakendada väljal **Ühiku kogus** määratud väärtusele.

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Mulle kuvatakse järgmine tõrketeade: „Varude arvestusühiku kümnendkohtade maksimumarv on 0.”

### <a name="issue-description"></a>Probleemi kirjeldus

Kui proovite sisestada laokannet või varude reserveerimist, kuvatakse järgmine tõrketeade: „Varude arvestusühiku kümnendkohtade maksimumarv on 0.”

See probleem ilmneb, kui laokanmete kogus on määratud kümnendväärtusena, mis on allpool täpsustaset, mida väli toetab. Näiteks on laokande jaoks määratud kogus *0,5*, kuid toetatakse ainult täisarvukoguseid. Seetõttu peab väärtus olema *0,5* asemel *1*.

### <a name="issue-resolution"></a>Probleemi lahendamine

1. Käivitage oma SQL-serveri eksemplaris järgmine skript, et ümardada laokannetes kogused. See skript parandab väärtused tabelis **inventTrans**.

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. Käivitage vaba kaubavaru järjepidevuse kontroll, kus valik **paranda tõrge** on sisselülitatud. See kontroll parandab väärtused tabelis **inventSum**.

> [!IMPORTANT]
> Soovitame tungivalt, et redigeeriksite skripti hoolikalt vastavalt oma keskkonnale, katsetaksite seda katsekeskkonnas ning seejärel kontrolliksite saadud andmeid enne skripti käivitamist tootmiskeskkonnas.
