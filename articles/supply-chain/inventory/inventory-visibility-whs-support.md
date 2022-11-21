---
title: Inventory Visibility WMS-i kaupade tugi
description: Selles artiklis kirjeldatakse laovarude nähtavuse tuge kaupadel, mis on lubatud laohaldusprotsessidele (WMS-kaubad).
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: bed402ecf20c19e81b2687efd90dba600460971a
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762735"
---
# <a name="inventory-visibility-support-for-wms-items"></a>Inventory Visibility WMS-i kaupade tugi

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab varude nähtavuse tuge kaupadel, mis on lubatud laohaldusprotsessidele (WMS). Funktsiooni, mis lisab selle võimaluse varude nähtavuse jaoks, nimetatakse Advanced *WMS-iks*.

## <a name="wms-items"></a>WMS-kaubad

WMS-kaup on kaup, mis on lubatud WMS-i jaoks ja töödeldakse laos, mis on ka WMS-i lubatud.

Lisateavet WMS-i ja laohalduse **mooduli kohta** Microsoftis Dynamics 365 Supply Chain Management vt laohalduse [ülevaadet](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Funktsiooni ulatus

Laovarude nähtavuse täpsema WMS-i funktsioon keskendub vaba kaubavaru koguse arvutustele, mis põhinevad laoseisu päringutel. See funktsioon ei luba teil varude nähtavust kasutada lao töötlemise üldtegevuste haldamiseks. Varude nähtavus ei näita laopõhiseid mõisteid selle kasutajatele. Siin on mõned näited neist mõistetest:

- Reserveerimishierarhia
- Kas kaup või ladu on WMS-i lubatud?
- Ühiku seeriagrupi ID
- Laopõhised protsessid, nt saadetised, koormad, lained ja töö

Lao nähtavus põhineb sellel teabel, mis põhineb tarneahela haldusest saadetud andmetel. WMS-põhised andmed (teisisõnu tabeli `WHSInventReserve` andmed) ei ole kasutajatele nähtavad.

Kui kasutate laovarude nähtavuse jaoks täpsema WMS-funktsiooni, on kõik päringutulemused identsed otse tarneahela halduses tehtud päringute tulemustega. Kuid need ei ole identsed päringute tulemustega, mis on tehtud laohalduse mobiilirakenduse abil, sest mobiilirakendus kasutab veidi erinevat arvutusloogikat.

## <a name="when-to-use-the-feature"></a>Funktsiooni kasutamise millal

Soovitame kasutada WMS-i funktsiooni lao nähtavuse jaoks stsenaariumite puhul, kus on täidetud kõik järgmised tingimused:

- Sünkroonite tarneahela haldusandmeid varude nähtavusega.
- Te kasutate WMS-i tarneahela halduses.
- Kasutajad reserveerivad WMS-i kaupu laotasemest madalamatel tasemetel (nt litsentsiplaadi tasemel, sest töötlete laotööd).

Teistes stsenaariumides on vabad päringutulemused samad, sõltumata sellest, kas lao nähtavuse täpsema WMS-i funktsioon on lubatud. Lisaks on parem jõudlus, kui te ei luba nende stsenaariumite funktsiooni, kuna arvutusi ja üldkulusid on vähem.

## <a name="enable-the-wms-feature-for-inventory-visibility"></a>Luba WMS-i funktsioon varude nähtavuse jaoks

WMS-i funktsiooni lubamiseks varude nähtavuse jaoks järgige neid samme.

1. Logige administraatorina tarneahela haldusse sisse.
1. Avage funktsioonihalduse [tööruum](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja lubage selles järjekorras järgmised funktsioonid:

    1. *Inventory Visibility integreerimine*
    1. *Laokauba lubamine varude nähtavuses*

1. Avage **Varude haldus \> Seadistus \> Varude nähtavuse integratsiooni parameetrid**.
1. Seadke vahekaardil **Luba WMS-kaubad** suvand **Luba WMS-kaubad väärtusele** *Jah*.
1. Logige keskkonda Power Apps sisse ja avage **Varude nähtavus**.
1. **Avage konfiguratsioonileht** ja lülitage vahekaardil **Funktsioonihaldus** sisse *funktsioon AdvancedWHS*.
1. Tarneahela halduses minge varude halduse perioodiliste **ülesannete \> varude nähtavuse \> integratsioonile**.
1. Tegevuspaanil valige Suvand **Keela,** et ajutiselt keelata varude nähtavus.
1. Tegevuspaanil valige luba **varude** nähtavuse uuesti lubamiseks. Lisandmoodul laaditakse uuesti ja uus funktsioon on nüüd lubatud. Teie WMS-ga seotud andmed käivitatakse sünkroonimise varude nähtavusega.

## <a name="query-on-hand-quantities-of-wms-items"></a>WmS-kaupade vaba koguse päring

WMS-kaupade päringu esitamiseks kasutage [sama rakenduse programmeerimisliidest (API)](inventory-visibility-api.md) ja sõnumi süntaksit, mida kasutate mitte-WMS-kaupade jaoks. Te ei pea määrama, kas kaup on WMS-kaup või mitte-WMS-kaup. Lao nähtavus eristab automaatselt kaupu, mis põhinevad talletatud andmetel.

WMS-kaupade päringute tulemused on põhiliselt samad, mis mitte-WMS-kaupade tulemused. Ainus erinevus on see, et andmeallika järgmised füüsilised `fno` meetmed arvutatakse WMS-loogika põhjal tarneahela halduses:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Kõik muud füüsilised meetmed arvutatakse nii, nagu need on, kui WMS-i funktsioon varude nähtavuse jaoks on keelatud.

Üksikasjalikku teavet SELLE kohta, kuidas WMS-kaupade vaba kaubavaru arvutused töötavad, vt laohalduse [valge raamatu reserveeringutest](https://www.microsoft.com/download/details.aspx?id=43284).

## <a name="on-hand-list-view-and-data-entity-for-wms-items"></a>WMS-kaupade vaba loendi kuva ja andmeüksus

Varude **nähtavuse kokkuvõtte lehe eellaadimine** annab vaate vaba kaubavaru *indeksi päringu eellaadimise tulemuste üksusele*. Erinevalt laoseisu *kokkuvõtte* üksusest annab *vaba* kaubavaru indeksi päringu eellaadimise tulemuste üksus toodetele vaba kaubavaru loendi koos valitud dimensioonidega. Lao nähtavus sünkroonib eellaaditud koondandmed iga 15 minuti järel.

Kui kasutate lao nähtavust WMS-kaupadega ja soovite WMS-kaupade vaba kaubavaru vaadata, *soovitame* teil lubada lao nähtavuse kokkuvõtte eellaadimise funktsiooni (vt ka [sujuva laoseisu päringu eellaadimist](inventory-visibility-power-platform.md#preload-streamlined-onhand-query)). Vastav andmeüksus talletab teie Dataverse päringu eellaadimise tulemuse, mida uuendatakse iga 15 minuti järel. Andmeüksuse nimi on `Onhand Index Query Preload Result`.

> [!IMPORTANT]
> Üksus Dataverse on kirjutuskaitstud. Saate vaadata ja eksportida varude nähtavuse üksuste andmeid, kuid **ärge muutke seda**.

WMS-i kaubakoguste muutused, mis on talletatud tarneahela halduse andmeallikas (`fno`), on keelatud. Selline käitumine vastab teiste laovarude nähtavuse funktsioonide käitumisele. See piirang jõustatakse konfliktide vältimiseks.

## <a name="wms-item-compatibility-for-other-functions-in-inventory-visibility"></a>WMS-i kauba ühilduvus teiste varude nähtavuse funktsioonide jaoks

[WMS-kaupade](inventory-visibility-reservations.md)[(WMS-kaupade)](inventory-visibility-allocation.md) kergeid reserveeringuid ja varude eraldamist toetatakse. WmS-iga seotud füüsilised andmed saate lisada ka tarkvara reserveerimise ja eraldamise arvutustesse.

## <a name="calculate-available-to-promise-quantities"></a>Arvuta lubaduse jaoks saadaolevad kogused

Lahendus toetab täielikult WMS-kaupade [jaoks lubaduse (ATP)](inventory-visibility-available-to-promise.md) lubamist. ATP arvutusi saab määratleda WMS-spetsiifilisi üksikasju mõjutamata.
