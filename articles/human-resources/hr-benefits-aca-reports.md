---
title: Taskukohase ravikindlustuse eelnõu (ACA) aruannete koostamine
description: Taskukohase ravikindlustuse eelnõu (ACA) aruandlus loob vormid 1095-B ja 1095-C, mis toetavad Taskukohase ravikindlustuse eelnõu **Tööandja kohustuse** osa.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 498705b86b705c70e7e84e3a03e459d02dfcb88f5cfbd4b7ef27e18173c2a1e0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774170"
---
# <a name="generate-aca-reports"></a>ACA aruannete loomine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Taskukohase ravikindlustuse eelnõu (ACA) aruandlus loob vormid 1095-B ja 1095-C, mis toetavad Taskukohase ravikindlustuse eelnõu **Tööandja kohustuse** osa.

> [!NOTE]
> ACA aruandlus on lubatud ainult USA juriidilistele isikutele.

## <a name="getting-started"></a>Alustamine

Vormide 1095-B ja 1095-C jaoks andmete jälgimiseks looge kõigepealt üks või rohkem ravikindlustusega hõlmatud gruppi. Taskukohase ravikindlustuskattega hõlmatud grupid näitavad järgmist.

- Töötajale kindlustuskaitse pakkumine
- Töötaja osa madalaima maksumusega kuumaksest, kui kulu ületab föderaalset vaesuspiiri
- Tööandja kasutatav Safe Harbor, kui see on kohaldatav

Taskukohase ravikindlustuse gurpid võimaldavad hallata nendel väljadel olevaid andmeid, ilma et oleks vaja muuta iga töötajakirjet, kus tingimused on samad. Taskukohase ravikindlustuse grupid saab määrata hõlpsasti vähemalt ühele töötajale, kasutades lehel suvandit **Massiline määramine**.

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>Mitme kindlustusgrupi versiooni säilitamine

Saate säilitada mistahes kindlustuskaitse grupist mitu versiooni. See funktsioon võimaldab teil teha muudatusi ilma, et peate looma uue grupi ja määrama töötajad sellele ümber. 

Pärast ACA kindlustuskaitse gruppide loomist saate **Massilise määramise** suvandiga määrata grupid töötajatele hulgi. Saate ka individuaalselt näidata, kas jälgida ja esitada ACA-teavet ning määrata töötaja Taskukohase ravikindlustuskaitse gruppi.

Te ei pea jälgima mõnda ACA kindlustuskaitse teavet, näiteks osalise tööajaga töötajate puhul. Sellisel juhul määrake välja **Kindlustuskaitse aruandlus** väärtuseks **Ei**. Kuigi peate määrama iga jälgitava ACA-teabega töötaja Taskukohas ravikindlustuskaitse gruppi, saate erineva väärtusega kuude korral ikka järgmisi suvandeid muuta.

- **Katvuse pakkumine**
- **Töötaja kulu osa**
- **Safe Harbor**

Erandite sisestamiseks mõnesse taskukohase ravikindlustuse grupi väärtusse valige lehel **Töötaja üksikasjad** vahekaardi **Tööhõive** jaotises **Täiendav teave** link **Ravikindlustusega hõlmatud** .

## <a name="reporting-health-care-coverage"></a>Tervisekindlustuse registreerimine

Lisaks jälgimisele, millist tervisekindlustust täisajaga töötajatele pakuti, kui tööandja pakub tööandja enda sõlmitud tervisekindlustust, millega töötaja on liitunud (olenemata sellest, kas töösuhe on täisajaga või osalise ajaga), tuleb vormil 1095 C esitada lisateavet. Iga töötaja (sh ülalpeetavad), kelle puhul tööandja toetusega tervisekindlustus kehtib, peavad olema lisatud nende kuude aruandesse, millal neile kindlustus kehtis. 

Saate näidata iga soodustuse plaani kohta, kas see tuleb aruandesse lisada, märkides ruudu **ACA-le esitatav**.

Lisaks, kui töötajad on otsustanud lasta oma ülalpeetavatele soodustuse määrata, võite lehel **Soodustuste haldamine** näidata kuupäevad, millal iga töötaja ülalpeetava kaitse kehtis. Näitamiseks, et ülalpeetavale kehtib soodustus, valige kiirkaardi **Ülalpeetavad** tegumipaanil nupp **Redigeeri**.

Lehel **Ülalpeetava kindlustuse kuupäevahaldur** saate märkida kuupäevad, millal ülalpeetavale soodustus kehtis. Kuupäevade sisestamisel sellele lehele märgitakse automaatselt ruut **Kaitstud** lehel **Soodustuste haldamine**.

## <a name="generate-1095-b-and-1095-c-forms"></a>Vormide 1095-B ja 1095-C loomine

Tootest saab luua ka vormid 1095-B ja 1095-C ning jaotada need igale töötajale. Süsteem saab elektrooniliselt luua ka 1095-C vorme ja 1094-C IRS-i edastusfaile.  

1095-C vormi loomisel sisestage asjakohane maksuaasta ja näidake, kas isikukood peaks olema varjatud. Rohkem kui 500 töötaja 1095-C vormi printimisel saate rohkem kui ühe PDF-faili. On soovitatav, et suurendate väärtust **Faili maksimummaht** aknas **Dokumendihalduse parameetrid** väärtuseni 150 MB.

## <a name="viewing-information"></a>Teabe vaatamine

Lehelt **Töötaja taskukohane ravikindlustus** saate vaadata, millised töötajad on igasse kindlustusgruppi määratud, milliseid töötajaid pole vaja aruandesse lisada ja millised töötajad on määramata.

Kui mõni väärtus taskukohase ravikindlustuse grupist on alistatud, kuvatakse muudetud väärtuse kõrval tärn. Kui kõigi 12 kuu väärtused on samad ja neid pole alistatud, prinditakse väärtus veerus **Kõik 12 kuud**.

Päringuakent saate kasutada ka selleks, et mõista, millised töötajad on märgitud mitte ACA-aruandlusesse kaasatuteks. Te ei pea jälgima, kas neile kindlustuskaitset pakuti ja nende kohta ei ole vaja aasta lõpus esitada vormi 1095-C. Kõigi selliste töötajate loendi loomiseks, kes ei saa vormi 1095-c valige suvand **Ei ole ACA-le esitatav** väljal **Filtreerimisalus**.

Lisaks saate vaadata ka töötajaid, kes on määramata (väli **ACA aruandesse kuuluv** on tühi) või kes on määratud taskukohase ravikindlustuse gruppi, mis on väljal **Aasta** valitud aasta puhul aegunud.

Saate koostatud töötajate nimekirju eksportida, kasutades mis tahes Exceli filtreerimisvalikuid.

Kui peate kindlustuskaitsega inimestest teatama, sest pakute isekindlustuskaitset, saate vaadata ülalpeetavaid, kes on soodustusplaanidega kaitstud ja märgitud kui **ACA-aruandele lisatavad**. Valige toimingupaanil nupp **Vaata ülalpeetavate kindlustuskaitset**.

> [!NOTE]
> Päringuaknas kuvatakse ainult soodustusplaanid, mis on märgitud kui **ACA-aruandele lisatavad**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]