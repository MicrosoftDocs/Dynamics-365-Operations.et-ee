---
title: Seadista ja loo elektroonilise aruandluse abil positiivsed maksefailid
description: See artikkel selgitab, kuidas seadistada positiivset makset elektroonilise aruandluse abil.
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 491048c7274ba6bb52e0a4b7a6ea5cd0f5ff4741
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878214"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Seadistage elektroonilise aruandluse abil positiivsed maksefailid

See artikkel selgitab, kuidas seadistada positiivset makset ja luua elektroonilise aruandluse abil positiivsed maksefailid.

> [!NOTE] 
> Enne panga positiivse **maksefaili funktsiooni** kasutamist peate esmalt üksuseloendit värskendama.
> Avage jaotise **Andmehaldus > Importimine/eksportimine > Raamistiku parameetrid** 
> kiirkaart **Üksuse sätted**, valige **Värskenda üksuste loendit**.


Positiivse makse seadistamine pangale edastatava elektroonilise tšekkide loendi loomiseks. Kui tšekk esitatakse pangale, võrdleb pank seda tšekkide loendiga. Kui tšekk vastab loendis olevale tšekile, maksab pank selle välja. Kui tšekk ei vasta ühelegi loendis olevale tšekile, võtab pank selle ülevaatamiseks enda kätte.

