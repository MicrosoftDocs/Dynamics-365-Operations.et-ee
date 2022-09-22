---
title: Partii likvideerimiskoodide kasutamine partiide märkimiseks saadaolevaks või mitte kättesaadavaks
description: See artikkel kirjeldab, kuidas seadistada ja kasutada partii likvideerimiskoode partiide märkimiseks kättesaadavaks või mitte kättesaadavaks koondplaneerimises, reserveerimisel, komplekteerimises ja/või lähetamisel.
author: t-benebo
ms.date: 09/16/2022
ms.topic: article
ms.search.form: PdsDispositionMaster, InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-16
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: cfb0743a573550de93d75063df517e0c143f2568
ms.sourcegitcommit: 20ce54cb40290dd116ab8b157c0a02d6757c13f5
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/20/2022
ms.locfileid: "9542905"
---
# <a name="use-batch-disposition-codes-to-mark-batches-as-available-or-unavailable"></a>Partii likvideerimiskoodide kasutamine partiide märkimiseks saadaolevaks või mitte kättesaadavaks

See artikkel kirjeldab, kuidas seadistada ja kasutada *partii likvideerimiskoode*. Iga partii likvideerimiskoodi olek on Kas Saadav *või* *Pole saadaval*. Määrate partii likvideerimiskoodid varude partiidele, et näidata, kas iga partii on saadaval koondplaneerimise, reserveerimise, komplekteerimise ja/või lähetamise jaoks.

Partii likvideerimiskoodide kasutamiseks peate seadistama koodid ja määrama need partiidele, mida soovite hallata.

## <a name="set-up-batch-disposition-codes"></a>Partii likvideerimiskoodide seadistamine

Peate seadistama iga partii likvideerimiskoodi, mida soovite oma süsteemis kasutada. Saate luua soovitud arvu koode. (Näiteks saate luua koode, et tuvastada erinevad põhjused, miks partii võib olla saadaval või mitte saadaval). Siiski on teil sageli vaid kaks koodi: üks saadaoleva jaoks *ja* teine mittesaadamatute *jaoks*. Saate luua ka kohandatud koode, mis võimaldavad kasutada partiid mõne operatsioonide, kuid mitte teiste jaoks.

Järgige neid samme partii likvideerimiskoodide häälestamiseks.

1. Minge varude **halduse häälestuse \>\> partii \> likvideerimise koondi**.
1. Partii **likvideerimise koondleht loetleb** teie praeguse partii likvideerimiskoodid ja võimaldab teil neid luua, kustutada ja redigeerida. Järgige üht neist sammudest.

    - Olemasoleva koodi redigeerimiseks valige see loendipaanil.
    - Uue koodi loomiseks valige tegevuspaanil **väärtus** Uus.

1. Seadke uue või valitud koodi päisesse järgmised väljad:

    - **Partii likvideerimiskood** – sisestage koodi kuvatav nimi.
    - **Kirjeldus** – kirjeldage koodi kasutamist.
    - **Partii likvideerimisolek** – valige olek, mis rakendub partiidele, millele kood on määratud:

        - *Pole saadaval* – partiisid ei saa kasutada koondplaneerimise, reserveerimise, komplekteerimise või lähetamise jaoks. Kui valite selle väärtuse, seadistatakse kõik **seadistuse** **kiirkaardil** Bloki suvandid valikule Jah *ja* kõik Nettable’i **valikud on seatud valikule** Ei *.* Mõnda neist sätetest saate siiski erandite lisamiseks muuta.
        - *Saadaval* : partiisid saab kasutada koondplaneerimise, reserveerimise, komplekteerimise ja/või lähetamise puhul. Kui valite selle väärtuse, seatakse kõigi **seadistuse** **kiirkaardil** Bloki valikute valikuks Ei *ja* kõigi Nettable-valikute **väärtuseks on seatud** Jah *.* Need sätted on kirjutuskaitstud, kui partii **likvideerimisoleku välja väärtuseks** on seatud *Vaba*.

