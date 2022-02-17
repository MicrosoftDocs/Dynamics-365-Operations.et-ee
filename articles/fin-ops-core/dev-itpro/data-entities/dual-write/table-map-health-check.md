---
title: Tabelikaardi tervisekontrolli veakoodid
description: Selles teemas kirjeldatakse tabelikaardi tervisekontrolli veakoode.
author: nhelgren
ms.date: 10/04/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: nhelgren
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 916f3cfca3bae7a073ce4e956a12080ee01c8d31
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061274"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Tabelikaardi tervisekontrolli veakoodid

[!include [banner](../../includes/banner.md)]



Selles teemas kirjeldatakse tabelikaardi tervisekontrolli veakoode.

## <a name="error-100"></a>Tõrge 100

Veateade on: "Minimaalne nõutav finance and Operations platvormi versioon on PU 43, et käivitada finants- ja operatsioonide soovitused."

Funktsioon nõuab finance and Operationsi rakenduste versiooni 10.0.19 või uuema versiooni platvormivärskendusi.

## <a name="error-400"></a>Tõrge 400

Tõrketeade on järgmine: "Olemi \{Finance and Operations UniqueEntityName\} jaoks ei leitud ärisündmuste registreerimisandmeid, mis tähendab, et kaart ei tööta või kogu väljavastendus on ühesuunaline."

## <a name="error-500"></a>Tõrge 500

Veateade on järgmine: "Projekti \{projekti nimi\} jaoks ei leitud projekti konfiguratsioone. See võib olla kas projekt pole lubatud või kõik väljavastendused on ühesuunalised klientide kaasamisest finance and Operationsi.

Kontrollige tabelikaardi kaardistusi. Kui need on ühesuunalised kliendi kaasamise rakendustest Finance and Operationsi rakendustesse, ei looda otsesünkroonimiseks liiklust Finance and Operationsi rakendustest rakendusse Dataverse.

## <a name="error-900"></a>Tõrge 900

Tõrketeade on "Olemi \{Finance and Operations UniqueEntityName\} kehtetu lähtefiltri \{allikasFilterivorming\}".

Finance and Operationsi rakenduste tabelikaardil määratud lähtefilter pole süntaktiliselt õige. Filtrikriteeriumide kinnitamiseks vt teemat [Reaalajas sünkroniseerimisprobleemide tõrkeotsing](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Tõrge 1000

Tõrketeade on järgmine: "Olemi \{finance and Operations UniqueEntityName\} päring, mida kasutatakse topeltkirjutamisalus sünkroonimiseks, on \{Finance and Operations EntityFilterQueryString \}. Päringukriteeriumidele vastavad kirjed valitakse reaalajas sünkroonimiseks."

Tagastatud olemipäring on olemi SQL-i tugipäring. Kontrollige, kas päringus on sisemisi liite või filtreid, mis määravad reaalajas sünkroonimiseks kogutavad ettevõtteandmed. Sisemised ühendused ja filtrid on kohustuslikud tingimused, mis peavad olema täidetud iga kirje puhul, mis võetakse kahekordse kirjutamise reaalajas sünkroonimiseks.

## <a name="error-1300"></a>Tõrge 1300

Tõrketeade on järgmine: "Olemi \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} virtuaalseid välju \{s.EntityFieldName\} ei pruugita topeltkirjutamise jaoks jälgida."

Finance and Operationsi tabelite virtuaalsed väljad pole jälgimiseks lubatud. Reaalajas sünkroonimine võib andmeid sünkroonida, kuid see ei saa veergudes tehtud muudatusi vastu võtta.

## <a name="error-1500"></a>Tõrge 1500

Veateade on järgmine: "Andmeallika \{datasource.DataSourceName\} jälgimise võimaldamiseks peab olema vähemalt üks väli vastendatud mitteotsinguväljaga kliendi kaasamise kohta."

Olemi andmeallikal ei ole ühtegi välja, mis on vastendatud kahekordseks kirjutamiseks. Kahekordse kirjutamise korral aluseks oleva tabeli muudatusi ei jälgita.

## <a name="error-1600"></a>Tõrge 1600

Veateade on:"Andmeallikas: \{andmeallikas. DataSourceName\} for entity \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} on vahemik. Väljaminevaks kaasatakse ainult vahemikutingimusele vastavad kirjed."

Finance and Operationsi rakenduste olemitel võivad olla andmeallikad, kus filtrivahemikud on lubatud. Need vahemikud määravad kirjed, mis võetakse reaalajas sünkroonimise osana. Kui mõned kirjed jäetakse finance and Operationsi rakendustest Dataverse rakendustest välja, kontrollige, kas kirjed vastavad olemi vahemiku kriteeriumidele. Lihtne viis selle kontrolli tegemiseks on käivitada SQL-päring, mis sarnaneb järgmise näitega.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Tõrge 1700

Veateade on järgmine, "Olemi \{datasourceTable.Key.entityName\} is tracked for entity \{origTableToEntityMaps.EntityName\} tabel \{datasourceTable.Key.subscribedTableName\}. Samade tabelite, mida jälgitakse mitme olemi puhul, võib mõjutada süsteemi jõudlust reaalajas sünkroonimiskannetel."

Kui sama tabelit jälgib mitu olemit, käivitavad kõik tabeli muudatused lingitud olemite kahekordse kirjutamise hindamise. Kuigi filtriklauslid saadavad ainult kehtivad kirjed, võib hindamine põhjustada toimivusprobleeme, kui on kaua kestnud päringuid või optimeerimata päringuplaanid. See probleem ei pruugi olla ärilisest vaatenurgast välditav. Kui aga mitme üksuse vahel on palju ristuvaid tabeleid, peaksite kaaluma olemi lihtsustamist või olemi päringute optimeerimisvõimaluste kontrollimist.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
