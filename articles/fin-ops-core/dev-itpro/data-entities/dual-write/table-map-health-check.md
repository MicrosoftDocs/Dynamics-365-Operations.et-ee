---
title: Tabelikaardi tervisekontrolli veakoodid
description: See artikkel kirjeldab tõrkekoode tabelikaardi seisundikontrolli jaoks.
author: RamaKrishnamoorthy
ms.date: 05/31/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 16c79a788b66830b77b2cdfb33fd2416c530f7d2
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111562"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Tabelikaardi tervisekontrolli veakoodid

[!include [banner](../../includes/banner.md)]



See artikkel kirjeldab tõrkekoode tabelikaardi seisundikontrolli jaoks.

## <a name="error-100"></a>Tõrge 100

Tõrketeade on järgmine: "Minimaalne nõutav finantside ja toimingute platvormi versioon on PU 43, et käivitada finantside ja toimingute soovitused."

See funktsioon nõuab platvormi uuendusi versioonile 10.0.19 või uuemale versioonile finantside ja toimingute rakendustest.

## <a name="error-400"></a>Tõrge 400

Tõrketeade on järgmine: " \{Üksuse finantside ja toimingute UniqueEntityName\} jaoks ei leitud ärisündmuste registreerimisandmeid, mis tähendab, et vastendus ei tööta või on kogu välja vastendamine ühesuunaline."

## <a name="error-500"></a>Tõrge 500

Veateade on järgmine: "Projekti \{projekti nimi\} jaoks ei leitud projekti konfiguratsioone. See võib olla kas projekt pole lubatud või on kõik väljavastendused ühesuunalised kliendi kaasamisest finantside ja toiminguteni."

Kontrollige tabelikaardi kaardistusi. Kui need on kliendikogemuse rakendustest finantside ja toimingute rakendustesse ühesuunalisena, siis ei looda ühtegi liiklust finantside ja toimingute rakenduste otsesünkroonimiseks Dataverse.

## <a name="error-900"></a>Tõrge 900

Tõrketeade on järgmine: "Üksuse finantside \{ja toimingute\}\{UniqueEntityName kehtetu allikafiltri lähtefiltri vorming\}."

