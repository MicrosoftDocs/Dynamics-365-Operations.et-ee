---
title: Hooldusnõuded
description: See artikkel annab ülevaate varahalduse hooldustaotluste haldamisest.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 488b6505aba246aa3a6ea69436514a274403bf49
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015634"
---
# <a name="maintenance-requests"></a>Puudumistaotluste loomine

[!include [banner](../../includes/banner.md)]

Hooldustaotlused on märkmed või avaldused, mis on loodud teavitama haldurit või plaanijat, et vara võib vajada hooldust või parandustööd, kuid ilma töötellimust loomata. Kui hooldustaotluse sisu loetakse kehtivaks, saab töötellimuse seejärel hooldustaotluse põhjal luua.

Hooldustaotlusi saab luua iga vara kohta varahalduses. Sõltuvalt sellest, kuidas teie ettevõte kasutab hooldustaotlusi, saab luua erinevat tüüpi hooldustaotlusi. Järgmisena on toodud mõned näited.

- Puudumistaotluste loomine
- Märkmed
- Parandused või täiustused
- Investeeringud
- Allika parandamine (seda tüüpi kasutatakse, kui saate varasid mõnest muust asukohast, et saaksite hooldust või parandustööd teha ja seejärel pärast töö lõpule viimist töö tagastada.)

## <a name="view-maintenance-requests"></a>Hooldusnõuete vaatamine

Hooldustaotluste vaatamiseks valige Varahalduse **hooldustaotlused** \> **·** \> **Kõik hooldustaotlused**, aktiivse **hoolduse taotlused või** minu funktsiooni **asukoha hooldustaotlused.** Iga loendileht kuvab osa hooldustaotlusega seotud teabest.

![Hooldusnõuete vaatamine.](media/01-manage-maintenance-requests.png)

> [!NOTE]
> Kasutage loendilehte **Minu funktsionaalse asukoha hooldustaotlused**, et vaadata hooldustaotluste loendit, mis sisaldab kas funktsionaalseid asukohti, millega olete töötajana seotud või varasid, mis on installitud funktsionaalsetele asukohtadele, millega olete töötajana seotud. (Lisateavet hooldustöötajate funktsionaalsete asukohtade häälestamise kohta vt teemast [Hooldustöötajad ja töörühmad](../setup-for-objects/workers-and-worker-groups.md).)
> 
> Kuigi kliendikonto teave on saadaval vara teenuse halduses (väline hooldus), see ei ole saadaval varahalduses (sisemine hooldus).

Kirje üksikasjade vaate avamiseks loendilehel **Kõik hooldustaotlused** ruudustiku vaates, valige link veerus **Hooldustaotlused**.

![Kuva hooldusnõude üksikasjad.](media/02-manage-maintenance-requests.png)

Tegumiriba nupud on korraldatud vahekaartidel. Järgmises tabelis kirjeldatakse lühidalt mooduli Asse Management nuppe.

| Nupu nimi                      | Kirjeldus |
|----------------------------------|-------------|
| Redigeerimine                             | Saate redigeerida valitud hankija nõude kaupa. |
| Uus                              | Loob uue hankija nõude |
| Kustutamine                           | Kustuta valitud kategooria taotlus |
| Töötellimuse kaust                  | Ühenda valitud hooldustaotlus töökäsu kaustaga. |
| Töötellimus                       | Loo töötellimus valitud hooldustaotluse põhjal. |
| Vara tõrge                      | Klõpsake **Vara tõrked**, kus saate luua valitud hooldustaotlusele tõrke registreerimise. |
| Töötellimused                      | Saate kuvada kõigi valitud hooldustaotlusega seotud töötellimuste loendi. |
| Valige Uuenda hoolduse taotluse olekut. | Valige Uuenda hoolduse taotluse olekut. |
| Elutsükli oleku logi              | Vaadake logi, mis näitab valitud hooldustaotluse olelustsüklit. |
| Hooldustaotluse tüübid      | Saate printida aruande, kus kuvatakse valitud hooldustaotluse üksikasjad. |
| Saada laenuvara                  | Saate valida laenuvara, mis peaks olema valitud hooldustaotluses valitud vara ajutiseks asenduseks. |
| Tagastuslaenu vara                | Registreeri laenuvarad tagastatud |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]