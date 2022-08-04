---
title: Inventory Visibility WMS-i kaupade tugi
description: Selles artiklis kirjeldatakse laovarude nähtavuse tuge kaupadel, mis on lubatud laohaldusprotsessidele (WMS-kaubad).
author: yufeihuang
ms.date: 03/10/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 54ce637d2d7b590988f7590eae5248276bcc4b96
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066606"
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

Soovitame kasutada varude nähtavuse jaoks täpsema WMS-i funktsiooni juhul, kui kõik järgmised tingimused on täidetud:

- Sünkroonite tarneahela haldusandmeid varude nähtavusega.
- Te kasutate WMS-i tarneahela halduses.
- Kasutajad reserveerivad WMS-i kaupu laotasemest erineval tasemel (näiteks laotöö kasutamisel).

Teistes stsenaariumides on vabad päringutulemused samad, sõltumata sellest, kas lao nähtavuse täpsema WMS-i funktsioon on lubatud. Lisaks on parem jõudlus, kui te ei luba nende stsenaariumite funktsiooni, kuna arvutusi ja üldkulusid on vähem.

## <a name="enable-the-advanced-wms-feature-for-inventory-visibility"></a>Luba täpsema WMS-i funktsioon varude nähtavuse jaoks

Varude nähtavuse täpsema WMS-funktsiooni lubamiseks järgige neid samme.

1. Logige administraatorina tarneahela haldusse sisse.
1. Avage funktsioonihalduse [tööruum](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja lubage selles järjekorras järgmised funktsioonid:

    1. *Inventory Visibility integreerimine*
    1. *Laokauba lubamine varude nähtavuses*

1. Avage **Varude haldus \> Seadistus \> Varude nähtavuse integratsiooni parameetrid**.
1. Seadke vahekaardil **Luba WMS-kaubad** suvand **Luba WMS-kaubad väärtusele** *Jah*.
1. Logige rakendusse Power Apps sisse.
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

Kõik muud füüsilised meetmed arvutatakse nii, nagu need on siis, kui Laiendatud WMS-i funktsioon varude nähtavuse jaoks on keelatud.

Üksikasjalikku teavet SELLE kohta, kuidas WMS-kaupade vaba kaubavaru arvutused töötavad, vt laohalduse [valge raamatu reserveeringutest](https://www.microsoft.com/download/details.aspx?id=43284).

Andmeüksused, mis on eksporditud, ei Dataverse saa wmS-kaupade koguseid veel värskendada. Andmeüksustes kuvatavad kogused on õiged nii MITTE-WMS-kaupade kui ka koguste puhul, mida WMS-loogika ei mõjuta (st kogused, `AvailPhysical` v.a kogused, `AvailOrdered` ja `ReservPhysical``ReservOrdered``fno` andmeallikas).

WMS-i kaubakoguste muutused, mis on talletatud tarneahela halduse andmeallikas, on keelatud. Nagu ka teiste varude nähtavuse funktsioonide puhul, jõustatakse see piirang konfliktide vältimiseks.

## <a name="soft-reservations-on-wms-items-in-inventory-visibility"></a>WMS-kaupade kerged reserveeringud varude nähtavuses

Üldiselt toetatakse WMS-kaupade [kergeid](inventory-visibility-reservations.md) reserveeringuid. WmS-ga seotud füüsilised andmed saate lisada ka tarkvara reserveerimise arvutamistes. 

Teatud piiranguna ei toetata *praegu* WMS-kaupade puhul reserveerimise arvutamiseks saadaolevat kogust. Seega, kui esineb reserveeringuid praeguste dimensioonide kohal, kus toimub kerge reserveerimine, *on saadatav reserveerimise arvutamine* vale. Kergeid reserveeringuid ei mõjutata, kui **valik ifCheckAvailForReserv** on kerge reserveerimise [API-s keelatud](inventory-visibility-api.md#create-one-reservation-event).

See piirang kehtib ka funktsioonidele ja kohandustele, mis põhinevad kergetel reserveerimistel (nt eraldus).

## <a name="calculate-available-to-promise-quantities"></a>Arvuta lubaduse jaoks saadaolevad kogused

Lahendus toetab täielikult WMS-kaupade [jaoks lubaduse (ATP)](inventory-visibility-available-to-promise.md) lubamist. ATP arvutusi saab määratleda WMS-spetsiifilisi üksikasju mõjutamata.