Finantside ja toimingute rakenduste tabelikaardil määratud allikafilter ei ole süntaktiliselt õige. Filtrikriteeriumide kinnitamiseks vt teemat [Reaalajas sünkroniseerimisprobleemide tõrkeotsing](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Tõrge 1000

Tõrketeade on järgmine: päring Entity \{Finance and Operations UniqueEntityName\}, mida kasutatakse topeltkirjutuse otsesünkroonimiseks \{, on finantsid ja toimingud EntityFilterQueryString \}. Päringukriteeriumidele vastavad kirjed valitakse reaalajas sünkroonimiseks."

Tagastatud olemipäring on olemi SQL-i tugipäring. Kontrollige, kas päringus on sisemisi liite või filtreid, mis määravad reaalajas sünkroonimiseks kogutavad ettevõtteandmed. Sisemised ühendused ja filtrid on kohustuslikud tingimused, mis peavad olema täidetud iga kirje puhul, mis võetakse kahekordse kirjutamise reaalajas sünkroonimiseks.

## <a name="error-1300"></a>Tõrge 1300

Tõrketeade on järgmine: " \{Virtuaalsed väljad s.EntityFieldName\} üksuse \{finantside ja toimingute EntityMetadata.EntityProperties.LogicalEntityName\} puhul ei pruugita topeltkirjutust jälitada."

Finantside ja toimingute tabelite virtuaalväljad ei ole jälgimise jaoks lubatud. Reaalajas sünkroonimine võib andmeid sünkroonida, kuid see ei saa veergudes tehtud muudatusi vastu võtta.

## <a name="error-1500"></a>Tõrge 1500

Veateade on järgmine: "Andmeallika \{datasource.DataSourceName\} jälgimise võimaldamiseks peab olema vähemalt üks väli vastendatud mitteotsinguväljaga kliendi kaasamise kohta."

Olemi andmeallikal ei ole ühtegi välja, mis on vastendatud kahekordseks kirjutamiseks. Kahekordse kirjutamise korral aluseks oleva tabeli muudatusi ei jälgita.

## <a name="error-1600"></a>Tõrge 1600

Tõrketeade on järgmine: andmeallikas \{. Üksuse finantside\} ja toimingute \{ÜksusMetadata.EntityProperties.LogicalEntityName\} vahemik on. Väljaminevaks kaasatakse ainult vahemikutingimusele vastavad kirjed."

Finantside ja toimingute rakenduste üksustel võivad olla andmeallikad, kus filtrivahemikud on lubatud. Need vahemikud määravad kirjed, mis võetakse reaalajas sünkroonimise osana. Kui mõned kirjed jäetakse finantside ja toimingute rakendustest vahele, kontrollige Dataverse, kas kirjed vastavad üksuse vahemiku kriteeriumitele. Lihtne viis selle kontrolli tegemiseks on käivitada SQL-päring, mis sarnaneb järgmise näitega.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Tõrge 1700

Veateade on järgmine, "Olemi \{datasourceTable.Key.entityName\} is tracked for entity \{origTableToEntityMaps.EntityName\} tabel \{datasourceTable.Key.subscribedTableName\}. Samade tabelite, mida jälgitakse mitme olemi puhul, võib mõjutada süsteemi jõudlust reaalajas sünkroonimiskannetel."

Kui sama tabelit jälgib mitu olemit, käivitavad kõik tabeli muudatused lingitud olemite kahekordse kirjutamise hindamise. Kuigi filtriklauslid saadavad ainult kehtivad kirjed, võib hindamine põhjustada toimivusprobleeme, kui on kaua kestnud päringuid või optimeerimata päringuplaanid. See probleem ei pruugi olla ärilisest vaatenurgast välditav. Kui aga mitme üksuse vahel on palju ristuvaid tabeleid, peaksite kaaluma olemi lihtsustamist või olemi päringute optimeerimisvõimaluste kontrollimist.

## <a name="error-1800"></a>Tõrge 1800
Tõrketeade on järgmine: "Datasource: {} üksuseLe CustCustomerV3Entity sisaldab vahemiku väärtust. Sissetulevate kirjete ajased alates finantsideni Dataverse ja toiminguid võivad mõjutada üksuse vahemiku väärtused. Sätete kinnitamiseks testige kirjete Dataverse värskendusi finantsidesse ja toimingutesse kirjetega, mis ei vasta filtri kriteeriumidele.

Kui finantside ja toimingute rakenduste üksuses on määratud vahemik, tuleb sissetulevat sünkroonimist finantsidelt ja toimingute rakendustele testida nende kirjete uuendamise suhtes, Dataverse mis ei vasta sellele vahemiku kriteeriumile. Kõiki kirjeid, mis ei ühti vahemikuga, koheldakse üksus sisestamistoiminguna. Kui aluseks olevas tabelis on kirje, siis sisestamine nurjub. Soovitame teil testida seda kasutusjuhtumeid kõigi stsenaariumite puhul enne tootmisele juurutamist.

## <a name="error-1900"></a>Tõrge 1900
Tõrketeade on järgmine: üksus: andmeallikaid {} ei jälgita väljamineva topeltkirjutuse suhtes. See võib mõjutada reaalajas sünkroonimispäringu jõudlust. Palunmodellge üksus finantsis ja toimingutes kasutamata andmeallikate ja tabelite eemaldamiseks või juurutage getEntityRecordIdsImpactedByTableChange käitusaja päringute optimeerimiseks."

Kui on palju andmeallikaid, mida ei kasutata tegeliku reaalajas sünkroonimise jälgimiseks finantside ja toimingute rakendustest, siis on võimalus, et üksuse jõudlus võib mõjutada reaalajas sünkroonimist. Jälgitud tabelite optimeerimiseks kasutage meetodit getEntityRecordIdsImpactedByTableChange.

## <a name="error-5000"></a>Tõrge 5000
Tõrketeade on järgmine: "Sünkroonne sünkroonne sünkroonne on registreeritud üksusekontode andmehalduse sündmuste jaoks. Need võivad mõjutada algset sünkroonimist ja reaalajas sünkroonimise jõudlust Dataverse. Parima jõudluse jaoks muutke aaaa asünkroonseks töötluseks. Registreeritud registreerimata {} kauba loend."

Üksuse sünkroonne sisu võib Dataverse mõjutada reaalajas sünkroonimist ja sünkroonimisjõudluseid, kuna see lisab kande koormale. Soovitatav lähenemine on lülitada välja üksus või teha need asyncid välja, kui koormuse aeg on algses sünkroonimises aeglane või kui teatud üksuse sünkroonimine on reaalajas.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

