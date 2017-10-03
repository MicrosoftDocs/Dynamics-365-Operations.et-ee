---
title: "Lao tööpoliitikad"
description: "Laotöö poliitikad juhivad seda, kas laotöö luuakse tootmises laoprotsessidega töötellimuse tüübi, varude asukoha ja toote põhjal."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 9262dcaa3b326d8c31b7d7416b102920795da94b
ms.openlocfilehash: 7612003bc20f91f173629893750478b034cff27b
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017

---

# <a name="warehouse-work-policies"></a>Lao tööpoliitikad

[!include[banner](../includes/banner.md)]


Laotöö poliitikad Microsoft Dynamics 365 for Finance and Operations, Enterprise editionis juhivad seda, kas laotöö luuakse tootmises laoprotsessidega töötellimuse tüübi, varude asukoha ja toote põhjal.

See tööpoliitika kontrollib, kas laotöö luuakse tootmises laoprotsesside jaoks. Saate seadistada tööpoliitika, kasutades **töötellimuse tüüpide**, **lao asukoha** ja **toote** kombinatsiooni. Näiteks toode L0101 teatatakse väljundasukohas 001 lõpetatuks. Lõpetatud kaupa tarbitakse hiljem teises tootmistellimuses väljastuskohaga 001. Sellisel juhul saate seadistada tööpoliitika, et takistada lõpetatud kaupade kõrvalepaneku jaoks töö loomist, kui teatate toote L0101 väljastuskohas 001 lõpetatuks. Tööpoliitika on individuaalne üksus, mida saab kirjeldada järgmise teabe kaudu.

-   **Tööpoliitika nimi**(tööpoliitika kordumatu identifikaator)
-   **Töötellimuse tüübid** ja **Töö loomise meetod**
-   **Lao asukohad**
-   **tooted.**

## <a name="work-order-types"></a>Töötellimuse tüübid
Saate valida järgmised töötellimuse tüübid.

-   Lõpetatud kaupade kõrvalepanek
-   Kaastoodete ja kõrvalsaaduste kõrvalepanek
-   Toormaterjalide komplekteerimine

Väljal **Töö loomise meetod** on väärtus **Mitte kunagi**. See väärtus näitab, et tööpoliitika takistab laotöö loomist valitud töötellimuse tüübi jaoks.

## <a name="inventory-locations"></a>Lao asukohad
Saate valida asukoha, millele tööpoliitika rakendub. Kui tööpoliitikaga ei seostu ühtki asukohta, siis ei rakendu tööpoliitika ühelegi protsessile. Lehel **Asukohad** saate ka valida või tühistada tööpoliitika valimise teatud asukohas.

## <a name="products"></a>Tooted
Saate valida toote, millele tööpoliitika rakendub. Saate rakendada tööpoliitika kõikidele toodetele või valitud toodetele.

## <a name="example"></a>Näide
Järgmises näites on kaks tootmistellimust: PRD-001 ja PRD-00*2*. Tootmistellimusel PRD-001 on toiming nimega **Assembler**, kus toode SC1 on teatatud lõpetatuks asukohale O1. Tootmistellimusel PRD-002 on toiming nimega **Värvimine** ja tarbib toodet SC1 asukohast O1. Tootmistellimus PRD-002 tarbib ka toormaterjali RM1 asukohast O1. RM1-d hoitakse laoasukohas BULK-001 ja komplekteeritakse asukohale O1 laotööga toormaterjali komplekteerimiseks. Komplekteerimistöö luuakse tootmise PRD-002 väljastamisel. 

