---
title: Arveldusgraafikute lõpetamine
description: See teema kirjeldab, kuidas lõpetada arveldusgraafikud ja arveldusgraafiku read kordustellimuse arvelduses.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: e823ce950d6a4687dc7cda14e06bffdbb4f37f7e
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690972"
---
# <a name="terminate-billing-schedules"></a>Arveldusgraafikute lõpetamine

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas lõpetada arveldusgraafikud ja arveldusgraafiku read kordustellimuse arvelduses. Arveldusgraafiku lõpetamisel peab selle olek olema **Aktiivne**. Selle olek ei saa olla **Ootel**. Samamoodi, kui lõpetate arveldusgraafiku rea, peab selle olek olema **Aktiivne**. Arveldusgraafiku rea lõpetamisel ei mõjutata arveldusgraafiku päisejaost.

Arveldusgraafiku või arveldusgraafiku rea lõpetamiseks minge ühte järgmistest kohtadest:

- Kõigi **/aktiivsete arveldusgraafikute loendileht**
- Kindel arveldusgraafik lehel **Kõik arveldusgraafikud**
- Kindel arveldusgraafiku rida lehel Kõik **arveldusgraafikud**

> [!NOTE]
> Kui soovite lõpetada korraga mitu arveldusgraafikut, kasutage massilise lõpetamise **töötlemise lehte**.

## <a name="terminate-a-billing-schedule-or-line"></a>Arveldusgraafiku või reaga lepingu loomine

Arveldusgraafiku või arveldusgraafiku rea lõpetamiseks järgige neid samme.

1. Valige arveldusgraafik või arveldusgraafiku rida ja seejärel valige **Lõpeta**. 
2. Seadke väljad **Lõpetamiskuupäev**, **Lõpetamise** tüüp **ja Põhjuse** kood.
3. Krediidi valikuvälja **väärtuseks** määrake Krediidi **väljaminek**.
4. Valige Lõpeta **.**

Valitud lõpetamise tüübil põhinev arveldusgraafiku olek muutub. Kui valisite **lõpetamise tüübiks** allesjäänud arve, on kõikide arveldusgraafiku ridade olek Viimane **arveldus**. Arveldusgraafiku olek jääb aktiivseks **kuni** viimase arve töötlemiseni. Pärast viimase arve töötlemist uuendatakse olek olekuks **Lõpetatud**. Kui valisite **lõpetamise tüübiks** Korrigeeri graafikut, uuendatakse arveldusgraafiku olek kohe lõpetatud **olekuks**.

## <a name="terminate-a-billing-schedule-or-line-and-apply-a-refund"></a>Lõpetage arveldusgraafik või rida ja rakendage tagasimakse.

Arveldusgraafiku või arveldusgraafiku rea lõpetamiseks ja tagasimakse rakendamiseks järgige neid samme.

1. Valige arveldusgraafik või arveldusgraafiku rida ja seejärel valige **Lõpeta**.
2. Seadke väljad **Lõpetamiskuupäev**, **Lõpetamise** tüüp **, Põhjuse** kood ja **Kreedit**.
3. Valige lõpeta **tagasimaksega**. Kuvatakse **mass-lõpetamise** töötlusleht ja seda filtreeritakse nii, et see näitab arveldusgraafikut.
4. Valige **arveldusgraafiku** ridade vaatamiseks eelvaade ja seejärel valige **Suvand Töötle**.

Pärast krediidi töötlemist avage arvelduse üksikasjade **leht**, et üle vaadata krediiti, mida arveldusgraafikule rakendati. Kui kreeditsumma on suurem kui 0 (null), kustutatakse kõik tulevased arveldamata read ja asendatakse arvelduse üksikasjaridadega, mis näitavad negatiivseid summasid kreediti puhul, mis rakendati arveldusgraafikule.

### <a name="view-example"></a>Kuva näide

Arveldusgraafikul on järgmine teave:

- Alguskuupäev on 1. jaanuar 2020.
- Lõppkuupäev on 31. detsember 2020.
- Arveldusperioodi summa on 100,00 eurot kuus.
- Arved on loodud arveldusperioodideks jaanuarist juulini.
- Lepingu lõpetamise kuupäev on 15. juuni 2020.

Kreediti korrigeerimise töötlemisel eemaldatakse lehelt Kuva arvelduse üksikasjad kõik tulevased arveldusperioodid (**august kuni detsember**). Kreediti korrigeerimise rida lisatakse pärast juuli arveldusperioodi:

- 16. juuni – 31. juuli, kreeditsummaga 150,00

