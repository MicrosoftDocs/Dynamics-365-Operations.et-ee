---
title: Muudetud summad Kuva aruanded ja dokumendid
description: "See teema pakub teavet värskendada summad Kuva aruanded ja muud dokumendid Eesti, Läti, Leedu, Poola, Tšehhi, Ungari ja Venemaa."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264254
ms.assetid: 70b32d8d-6fa7-4617-ba74-a74bc6568d6e
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 870341b81e49c9fc677052e9ef87a580892f486f
ms.lasthandoff: 03/31/2017


---

# <a name="update-how-amounts-are-displayed-on-reports-and-documents"></a>Muudetud summad Kuva aruanded ja dokumendid

See teema pakub teavet värskendada summad Kuva aruanded ja muud dokumendid Eesti, Läti, Leedu, Poola, Tšehhi, Ungari ja Venemaa.

Aastal Eesti, Läti, Leedu, Poola, Tšehhi, Ungari ja Venemaa juriidiliste, seadistage täisnimi ja lühikesed sõnad rahaühikud ja allüksustes. Neid nimesid saab muuta, kuidas summad esitatakse dokumendid ja aruanded. Näiteks: summa **LTL 100.20** võib kuvada **100 litti 20 Centas**.

## <a name="set-up-full-and-short-names-for-currency-units-and-subunits"></a>Täis- ja rahaühikud ja allüksustes nimede seadistamine
Täis- ja nimed rahaühikud ja allüksused keele seadistamiseks täitke järgmised juhised:

1.  Avatud on **valuutade** lehel.
2.  Valige valuuta.
3.  Kohta ning tegevus paanil klõpsake **käänamine**.
4.  Täisnimi ja lühinimi keele lisamiseks klõpsake **uus** ja täitke järgmised väljad.
    |                                                           |                                                                                                                                                                                                                    |
    |-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **Field**                                                 | **Description**                                                                                                                                                                                                    |
    | **Language**                                              | Valige praeguse teksti keel.                                                                                                                                                                          |
    | **Ainsuse nimetav (ühikut väljagrupi nimi)**       | Sisestage valuuta ainsuse vormi. Näiteks litt ainsuse vorm on litt.                                                                                                                         |
    | **Mitmuse nimetav (ühikut väljagrupi nimi)**         | Sisestage valuuta mitmuses. Näiteks sisestage Litai. **Märkus**: selle **ainsuse omastavas** ja **mitmuse omastav** väljad on saadaval jaotises keeles on **keele** välja. |
    | **Ainsuse nimetavas välja (osad väljagrupi nimi)** | Sisestage valuuta ribosoomi ainsuse vormi.                                                                                                                                                            |
    | **Mitmuse nimetav (osad väljagrupi nimi)**         | Sisestage valuuta ribosoomi mitmuses.                                                                                                                                                              |
    | **(Lühend väljagrupp) ühikute kiirnimi**       | Sisestage tuvastamiseks valuuta ISO kood. Näiteks littide tuvastamiseks sisestage LTL.                                                                                                                             |
    | **Otsetee nimi osad (lühend väljagrupp)**      | Sisestage valuuta allüksuse nimetus. Näiteks sisestage Centas.                                                                                                                                         |
    | **Conjunction 'and' between units and parts**             | Saate printida sidesõna "ja" rahaühikute ja üksuse osade vahel. Näiteks arvete ja aruannete, LTL 100.20 summa kuvatakse 100 litti ja 20 Centas.                      |

5.  Click **Save**.



