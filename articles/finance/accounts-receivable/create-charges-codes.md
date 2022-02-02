---
title: Kulude koodide loomine
description: See teema kirjeldab, kuidas konfigureerida kulude koode nii ostureskontro kui ka müügireskontro jaoks.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MarkupTable
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 034be190890a67fd0921d40fffdc704b9d6d5df7
ms.sourcegitcommit: 5bfd6511d710deb539b4030eb0e9c48d25513595
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/19/2022
ms.locfileid: "8014104"
---
# <a name="create-charges-codes"></a>Kulude koodide loomine

See teema kirjeldab, kuidas konfigureerida kulude koode nii ostureskontro kui ka müügireskontro jaoks. Kui teie organisatsioon nõuab, et lisaks müügitellimuse või ostutellimuse rea kaupadele jälgitakse müügisummasid või ostusummasid, saate selleks kasutada kulude koode. Näiteks maksate veose ja kindlustuse ostutellimusel ning need summad esitatakse ostutellimusel eraldi. Sel juhul saate määrata, kas summad sisestatakse kulukontodele või lisatakse kaupade kuludele.

## <a name="set-up-charges-codes-for-accounts-receivable"></a>Müügireskontro kulude koodide seadistamine

Müügireskontro jaoks kulude koodide loomiseks järgige neid samme.

1. Minge **müügireskontro** &gt; **kulude seadistuse** &gt; **kulude koodi**.
2. Valige suvand **Uus**.
3. Sisestage **tasukood** väljale Tasukood.
3. Sisestage **kulu** kirjeldus väljale Kirjeldus.
4. Valikuline: **valige väljal** Kauba käibemaksugrupp käibemaksugrupp.
5. Määrake **kiirkaardil** Sisestamine, kuidas tasu automaatselt debiteerida ja krediteerida.
6. Kui valisite deebeti tüübiks või kreediti tüübiks Pearaamatukonto, määrake sisestustüübiks sisestusväljad ja **määratlege** **·** **põhikonto** kontoväljadel.

### <a name="example"></a>Näide

Tasu maksab klient. Seetõttu lisatakse see müügitellimuse kogusummadele. Seadistate järgmise sisestamisteabe:

- Valige **jaotises** Deebet väljal Tüüp **suvand** **Klient/Hankija,** et lisada arve tasu kliendi kontole.
- Jaotises Kreedit väljal Tüüp **valige** **·** **pearaamatukonto**. Seejärel valige **väljal** Konto arvekuludest tulu põhikonto.

> [!NOTE]
> Kui valitud koodi deebeti tüüp või kreediti tüüp on kas Pearaamatukonto või Kaup, saate **·** **kulukande** jaoks sisestada muu valuuta.

Tasu teksti saate printida kliendile määratud keeles. Kulude koodi teksti määramiseks teistes keeltes valige suvand **Tõlked**.

## <a name="set-up-charges-codes-for-accounts-payable"></a>Ostureskontro kulude koodide seadistamine

Ostureskontro jaoks kulude koodide loomiseks järgige neid samme.

1. Järgige üht neist sammudest.

    - Minge **ostureskontro** &gt; **kulude** **seadistuse** &gt; **kulude** koodi.
    - Minge hanke **kulude häälestuse** &gt; **·** &gt; **·** &gt; **koodile**.

2. Valige suvand **Uus**.
3. Sisestage **tasukood** väljale Tasukood.
3. Sisestage **kulu** kirjeldus väljale Kirjeldus.
4. Valikuline: **valige väljal** Kauba käibemaksugrupp käibemaksugrupp.
5. Valikuline: **sisestage** väljale Suurim summa maksimumsumma, mis on kulude koodi puhul lubatud.

    Seda välja kasutatakse hankija arvete tasude kontrollimiseks. Tasude kinnitamise lubamiseks märkige lehe Ostureskontro parameetrid vahekaardil Arve kinnitamine ruut Luba **arvete** **·** **vastendamine**.

    > [!IMPORTANT]
    > Arvete tasude kinnitamiseks peate looma ka poliitika reegli tüübi eksemplari, mis põhineb kindla hankija arve poliitika kuludel.

6. Määrake **kiirkaardil** Sisestamine, kuidas tasu automaatselt debiteerida ja krediteerida.
7. Kui valisite deebeti tüübiks või kreediti tüübiks Pearaamatukonto, määrake sisestustüüp Deebeti sisestus- ja kreediti sisestusväljad ning määratlege põhikonto deebetkonto **ja** **·** **·** **·** **kreeditkonto** väljadel.
8. Kuluväärtuste võrdluse võimaldamiseks arvel, mis sisaldab vastava ostutellimuse päise või ridade kulusid, märkige ruut Võrdle ostutellimuse ja **arve** väärtusi.

### <a name="example"></a>Näide

Saate kirjendada tasu kuluna osana ostutellimuse või hankija arve kogusummast. Järgige neid samme sisestamisteabe häälestamiseks. 

- Jaotises **Kreedit** valige väljal Tüüp **suvand** **Klient/Hankija,** et lisada arve tasu hankija kontole.
- Valige **jaotises** Deebet väljal Tüüp väärtus **Pearaamatu** **konto**. Seejärel valige **väljal** Konto arve kulude põhikonto.

Järgige neid samme sisestamisteabe seadistamiseks nii, et ühiku kulu lisatakse kaubakulule.

- Jaotises **Kreedit** valige väljal Tüüp **suvand** **Klient/Hankija,** et lisada arve tasu hankija kontole.
- Valige **jaotises** Deebet väljal Tüüp **suvand** **Kaup, et lisada** kaubakulule kulu.

> [!NOTE]
> Võib-olla soovite kasutada valuutat, mis erineb ostutellimusel või arvel määratud valuutast. Kui valitud koodi deebeti tüüp või kreediti tüüp on kas Pearaamatukonto või Kaup, saate **sisestada erineva** **valuuta**.

Tasu teksti saate printida kliendile määratud keeles. Kulude koodi teksti määramiseks teistes keeltes valige suvand **Tõlked**.