Kui kasutatakse tasumata tulu funktsiooni, **värskendatakse tasumata tulu** töölehe sisestamise auditi lehekülge lõpetamise kandega.

## <a name="terminate-a-billing-schedule-or-line-without-applying-a-credit"></a>Lõpeta arveldusgraafik või rida ilma krediiti rakendamata

Arveldusgraafiku või arveldusgraafiku rea lõpetamiseks ilma krediiti rakendamata, järgige neid samme.

1. Valige arveldusgraafik või arveldusgraafiku rida ja seejärel valige **Lõpeta**.
2. Seadke lõpetamise **kuupäeva väli**.
3. Seadke välja Lõpetamistüüp **väärtuseks** Korrigeerimata **·**. Välja **Kreedit väärtus** seatakse automaatselt väärtusele Kreedit **puudub**.
3. Seadke väli **Põhjuse** kood.
4. Sisestage **väljale Lõpetamismärkused** nõutavad märkused.
5. Valige Lõpeta **.** 

Lõpetamise töötlemisel eemaldatakse kõik arvelduse üksikasjaread pärast lõpetamise kuupäeva. (Need read sisaldavad rida, mis sisaldab lõpetamise kuupäeva.) Lõpetatud ridade kohta ei saa arveid luua. Lõpetamise eemaldamisel lisatakse kõik lõpetatud read tagasi **lehele Kuva arvelduse** üksikasjad ja muutuvad arveldamiseks kättesaadavaks.

## <a name="fields"></a>Väljad

Lehel **Kuva arvelduse üksikasjad** on järgmised väljad.

| Väli | Kirjeldus |
|-------|-------------| 
| Lõpetamiskuupäev | Valige kuupäev, millal soovite lõpetada arveldusgraafiku või arveldusgraafiku rea. |
| Lõpetamise tüüp | <p>Valige lõpetamise tüüp:</p><ul><li>**Graafiku** korrigeerimine: katkestage rea arveldusperioodid lõpetamise kuupäeval ja muutke rea olekuks Viimane **arveldus**. Kui reaüksusel on olemas viitvõla graafik, korrigeeritakse seda summa võrra, mis ei pea enam tuvastama. Kui arvelduse alguskuupäev on pärast lõpetamise kuupäeva, eemaldatakse arveldusperioodi jääk.</li><li>**Arve jääk** : lisage arveldusperioodile järelejäänud summad ja muutke rea olekuks Viimane **arveldus**. Kui reaüksuse kohta on olemas viitvõla graafik, uuendatakse viitvõla lõppkuupäeva. Kui arvelduse alguskuupäev on pärast lõpetamise kuupäeva, lisatakse arveldusperioodile kõigi järelejäänud arveldusperioodide kogusumma ja järelejäänud arveldusperioodid eemaldatakse.</li><li>**Korrigeerimine** puudub – lõpetage rea arveldusperioodid määratud lõpetamiskuupäeval. Ühtegi korrigeerimist ei ole tehtud. Kui on valitud selle lõpetamise tüüp, **on välja** **·** **Kreedit väärtuseks seatud Kreediti kreedit ja päevane** ergas väli on seatud väärtusele **Ei.** Mõlemad väljad muutuvad kirjutuskaitstuks ja neid ei saa muuta.</li></ul> |
| Krediidi valik | <p>Valige, kuidas krediiti arveldusgraafiku rea lõpetamisel rakendatakse:</p><ul><li>**Kreediti** korrigeerimine: looge arveldusgraafiku kreediti korrigeerimine, kui rida lõpetatakse. Kreediti korrigeerimine ilmub arveldusgraafiku tulevases arveldusperioodis. Korrektsioon korrigeerib automaatselt ka arve summat järgmiseks arveldusperioodiks, kuni krediiti on arveldusgraafikule rakendatud.</li><li>**Väljasta** krediit – looge kreeditarve, kui arveldusgraafik või arveldusgraafiku rida on lõpetatud.</li><li>**Kreedit puudub** – ärge looge kreediti korrigeerimist ega kreeditarvet, kui arveldusgraafik või arveldusgraafiku rida on lõpetatud. See valik on saadaval ainult siis, kui kasutate arveldusgraafiku **lõpetamiseks** korrigeerimistüübi Korrigeerimata lõpetamist.</li></ul><p>Vaikevalik on pärit korduva lepingu **arveldusparameetrite lehelt**.</p> |
| Põhjuse kood | Valige lõpetamise põhjuse kood. |
| Põhjuse kirjeldus | Põhjusekoodi kirjeldus. |
| Lõpetamise märkmed | Sisestage lepingu lõpetamise kohta märkused. |

<!--## Additional information-->