[![Lao tööpoliitikad](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png) 

Kui plaanite selle stsenaariumi jaoks konfigureerida lao tööpoliitika, peaksite arvestama järgmist teavet.

-   Laotöö pole lõpetatud kaupade kõrvalepanekuks vajalik, kui teatate toote SC1 lõpetatuks tootmistellimusest PRD-001 asukohale O1. Seda seetõttu, et tootmistellimuse PRD-002 toiming **Värvimine** tarbib samas asukohas SC1.
-   Laotöö on toormaterjali komplekteerimiseks vajalik, et liigutada toormaterjali RM1 laoasukohast BULK-001 asukohta O1.

Siin on näide tööpoliitikast, mida saate nende kaalutluste põhjal seadistada.

|                                         |                                                       |
|-----------------------------------------|-------------------------------------------------------|
|**Tööpoliitika nimi**<br>                 |**Töökäsu tüübid**<br>                               |
| Kõrvalepanekuta 01     `                    |- Lõpetatud kaupade kõrvalepanek<br>                           |
|                                         |**Asukohad**<br>                                      |
|                                         |- O1   |                                               |
|                                         |**Tooted** <br>                                      |
|                                         |- SC1                                                  |

Järgmised protseduurid annavad etapiviisilise juhise, kuidas seadistada selle stsenaarium jaoks laotöö poliitikat. Samuti on kirjeldatud näidisseadistust, mis näitab, kuidas teatada tootmistellimus lõpetatuks asukohale, mis pole litsentsiplaadiga kontrollitav.

## <a name="set-up-a-warehouse-work-policy"></a>Lao tööpoliitika seadistamine
Laotoimingud ei hõlma alati laotööd. Tööpoliitika määratlemisel saate vältida töö loomist toormaterjali komplekteerimise puhul ja lõpetatud kaupade ladustamist toodete kogumi puhul kindlates asukohtades. Selle protseduuri loomiseks kasutati demoettevõtte USMF andmeid. 

ETAPID (21)

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| 1.  | Minge asukohta Laohaldus &gt; Seadistus &gt; Töö &gt; Tööpoliitikad.        |
| 2.  | Klõpsake valikut Uus.                                                                 |
| 3.  | Tippige välja Tööpoliitika nimi väärtus Ladustamitööd ei ole.                    |
| 4.  | Klõpsake nuppu Salvesta.                                                                |
| 5.  | Klõpsake vahekaarti Lisa.                                                                 |
| 6.  | Märkige loendis valitud rida.                                        |
| 7.  | Tehke väljal Töötellimuse tüüp valik Lõpetatud kaupade kõrvalepanek.            |
| 8.  | Klõpsake vahekaarti Lisa.                                                                 |
| 9.  | Märkige loendis valitud rida.                                        |
| 10. | Tehke välja Töötellimuse tüüp valik Kaastoodete ja kõrvalsaaduste kõrvalepanek. |
| 11. | Laiendage jaotist Lao asukohad.                                    |
| 12. | Klõpsake vahekaarti Lisa.                                                                 |
| 13. | Märkige loendis valitud rida.                                        |
| 14. | Sisestage loendisse Ladu väärtus 51.                                         |
| 15. | Sisestage või valige väljal Asukoht väärtus 001.                              |
| 16. | Laiendage jaotist Tooted.                                               |
| 17. | Tehk väljal Toote valimine valik Valitud.                         |
| 18. | Klõpsake vahekaarti Lisa.                                                                 |
| 19. | Märkige loendis valitud rida.                                        |
| 20. | Sisestage või valige väljal Kaubakood väärtus L0101.                         |
| 21. | Klõpsake nuppu Salvesta.                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>Teatage tootmistellimus lõpetatuks asukohale, mis pole litsentsiplaadiga kontrollitud
Selles protseduuris esitatakse näide lõpetatuks kuulutamisest mittelitsentsiplaadiga kontrollitava asukoha jaoks. Selle ülesande eeltingimus on kehtiv tööpoliitika. Eelmine protseduur näitab tööpoliitika seadistust. 

ETAPID (25)

<table>
<tbody>
<tr>
<td colspan="3"><strong>Alamülesanne: väljundi asukoha seadistamine.</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>Avage Organisatsiooni haldus &gt; Ressursid &gt; Ressursigrupid.</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>Valige loendist ressursigrupp 5102.</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>Klõpsake nuppu Redigeeri.</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>Sisestage väljale Väljastusladu väärtus 51.</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>Sisestage väljale Väljundi asukoht väärtus 001.</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>Asukoht 001 pole litsentsiplaadiga juhitav asukoht. Saate seadistada mittelitsentsiplaadi väljundi asukoha ainult siis, kui asukohale on olemas vastav tööpoliitika.</td>
</tr>
<tr>
<td colspan="3"><strong>Alamülesanne: tootmistellimuse loomine ja selle lõpetatuna kinnitamine.</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>Sulgege leht.</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>Avage Tootmise juhtimine &gt; Tootmistellimused &gt; Kõik tootmistellimused.</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>Klõpsake valikut Uus tootmistellimus.</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>Sisestage väljale Kauba kood väärtus L0101.</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>Klõpsake käsku Loo.</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>Klõpsake toimingupaanil valikut Tootmistellimus.</td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td>Klõpsake suvandit Hinnang.</td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td>Klõpsake nuppu OK.</td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td>Klõpsake käsku Käivita.</td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td>Klõpsake vahekaarti Üldine.</td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td>Tehke väljal Automaatne koosluse tarbimine valik Mitte kunagi.</td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td>Klõpsake nuppu OK.</td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td>Klõpsake valikut Kinnita lõpetamine.</td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td>Klõpsake vahekaarti Üldine.</td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td>Tehke väljal Aktsepteeri viga valik Jah.</td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td>Klõpsake nuppu OK.</td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td>Klõpsake toimingupaanil valikut Ladu.</td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td>Klõpsake suvandit Töö üksikasjad.</td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td>Kui tootmistellimus on lõpetatuks kuulutatud, pole ladustamiseks tööd loodud. See ilmneb, kuna määratletud on tööpoliitika, mis takistab töö loomist, kui toode L0101 kuulutatakse lõpetatuks asukohale 001.</td>
</tr>
</tbody>
</table>




