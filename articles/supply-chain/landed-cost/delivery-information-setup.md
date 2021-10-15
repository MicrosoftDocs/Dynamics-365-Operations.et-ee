---
title: Tarneteabe häälestus
description: Selles teemas kirjeldatakse, kuidas seadistada tarneteavet moodulis Väljalaadimiskulu.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMPortTable, ITMLeadTimeTable, ITMLegTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 57f17d481f9660d67b96ac2c8e68558407b1bcf9
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577596"
---
# <a name="delivery-information-setup"></a>Tarneteabe häälestus

[!include [banner](../../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas seadistada tarneteavet moodulis **Väljalaadimiskulu**.

## <a name="shipping-ports"></a>Saatmise sadamad

Saatmissadamad määratlevad, kust ja kuhu kaupu saadetakse. Iga teekonna puhul määratletakse sihtsadam ja lähtesadam, mis põhinevad teekonna laeva jaoks valitud teekonnal. Saatmissadamaid kasutatakse teekonna etappide ja teekonnategevuste loomiseks. Tavaliselt määratletakse need linna ja riigi või regiooni nimega, kus asub kauba füüsilise saatmissadam.

Saatmiskonteineritega töötamiseks avage **Väljalaadimiskulu \> Tarneteabe seadistus \> Saatmissadamad**. Seal saate oma saatmissadamate kirjeid vaadata, lisada ja eemaldada. Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Saatmissadam | Sisestage saatmissadama ainu-ID nimi/number. |
| Kirjeldus | Sisestage saadmissadama kirjeldus. |

## <a name="tracking-control-center"></a><a name="tracking-control-center"></a>Jälgimise juhtimiskeskus

Te kasutate jälgimiskontrollikeskust, et seadistada täitmisajad, olekuvärskendused ja teeekonnaga seotud teabevoo, kui saatmiskonteinerid liiguvad ühelt etapilt järgmisele. Jälgimiskontrolli kirje loomisel seotakse see teekonna konkreetse etapiga. Kui teekonna etappi uuendatakse, uuendatakse sellega seotud kirjet ja täidetakse vastavalt määratlusele. Üksikteekondade jälgimisteavet saate uuendada lehel **Kõik teekonnad**.

Jälgimiskontrolli keskuse avamiseks valige **Väljalaadimiskulu \> Tarneteabe häälestus \> Jälgimiskeskus**.

Jälgimiskontrollikeskuses kuvatakse üks kolmest lehevaatest, sõltuvalt loendipaani väljal **Loo tüüp** valitud väärtusest: *Tühi*, *Täitmisaeg* või *Olekuvärskendus*. Iga loomistüüp uuendab erinevat teabekomplekti, mis on seotud teekonna edenemisega lähtepunktist lõppsihtkohta.

### <a name="common-rule-settings"></a>Üldised reeglisätted

Järgnevas tabelis kuvatakse väljad, mis on saadaval kõigi kolme loomistüübi jaoks jälgimiskontrollikeskuses.

| Field | Kirjeldus |
|---|---|
| Lähtetabel, lähteväli | Need väljad määratlevad andmebaasis lähtetabeli ja -välja. Reegel laadib väärtuse väljale ja kasutab seda siis viisil, mis on määratletud muude reeglisätetega. |
| Sihttabel, sihtväli | Need väljad määratlevad andmebaasis sihttabeli ja -välja. Reegel laadib väärtuse väljale ja siis kasutab seda (või kirjutab selle üle) viisil, mis on määratletud muude reeglisätetega. |
| Tegevus | See väli tuvastab tegevuse tüübi, mida tuleks rakendada reegliga vastendatud saatmiskonteinerile. |
| Vastendamiskriteeriumid | See väli määrab, kuidas süsteem tuvastab reegli vaste. Igas eksemplaris vaatab süsteem üle lähte- ja sihttabelite andmed, et määratleda, kas ja millal tuleks välja sihttabelis uuendada.<p>Lähtetabeliks on näiteks *Teekonnad* ja sihttabeliks on *Ostu päis* või *Ostu read*. Tabelis *Teekonnad* on suvandi **Lähtesadam** väärtus *Hongkong* ja tabelis *Ostu päis* on suvandi **Lähtesadam** väärtus *Shanghai*. Seejärel luuakse reegel, milles sihtsadamaks on *Hongkong*. Sellisel juhul töötavad välja **Vastendamiskriteeriumid** väärtused järgmiselt:</p><ul><li>**Mõlemad** – sihtvälja ei uuendata, kuna üks kahest sadamast ei ühti.</li><li>**Lähtepunkt** – sihtvälja uuendatakse, sest lähtetabeli lähtesadam on *Hongkong*.</li><li>**Sihtpunkt** – sihtvälja ei uuendata, sest sihttabeli lähtesadam on *Shanghai* (mitte *Hongkong*).</li></ul> |
| Kopeeri tegevus | Saadaolevad väärtused on *Kopeeri* ja *Vaikimisi*. Väärtuse kopeerimiseks lähteväljalt sihtväljale valige *Kopeeri*. Sihtväljale staatilise väärtuse määramiseks valige *Vaikimisi*. |
| Vaikimisi | Kui välja **Kopeerimistoiming** väärtuseks on seatud *Vaikimisi*, määratleb väli **Vaikimisi** sihtvälja vaikeväärtuse. Näiteks kui tegevus on seotud sadama uuendamisega ja välja **Kopeerimistoiming** väärtuseks on seatud *Vaikimisi*, määratleb väli **Vaikimisi** sadama. |
| Etapp | See väli määrab teekonna selle etapi, mille jaoks määratud tegevus aset leiab, nt laadimine või toll. |
| Teenusepakkuja | Kui praeguse olekuvärskenduse/teekonnaetapi jaoks kasutatakse konkreetset teenusepakkujat, siis määratleb see väli teenusepakkuja. Teenusepakkujad määratletakse hankija kontol. |

### <a name="lead-time-rules"></a>Täitmisaja reeglid

Täitmisaeg on hinnanguline aeg, mille jooksul reisi nõuab reisi jaoks määratletud teekonnaetapi lõpuleviimist. Reisi eeldatava tarnekuupäeva arvutamiseks kasutatakse reisi iga teekonnaetapi täitmisaega. See kuupäev sisestatakse siis reisi igal osturea väljale **Kinnitatud tarnekuupäev**.

Täitmisaja reegleid kasutatakse kuupäevauuenduste haldamiseks. Tegevused luuakse automaatselt, kui reisi jaoks kasutatakse teekonnamalli.

Täitmisaja reegli lisamiseks jälgimiskeskusesse järgige neid samme.

1. Järgige üht neist sammudest.

    - Avage **Väljalaadimiskulu \> Mitmeetapilise teekonna marsruudi seadistamine \> Etapid**. Valige etapp, mille jaoks soovite täitmisajad seadistada, ja seejärel valige tegevuspaanil **Jälgimiskontrollikeskus**. Jälgimiskontrollikeskus eellaaditakse koos teabega valitud etapi kohta.
    - Valige **Väljalaadimiskulu \> Tarneteabe seadistamine \> Jälgimiskontrollikeskus**. Seejärel peate selle protseduuri 4. toiminguna käsitsi valima etapi.

1. Seadke loendipaanil välja **Loo tüüp** väärtuseks *Täitmisaeg*.
1. Valige toimingupaanil nupp **Uus**.
1. Kui alustasite 1. toimingus jälgimiskontrollikeskusest, seadke välja **Etapp** väärtuseks see etapp, mille jaoks soovite täitmisaja reegli luua. Kui alustasite lehelt **Etapid**, on välja **Etapp** väärtuseks eelnevalt määratud etapp, mille valisite enne jälgimiskontrollikeskuse avamist.

    Vastavalt välja **Etapp** väärtusele seadistatakse automaatselt mitu välja, nagu siin näha:

    - **Lähtetabel:** *Konteineri tegevused*
    - **Lähteväli:** *Alguskuupäev*
    - **Sihttabel:** *Konteineri tegevused*
    - **Sihtväli:** *Eeldatav lõppkuupäev*

1. Valige väljal **Tegevus** see tegevus, mille suhtes peaks praegune reegel rakenduma.
1. Sisestage väljale **Täitmisaeg** see täitmisaeg (päevades), mida tuleks rakendada praeguse reegli käivitumisel.

### <a name="status-update-rules"></a>Olekuvärskenduse reeglid

Kirjed, milles välja **Loo tüüp** väärtuseks on seatud *Olekuvärskendus*, värskendavad ostutellimuse ridade olekut või reisi olekut reisi saatmiskonteineri või foolio tasemel. Olekuid saab sõltumatult seadistada. Kasutage neid, et kasutajat või osakonda reisi etapist teavitada (nt vastuvõetud dokumendid või transiidis olevad kaubad).

Kui välja **Loo tüüp** väärtuseks on seatud *Olekuvärskendus*, sisaldab jälgimisjuhtimiskeskus kiirkaarti **Read**, kus saate määratleda kuluala ja reisi värskendatud oleku. Näiteks on teil rida, kus välja **Kuluala** väärtuseks on seatud *Konteiner* ja väli **Reisi olek** on seatud väärtusele *Transiidis olevad kaubad*. Sel juhul värskendatakse siis, kui tellimuse konkreetne etapp jõuab lõpule, saatmiskonteineri väli **Reisi olek** väärtusele *Transiidis olevad kaubad*.

Olekuvärskendused annavad teavet reisi oleku kohta reisiridadel ja selle reisiga seotud ostutellimuse ridadel. Kui reis liigub oma teekonnal läbi sadama, laevasõidu ja tolli sihtlattu, annab reisikirje väli **Reisi olek** kiiresti ülevaate olekust, milles kaubad on.

Olekuvärskenduse reegli lisamiseks jälgimiskeskusesse järgige neid samme.

1. Järgige üht neist sammudest.

    - Avage **Väljalaadimiskulu \> Mitmeetapilise teekonna marsruudi seadistamine \> Etapid**. Valige etapp, mille jaoks soovite olekuvärskenduse seadistada, ja seejärel valige tegevuspaanil **Jälgimiskontrollikeskus**. Jälgimiskontrollikeskus eellaaditakse koos teabega valitud etapi kohta.
    - Valige **Väljalaadimiskulu \> Tarneteabe seadistamine \> Jälgimiskontrollikeskus**. Seejärel peate selle protseduuri 4. toiminguna käsitsi valima etapi.

1. Seadke loendipaanil välja **Loo tüüp** väärtuseks *Olekuvärskendus*.
1. Valige toimingupaanil nupp **Uus**.
1. Kui alustasite 1. toimingus jälgimiskontrollikeskusest, seadke välja **Etapp** väärtuseks see etapp, mille jaoks soovite olekuvärskenduse reegli luua. Kui alustasite lehelt **Etapid**, on välja **Etapp** väärtuseks eelnevalt määratud etapp, mille valisite enne jälgimiskontrollikeskuse avamist.

    Vastavalt välja **Etapp** väärtusele seadistatakse automaatselt mitu välja, nagu siin näha:

    - **Lähtetabel:** *Konteineri tegevused*
    - **Lähteväli:** *Tegelik lõppkuupäev*
    - **Sihttabel:** see väli jäetakse tühjaks.
    - **Sihtväli:** see väli jäetakse tühjaks.

1. Valige väljal **Tegevus** see tegevus, mille suhtes peaks teie reegel rakenduma.
1. Sisestage kiirkaardil **Read** igale kulualale olekuvärskendused.

### <a name="blank-type-rules"></a>Tühja tüübi reeglid

Kirjeid, mille välja **Loo tüüp** väärtus on *Tühi*, kasutatakse selleks, et alistada või sisestada välja väärtus mõne muu välja andmete põhjal. Väljalaadimiskulu väli kirjutab jälgimiskontrollikeskuses häälestatud reeglite alusel Microsoft Dynamics 365 Supply Chain Managementi muudel aladel olevad andmed üle.

1. Valige **Väljalaadimiskulu \> Tarneteabe seadistamine \> Jälgimiskontrollikeskus**.
1. Seadke loendipaanil välja **Loo tüüp** väärtuseks *Tühi*.
1. Valige toimingupaanil nupp **Uus**.
1. Määratlege lähte- ja sihtväärtused, vastendamiskriteeriumid, kopeerimistegevus ja muud asjakohased parameetrid vastavalt reegli nõuetele.

### <a name="required-tracking-control-setup"></a>Nõutav jälgimiskontrolli häälestus

Iga teekonnamalli kohta tuleb jälgimiskontrollikeskuses seadistada kaks kirjet. Mõlema kirje puhul on välja **Loo tüüp** väärtus *Tühi* ja neid kasutatakse kõikides väljalaadimiskulu juurutustes. Need aitavad tagada, et ostu kinnitatud kuupäeva ja transiidis olevate kaupade eeldatavaid kuupäevi uuendatakse reiside kohta ja seotud ostutellimuste ridadel eeldataval viisil.

Esimene kirje on kohustuslik osturidade värskendamiseks. Sellel peavad olema järgmised sätted:

- **Lähtetabel:** *Konteineri tegevused*
- **Lähteväli:** *Eeldatav lõppkuupäev*
- **Sihttabel:** *Osturead*
- **Sihtväli:** *Kinnitatud või tarnekuupäev*

Teine kirje on nõutav transiidis olevate kaupade värskendamiseks. Sellel peavad olema järgmised sätted:

- **Lähtetabel:** *Konteineri tegevused*
- **Lähteväli:** *Eeldatav lõppkuupäev*
- **Sihttabel:** *transiidis olevate kaupade tellimus*
- **Sihtväli:** *Eeldatav kuupäev*
