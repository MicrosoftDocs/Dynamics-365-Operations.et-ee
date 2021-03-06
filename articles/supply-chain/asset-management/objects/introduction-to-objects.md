---
title: Varade sissejuhatus
description: Selles teemas antakse ülevaade varadest moodulis Asset Management.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetTimeline, EntAssetObjectTableLookup, EntAssetObjectTableParent, EntAssetObjectOverview, EntAssetObjectImage, EntAssetObjectTable, EntAssetLifecycleStateLog, EntAssetObjectWorkOrderActive, EntAssetObjectAttribute
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91c4ad4a96ce94c911066604794420c335a491b1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808564"
---
# <a name="introduction-to-assets"></a>Varade sissejuhatus

[!include [banner](../../includes/banner.md)]

 

Selles teemas antakse ülevaade varadest moodulis Asset Management. *Vara* on mistahes tüüpi seade, nt masin või masina osa, mis nõuab hooldust, teenindust või remonti.

Vara uuendatakse automaatselt koos seotud teabega. Näiteks võib see seotud teave olla uute või värskendatud töökäskude kohta. Saate luua varasid, kasutades kas menüükäske **Kõik varad** või **Ootel varad**. Selles teemas selgitatakse, kuidas luua varasid menüükäsu **Kõik varad** abil. Lisateavet varade loomise kohta menüükäsuga **Ootel varad** lugege teemat [Varade loomine ostutellimuste alusel](../objects/create-objects-based-on-purchase-orders.md).

## <a name="all-assets"></a>Kõik varad

Valige **Varahaldus**\>**Ühised**\>**Varad**\>**Kõik varad**. Lehel **Kõik varad** kuvatakse kõik varad ja osa nendega seotud teabest. Ainult aktiivsete varade vaatamiseks valige **Aktiivsed varad.** Ainult hooldustöötajana seotud töö asukohtadesse installitud varade vaatamiseks valige **Minu aktiivsed varad.** (See seos on seadistatud lehel **Töötajad**. Lisateavet lugege teemast [Hooldustöötajad ja töötajate grupid](../setup-for-objects/workers-and-worker-groups.md).)

Valige tabelivaates **Kõik varad** link veerus **Vara** veerus, et vaadata valitud kirje üksikasju. Kirje redigeerimiseks valige nupp **Redigeeri.** Üksikasjavaade näitab üksikasjalikku teavet, mis on seotud varaga. Paremal olev paan **Seotud teave** sisaldab täiendavat varaga seotud teavet. Laiendage paani, et kuvada seotud teavet valitud vara kohta.

Tegumiriba nupud on korraldatud vahekaartidel. Järgmises tabelis kirjeldatakse lühidalt mooduli Asse Management nuppe.

| Nupu nimi          | Kirjeldus                                                                                                                                                       |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Redigeeri                 | Saate redigeerida valitud vara.                                                                                                                                         |
| Uus                  | Saate luua uue vara.                                                                                                                                                |
| Kustuta               | Saate valitud vara kustutada.                                                                                                                                       |
| Teisalda vara           | Saate teisaldada varad kas muusse vara struktuuri või muusse asukohta samas varastruktuuris.                                                                                         |
| Asenda vara        | Saate vara hierarhias ühe alamvara teisega asendada.                                                                                                  |
| Installi vara        | Saate vara töö asukohta installida.                                                                                                                          |
| Kopeeri vara           | Saate vara hierarhia kopeerida teise teise varasse.                                                                                                                          |
| Nõuded             | Avage loendi **Aktiivsed varad** leht, kus saate vaadata valitud vara jaoks loodud hooldustaotlusi.                                                                         |
| Sündmuse ajalugu        | Saate vaadata vara kohta tehtud erinevate registreerimiste ülevaadet.                                                                                                         |
| Vara kooslus            | Saate vaadata kõigi varas kasutatavate kaupade (varuosade ja muude kaupade) loendit.                                                                                  |
| Töökäsud          | Saate avada loendi **Aktiivsed töökäsud** lehe, kus saate vaadata vara töökäske.                                                                                        |
| Kontroll-loend            | Saate vaadatavarale registreeritud hoolduse kontrollnimekirja ja mõõtmiste ülevaadet.                                                                                                 |
| Hoolduskatkestus | Saate luua või vaadata vara hoolduskatkestusi.                                                                                                       |
| Projekti kanded | Saate vaadata kõiki vara jaoks loodud töökäskudega seotud sisestatud kandeid.                                                                                       |
| Vara mõõtmised       | Saate luua või vaadata vara varamõõdikuid.                                                                                                               |
| Hooldusgraafik | Avage loendi **Avatud hooldusgraafik** leht, kus saate vaadata varaga seotud hoolduskavu, hooldustaotlusi ja hoolduskordi ja mille olek on **Loodud.** |
| Vara oleku värskendamine   | Saate uuendada vara töötsükli olekut. Saate valida mitu vara loendi **Kõik varad** lehel ja seejärel uuendada varade töötsükli olekut kõigi nende jaoks korraga.              |
| Töötsükli oleku logi  | Saate vaadata Logi, mis näitab valitud vara töötsükli etappe.                                                                                                                 |
| Vara dokumendid      | Saate vaadata varale manustatud dokumentide loendit. Need dokumendid seadistatakse asukohas **Varahaldus** \> **Seadistus** \> **Vara dokumendid**.                 |
| Atribuudid           | Saate luua või vaadata vara atribuute.                                                                                                                             |
| Pilt                | Saate valida vara jaoks pildi.                                                                                                                                   |
| Emaettevõtte varad        | Saate vaadata valitud vara ülataseme vara ajalugu.                                                                                                                |
| Töö asukohad | Saate vaadata valitud vara töö asukoha ajalugu.                                                                                                          |
| Seisundi hindamine | Saate registreerida vara seisundi hindamise mõõdikud.                                                                                                         |
| Vead               | Avage loendi **Vara rikked** lehte, kus saate vaadata varale registreeritud rikkeid.                                                                                             |
| Kulude jälitamine         | Saate võrrelda vara eelarvekulusid ja tegelikke kulusid.                                                                                                              |
| Tunnijuhtimine         | Saate võrrelda vara eelarvetunde ja tegelikke tunde.                                                                                                              |
| Vara KPI-d           | Saate arvutada ja vaadata vara võtmejõudlusnäidikuid (KPI-sid).                                                                                              |
| Töötüübid            | Saate vaadata vara praeguste töö vaiketüüpide ülevaadet.                                                                                                            |
| Kriitilisuse tüübid    | Saate vaadata või uuendada kriitilisuse tüüpe.                                                                                                                              |
| Varuosad          | Saate vaadata kinnitatud ja alternatiivsete varuosade loendit, mida saab varal kasutada.                                                                               |
| Vara tarbimine    | Saate printida aruande, milles kuvatakse vara tarbimise registreerimisi.                                                                                                |
| Vara tõrge          | Saate printida aruande, milles kuvatakse vara tõrgete registreerimisi.                                                                                                      |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]