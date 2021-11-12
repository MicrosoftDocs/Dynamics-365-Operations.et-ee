---
title: Tabelikaardi tervisekontrolli veakoodid
description: Selles teemas kirjeldatakse tabelikaardi tervisekontrolli veakoode.
author: nhelgren
ms.date: 10/04/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: nhelgren
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 4f0b92a6bc6c051a6bb24b49d3280ca5ecea3625
ms.sourcegitcommit: c4500b626667185643b3a2e7fc3a004d42198d07
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/29/2021
ms.locfileid: "7725071"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Tabelikaardi tervisekontrolli veakoodid

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas kirjeldatakse tabelikaardi tervisekontrolli veakoode.

## <a name="error-100"></a>Tõrge 100

Veateade: "Finance and Operations soovituste käitamiseks on minimaalne nõutav Finance and Operationsi rakenduste platvormi versioon PU 43".

Funktsioon nõuab platvormivärskendusi Finance and Operationsi rakenduste versioonile 10.0.19 või uuemale.

## <a name="error-400"></a>Tõrge 400

Veateade on järgmine: "Olemi \{Finance and Operations UniqueEntityName\} jaoks ei leitud ärisündmuste registreerimisandmeid, mis tähendab, et kaart ei tööta või kogu väljade kaardistus on ühesuunaline."

## <a name="error-500"></a>Tõrge 500

Veateade on järgmine: "Projekti \{projekti nimi\} jaoks ei leitud projekti konfiguratsioone. See võib juhtuda, et projekt pole lubatud või kõik väljade kaardid on ühesuunalised alates klientide kaasamisest kuni rakenduseni Finance and Operations."

Kontrollige tabelikaardi kaardistusi. Kui need on ühesuunalised kliendikaasamise rakendustest Finance and Operations rakendustesse, ei genereerita Finance and Operationsi rakendustest Dataverse'i reaalajas sünkroonimiseks liiklust.

## <a name="error-900"></a>Tõrge 900

Veateade on järgmine: "Vigane allikafiltri \{sourceFilter\} vorming üksuse \{Finance and Operations UniqueEntityName\} puhul."

Finance and Operationsi rakenduste tabelikaardil määratud allikafilter ei ole süntaktiliselt õige. Filtrikriteeriumide kinnitamiseks vt teemat [Reaalajas sünkroniseerimisprobleemide tõrkeotsing](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Tõrge 1000

Veateade on järgmine: "Kahekirjutava reaalajas sünkroonimise jaoks kasutatav päring \{Finance and Operations UniqueEntityName\} on \{Finance and Operations EntityFilterQueryString\}. Päringukriteeriumidele vastavad kirjed valitakse reaalajas sünkroonimiseks."

Tagastatud olemipäring on olemi SQL-i tugipäring. Kontrollige, kas päringus on sisemisi liite või filtreid, mis määravad reaalajas sünkroonimiseks kogutavad ettevõtteandmed. Sisemised ühendused ja filtrid on kohustuslikud tingimused, mis peavad olema täidetud iga kirje puhul, mis võetakse kahekordse kirjutamise reaalajas sünkroonimiseks.

## <a name="error-1300"></a>Tõrge 1300

Veateade on järgmine: "Olemi \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} virtuaalseid välju \{s.EntityFieldName\} ei pruugita kahekordse kirjutamise jaoks jälgida."

Rakenduse Finance and Operations tabelite virtuaalsed väljad pole jälgimiseks lubatud. Reaalajas sünkroonimine võib andmeid sünkroonida, kuid see ei saa veergudes tehtud muudatusi vastu võtta.

## <a name="error-1500"></a>Tõrge 1500

Veateade on järgmine: "Andmeallika \{datasource.DataSourceName\} jälgimise võimaldamiseks peab olema vähemalt üks väli vastendatud mitteotsinguväljaga kliendi kaasamise kohta."

Olemi andmeallikal ei ole ühtegi välja, mis on vastendatud kahekordseks kirjutamiseks. Kahekordse kirjutamise korral aluseks oleva tabeli muudatusi ei jälgita.

## <a name="error-1600"></a>Tõrge 1600

Veateade on järgmine: "Andmeallikas: \{datasource.DataSourceName\} olemile \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} on vahemik. Väljaminevaks kaasatakse ainult vahemikutingimusele vastavad kirjed."

Finance and Operationsi rakenduste olemitel võivad olla andmeallikad, kus filtrivahemikud on lubatud. Need vahemikud määravad kirjed, mis võetakse reaalajas sünkroonimise osana. Kui mõned kirjed jäetakse Finance and Operationsi rakendustest Dataverse'i vahele, kontrollige, kas kirjed vastavad olemi vahemiku kriteeriumidele. Lihtne viis selle kontrolli tegemiseks on käivitada SQL-päring, mis sarnaneb järgmise näitega.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Tõrge 1700

Veateade on järgmine, "Olemi \{datasourceTable.Key.entityName\} is tracked for entity \{origTableToEntityMaps.EntityName\} tabel \{datasourceTable.Key.subscribedTableName\}. Samade tabelite, mida jälgitakse mitme olemi puhul, võib mõjutada süsteemi jõudlust reaalajas sünkroonimiskannetel."

Kui sama tabelit jälgib mitu olemit, käivitavad kõik tabeli muudatused lingitud olemite kahekordse kirjutamise hindamise. Kuigi filtriklauslid saadavad ainult kehtivad kirjed, võib hindamine põhjustada toimivusprobleeme, kui on kaua kestnud päringuid või optimeerimata päringuplaanid. See probleem ei pruugi olla ärilisest vaatenurgast välditav. Kui aga mitme üksuse vahel on palju ristuvaid tabeleid, peaksite kaaluma olemi lihtsustamist või olemi päringute optimeerimisvõimaluste kontrollimist.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
