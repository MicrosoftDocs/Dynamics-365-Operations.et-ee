---
title: Inventory Visibility WHS-i kaupade tugi
description: Selles teemas kirjeldatakse laovarude nähtavuse tuge kaupadel, mis on lubatud täpsemate laoprotsesside jaoks (laohaldusüksused).
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
ms.openlocfilehash: cfbff05697f4159cb74d110887b8029f28fbf96b
ms.sourcegitcommit: 1050e58e621d9a0454895ed07c286936f8c03320
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2022
ms.locfileid: "8625425"
---
# <a name="inventory-visibility-support-for-whs-items"></a>Inventory Visibility WHS-i kaupade tugi

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse laovarude nähtavuse tuge kaupadel, mis on lubatud täpsemate laoprotsesside jaoks (laohaldusüksused). Funktsiooni, mis lisab selle võimaluse varude nähtavuse jaoks, nimetatakse täpsemaks *laotööleheks*.

## <a name="whs-items"></a>Laoala elemendid

Laohaldus on kaup, mis on lubatud täpsemaks laoprotsessiks ja mida töödeldakse laos, kus laohaldus on samuti lubatud.

Lisateavet laohalduse ja laohalduse mooduli **kohta Microsoftis** vt laohalduse Dynamics 365 Supply Chain Management ülevaatest [...](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Funktsiooni ulatus

Laovarude nähtavuse täpsema laovaru funktsioon keskendub vaba kaubavaru päringutel põhinevatele vaba kaubavaru koguse arvutustele. See funktsioon ei luba teil varude nähtavust kasutada lao töötlemise üldtegevuste haldamiseks. Varude nähtavus ei näita laopõhiseid mõisteid selle kasutajatele. Siin on mõned näited neist mõistetest:

- Reserveerimishierarhia
- Kas kaup või ladu on laohaldust lubanud?
- Ühiku seeriagrupi ID
- Laopõhised protsessid, nt saadetised, koormad, lained ja töö

Lao nähtavus põhineb sellel teabel, mis põhineb tarneahela haldusest saadetud andmetel. Laoala põhised andmed (teisisõnu tabeli andmed `WHSInventReserve`) ei ole kasutajatele nähtavad.

Kui kasutate laovarude nähtavuse jaoks täpsema laohaldusfunktsiooni, on kõik päringutulemused identsed otse tarneahela halduses tehtud päringute tulemustega. Kuid need ei ole identsed päringute tulemustega, mis on tehtud laohalduse mobiilirakenduse abil, sest mobiilirakendus kasutab veidi erinevat arvutusloogikat.

## <a name="when-to-use-the-feature"></a>Funktsiooni kasutamise millal

Varude nähtavuse jaoks on soovitatav kasutada täpsema laotöölehe funktsiooni, kui kõik järgmised tingimused on täidetud:

- Sünkroonite tarneahela haldusandmeid varude nähtavusega.
- Te kasutate whS-i tarneahela halduses.
- Kasutajad reserveerivad laohaldust kasutavad kaubad laotasemest erineval tasemel (näiteks laotöö kasutamisel).

Teistes stsenaariumides on vaba kaubavaru päringu tulemused samad, olenemata sellest, kas lao nähtavuse täpsema laohalduse funktsioon on lubatud. Lisaks on parem jõudlus, kui te ei luba nende stsenaariumite funktsiooni, kuna arvutusi ja üldkulusid on vähem.

## <a name="enable-the-advanced-whs-feature-for-inventory-visibility"></a>Täpsema laotöölehe funktsiooni lubamine varude nähtavuse jaoks

Laovarude nähtavuse täpsema laotöölehe funktsiooni lubamiseks järgige neid samme.

1. Logige administraatorina tarneahela haldusse sisse.
1. Avage funktsioonihalduse [tööruum](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja lubage selles järjekorras järgmised funktsioonid:

    1. *Inventory Visibility integreerimine*
    1. *Laokauba lubamine varude nähtavuses*

1. Avage **Varude haldus \> Seadistus \> Varude nähtavuse integratsiooni parameetrid**.
1. Seadke vahekaardil **Lao whS-kaubad** suvandi Luba **laoala kaubad väärtusele** *Jah*.
1. Logige rakendusse Power Apps sisse.
1. **Avage konfiguratsioonileht** ja lülitage vahekaardil **Funktsioonihaldus** sisse *funktsioon AdvancedWHS*.
1. Tarneahela halduses minge varude halduse perioodiliste **ülesannete \> varude nähtavuse \> integratsioonile**.
1. Tegevuspaanil valige Suvand **Keela,** et ajutiselt keelata varude nähtavus.
1. Tegevuspaanil valige luba **varude** nähtavuse uuesti lubamiseks. Lisandmoodul laaditakse uuesti ja uus funktsioon on nüüd lubatud. Laotöölehega seotud andmete sünkroonimine varude nähtavusega algab.

## <a name="query-on-hand-quantities-of-whs-items"></a>Laoala kaupade laokoguste päring

WhS-kaupade päringu esitamiseks kasutate sama rakenduse [programmeerimisliidest (API)](inventory-visibility-api.md) ja sõnumi süntaksit, mida kasutate mitte-WHS-kaupade puhul. Te ei pea määrama, kas kaup on lao- või laoala mitte-laoala kaup. Lao nähtavus eristab automaatselt kaupu, mis põhinevad talletatud andmetel.

Whs-i kaupade päringute tulemused on põhiliselt samad, mis mitte-WHS-kaupade tulemused. Ainus erinevus on see, et andmeallika järgmised füüsilised `fno` meetmed arvutatakse laohaldusloogika alusel tarneahela haldamises:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Kõik muud füüsilised meetmed arvutatakse nii, nagu need on, kui lao nähtavuse täpsema laovaru funktsioon on keelatud.

Üksikasjalikku teavet laohalduse kaupade vaba kaubavaru kalkulatsioonide töö kohta vt laohalduse [valgest raamatust Reserveeringud](https://www.microsoft.com/download/details.aspx?id=43284).

Andmeüksused, mis eksporditakse, ei Dataverse saa veel laoala kaupade koguseid värskendada. Andmeüksustes kuvatavad kogused on õiged nii mitte-laoala kaupade kui ka koguste puhul, mida ei mõjuta lao teatud laoala loogika (st kogused, `AvailPhysical` v.a kogused, `AvailOrdered` ja `ReservPhysical``ReservOrdered``fno` andmeallikas).

Laohalduse kaubakoguste muutmine, mis on talletatud tarneahela haldamise andmeallikas, on keelatud. Nagu ka teiste varude nähtavuse funktsioonide puhul, jõustatakse see piirang konfliktide vältimiseks.

## <a name="soft-reservations-on-whs-items-in-inventory-visibility"></a>Laotöölehe kaupadele varude nähtavuses tehtud kerged reserveerimised

Üldiselt toetatakse laoteenuste [kaupade kergeid](inventory-visibility-reservations.md) reserveeringuid. Laoalaga seotud füüsilised kalkulatsioonid saate lisada ka kerge reserveerimise arvutustesse. 

Teadaolevas piirangus ei toetata *praegu* laoarvestuse kaupade puhul saadaolevat reserveeringu arvutamiseks saadaolevat kogust. Seega, kui esineb reserveeringuid praeguste dimensioonide kohal, kus toimub kerge reserveerimine, *on saadatav reserveerimise arvutamine* vale. Kergeid reserveeringuid ei mõjutata, kui **valik ifCheckAvailForReserv** on kerge reserveerimise [API-s keelatud](inventory-visibility-api.md#create-one-reservation-event).

See piirang kehtib ka funktsioonidele ja kohandustele, mis põhinevad kergetel reserveerimistel (nt eraldus).

## <a name="calculate-available-to-promise-quantities"></a>Arvuta lubaduse jaoks saadaolevad kogused

Lahendus toetab täielikult saadaolevat [laoteenuste (ATP)](inventory-visibility-available-to-promise.md) lubamist. ATP arvutusi saab määratleda laoalapõhiseid üksikasju mõjutamata.