## <a name="security-for-positive-pay-files"></a>Positiivse makse failide turve
Positiivse makse failides võib olla tundliku loomuga teavet maksesaajate ja tšekisummade kohta. Seetõttu kasutage kindlasti vajalikke turvameetmeid alates failide loomise hetkest kuni nende panka saabumiseni. Positiivse makse failid laaditakse alla teie veebibrauseri määratud asukohta. Kuna positiivsed maksefailid võivad sisaldada tundliku loomuga teavet, Microsoft Dynamics on oluline, et selle teabe loomiseks ja vaatamiseks on oluline ainult volitatud kasutajatel 365 Finantsid. Järgmise tabelis abil saate määratleda vajalikke õigusi.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ülesanne</th>
<th>Eesõigus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Saate luua positiivse makse faile loendilehelt <strong>Pangakontod</strong> või lehelt <strong>Pangakontod</strong>.</td>
<td><ul>
<li><strong>Panga positiivse makse teabe haldamine</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="even">
<td>Positiivse makse failide loomine juriidiliste isikute ning pangakontode jaoks lehelt <strong>Loo positiivne maksefail</strong>.</td>
<td><ul>
<li><strong>Panga positiivse makse teabe haldamine</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Positiivseid maksefaile saab vaadata lehelt <strong>Positiivse maksefaili kokkuvõte</strong>.</td>
<td><strong>Vaata panga positiivset makseteavet mitme juriidilise isiku kohta</strong> (BankPositivePayView)</td>
</tr>
<tr class="even">
<td>Positiivse maksefaili saab kinnitada lehelt <strong>Positiivse maksefaili kokkuvõte</strong>.</td>
<td><strong>Kinnita positiivne maksefail</strong> (BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td>Positiivse maksefaili saab tagasi võtta lehelt <strong>Positiivse maksefaili kokkuvõte</strong>.</td>
<td><strong>Positiivse makse faili tagasivõtmine</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-the-electronic-reporting-configuration"></a>Elektroonilise aruandluse konfiguratsiooni seadistamine

1. Minge tööruumide **elektroonilise aruandluse \> juurde**.
2. Microsofti konfiguratsioonipakkuja paanil **valige** hoidlad **·**.
3. Valige **Globaalne** ja seejärel valige **Ava**.
4. Kui tuleb luua ühendus hoidlaga, valige dialoogiaknast sinine link.
5. Leidke ja valige konfiguratsiooniloendist Positiivne **maksemudel Positiivne \> maksevorming**.
6. Valige kiirkaardil **Versioonid** uusim versioon ja seejärel käsk **Impordi**.

## <a name="set-up-a-positive-pay-format"></a>Positiivse maksevormingu seadistamine

1. Avage sularaha- **ja pangahalduse seadistuse positiivse \> makse \> vormingud**.
2. Valige suvand **Uus**.
3. Seadistage **maksevorming** ja kirjelduse **väljad**.
4. Märkige ruut **Üldine elektrooniline ekspordivorming**.
5. Seadke konfiguratsioonivälja **Ekspordivorming** väärtuseks Positiivne **maksevorming**.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Määrake pangakontole positiivne maksevorming.
Iga pangakonto puhul, millele soovite positiivset makseteavet luua, tuleb määrata eelmises osas kirjeldatud positiivse makse vorming. Valige lehelt Pangakontod arvele vastav positiivse makse vorming. Sisestage väljale **Positiivse makse alguskuupäev** esimene kuupäev positiivse makse failide loomiseks. 

>[!Important]
> Sisestage kuupäev väljale **Positiivse makse** alguskuupäev. Kui see tühjaks jätta, sisaldab esimene positiivne maksefail kõiki selle pangakonto jaoks loodud tšekke.

1. Minge sularaha **- ja pangahalduse pankade \> pangakontodele \>**.
2. Avage pangakonto.
3. Seadke kiirkaardil **Üldine** positiivse makse **vormingu väli** varem loodud vormingusse.
4. Seadke välja **Positiivse makse alguskuupäev** praegusele kuupäevale.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Numbriseeria määramine positiivse makse failidele
Igal positiivse makse failil peab olema kordumatu number. Looge sularaha **ja panga halduse parameetrite** lehel numbriseeria positiivsete maksefailide jaoks **numbriseeria vahekaardil** Numbriseeriad.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Ühe pangakonto jaoks positiivse makse faili loomine
Saate luua positiivse makse faili üksikule juriidilisele isikule ja üksikule pangakontole. Teavet positiivse makse failide loomise kohta korraga mitmele juriidilisele isikule ja pangakontole leiate järgmisest osast. Positiivse maksefaili loomiseks ühele juriidilisele isikule ja ühele pangakontole avage dialoogiboks **Positiivse maksefaili loomine** lehelt **Pangakontod**. Sisestage väljale **Katkestuskuupäev** viimase tšeki kuupäev, et lisada see positiivsele maksefailile. Kõik tšekid, mida ei ole lisatud positiivsele maksefailile selle tšeki kuupäeva lõpuks, lisatakse faili.

1. Avage sularaha **- ja pangahalduse \> pangakontod \>**.
2. Avage pangakonto, mille jaoks on seadistatud positiivne makse.
3. Valige halda **maksete positiivse \> makse positiivse \> makse faili**.
4. Seadke välja **katkestamise** kuupäev. Kaasatakse enne seda kuupäeva loodud tšekid.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Mitme pangakonto jaoks positiivse makse faili loomine
Mitme pangakonto jaoks positiivse maksefaili loomiseks kasutage perioodilist ülesannet **Positiivne** maksefail. Valige failile positiivne maksevorming ja määrake, kas luua fail kõikidele juriidilistele isikutele või valitud juriidilisele isikule. Saate luua positiivse maksefaili ka kõikidele pangakontodele, mis kasutavad positiivset maksevormingut, või valitud pangakontole. Sisestage väljale **Katkestuskuupäev** viimase tšeki kuupäev, et lisada see positiivsele maksefailile. Kõik tšekid, mida ei ole lisatud positiivsele maksefailile selle tšeki kuupäeva lõpuks, lisatakse faili.

## <a name="view-the-results-of-positive-pay-file-generation"></a>Positiivse maksefaili loomise tulemuste vaatamine
Pärast seda, kui positiivne maksefail on loodud, saate vaadata tulemusi lehel **Positiivse maksefaili kokkuvõte**. Üksikute tšekkide üksikasjade vaatamiseks minge lehele Positiivse **maksefaili üksikasjad**.

## <a name="confirm-a-positive-pay-file"></a>Positiivse maksefaili kinnitamine
Kui positiivses maksefailis loetletud tšekid on tasutud, saate pangast kinnituskoodi. Seejärel saate positiivse maksefaili kinnitada. Valige lehelt **Positiivse maksefaili kokkuvõte** positiivne maksefail, mille olek on **Loodud**, ja valige siis toiming **Sisesta kinnitus**. Positiivse maksefaili kinnitamisel salvestatakse pangast saadud kinnituskood.

## <a name="recall-a-positive-pay-file"></a>Positiivse makse faili tagasikutsumine
Kui peate positiivse makse faili muutma, saate selle tagasi kutsuda. Valige lehelt **Positiivse maksefaili kokkuvõte** positiivne maksefail, mille olek on **Loodud**, ja valige siis toiming **Võta tagasi**. Igas positiivse makse failis oleva tšeki puhul lähtestatakse väli, mis näitab, kas see tšekk on olnud positiivse makse faili lisatud. Siis saate luua uue positiivse maksefaili, mis sisaldab tagasi võetud tšekki.


Tulemuseks saadav XML-fail laaditakse alla.