1. Kui seate **välja** *Partii* likvideerimisolek väärtuseks Pole saadaval, saate kohandada iga toimingu blokeerimisolekut (reserveerimine, komplekte ja lähetamine) iga tellimuse tüübi jaoks (müük, ülekanne ja tootmine). Tootmistellimuste puhul saate valida tootmise komplekteerimise töölehe blokeerimise või blokeeringu tühistamise. Samuti saate koondplaneerimise blokeerida või blokeeringust eemaldada. Iga toimingu blokeerimiseks või **blokeeringu** tühistamiseks vastavalt vajadusele kasutage kiirkaardi Häälestus suvandeid. Määrake koondplaneerimise **lubamiseks suvandi** Nettable *väärtuseks* Jah või seadistage see suvandile *Ei*, et koondplaneerimine blokeerida.

## <a name="assign-batch-disposition-codes-to-batches"></a>Partii likvideerimiskoodide määramine partiidele

Pärast seda, kui olete määranud partii likvideerimiskoodid, mida vajate, järgige neid samme nende määramiseks partiidele.

1. Minge laohalduse seadistuse varude partiidele **\>.\>\>**
1. Valige üks või mitu partiid, mille jaoks määrata partii likvideerimiskood.
1. Tegevuspaani vahekaardil Lähtesta valige **partii** likvideerimiskoodi **lähtestamine**.
1. Dialoogiboksis Muuda **varupartii** piiranguid määrake dialoogiboksis Uus partii **likvideerimiskoodi väli koodi nimele,** mille soovite määrata.
1. Uue **sätte rakendamiseks ja muudatuse salvestamiseks valige OK**.

    Partiide **lehel uuendatakse partii** **·** **likvideerimiskoodi ja partii likvideerimisoleku veergude väärtused nii, et need peegeldavad valitud partiide uusi sätteid.**

## <a name="master-planning-example"></a>Koondplaneerimise näide

See näide näitab, kuidas partii likvideerimiskoodid võivad koondplaneerimist mõjutada.

Selles näites on partii likvideerimiskoodid seadistatud järgmiselt:

- *P-saadaval:*

    - **Partii likvideerimisolek:** *saadaval*
    - **Tasaarveldus:** *Jah*

- *Pole saadaval:*

    - **Partii likvideerimisolek:** *pole saadaval*
    - **Tasaarveldus:** *ei*

On olemas toode (*Toode-1*), kus on kaks partiid: *Partii-A* ja *Partii-B*. Need partiid seadistatakse järgmiselt:

- *Partii A:*

    - **Partii likvideerimiskood:** *P-saadaval*
    - **Vaba kogus:** 1

- *Partii B:*

    - **Partii likvideerimiskood:** *P-pole saadaval*
    - **Vaba kogus:** 1

Müügitellimus (*SO1*) on olemas kogusele 2 tootest *–1*. Tarnekuupäev on kolm päeva alates tänasest.

Käivitate koondplaneerimise ja seadistate järgmised selle näite puhul asjakohased väärtused:

- **Plaanitud tellimus:** *ostutellimus*
- **Täiendusstrateegia:** *nõue*
- **Täitmisaeg:** *0*

Planeerimise käitamise tulemusena kasutab süsteem saadaolevat partiid (Partii A), et katta müügitellimuse SO1 *tootest* 1 *kogus* tootest -1 *.* Partiid Batch-B ei saa siiski *kasutada*, kuna see partii on märgitud planeerimiseks mittesaad kättesaadavaks. Seepärast loob süsteem järelejäänud koguse *katteks uue tootetoote 1* *partii jaoks plaanitud ostutellimuse*.

Järgmine näide näitab plaanimise tulemuse ajajoont.

![Näide, mis näitab, kuidas partii likvideerimiskoodid võivad koondplaneerimist mõjutada.](media/batch-codes-planning-example.png "Näide, mis näitab, kuidas partii likvideerimiskoodid võivad koondplaneerimist mõjutada")
