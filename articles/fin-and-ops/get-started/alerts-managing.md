---
title: Teatiste pakktöötlus
description: See teema annab teavet teatiste pakktöötluse kohta rakenduses Microsoft Dynamics 365 for Finance and Operations.
author: tjvass
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 482cf30b4f82e8801ebc12e3925c1efb09f7eb1e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546981"
---
# <a name="batch-processing-of-alerts"></a>Teatiste pakktöötlus

[!include [banner](../includes/banner.md)]

Süsteemi Microsoft Dynamics 365 for Finance and Operations teatisi töödeldakse pakktöötluse funktsioonidega. Enne teatiste edastamist tuleb pakktöötlus seadistada.

Rakendus Finance and Operations toetab kahte tüüpi sündmusi.

- Sündmused, mille käivitavad muutuspõhised sündmused. Neile viidatakse ka kui sündmused Loo/Kustuta ja Värskenda.
- Sündmused, mille käivitavad tähtajad.

Pakktöötlust saab seadistada mõlemat tüüpi sündmuse jaoks.
        
## <a name="batch-processing-for-change-based-events"></a>Muutuspõhiste sündmuste pakktöötlus

Rakendus Finance and Operations arvestab kõiki muutuspõhiseid sündmusi, mis on toimunud pärast pakktöötluse viimast käivitamist. Muutusel põhinevad sündmused hõlmavad väljade värskendusi, kirjete kustutamist ja kirjete loomist. Neid sündmusi võrreldakse teatisereeglites seadistatud tingimustega. Kui sündmus kattub reegli tingimustega, loob pakktöötlus teatise.

### <a name="frequency-for-change-based-events"></a>Muutuspõhiste sündmuste sagedus

Muutusel põhinevate sündmuste jaoks saab seadistada pakett-töö, mis käivitab sündmuse töötlemise varsti pärast seda, kui süsteem on sündmuse registreerinud. Kui seadistate pakett-töö sagedasema kordumise, saavad kasutajad muudatuste toimumisest varem teatiseid. Kuid väga sage pakktöötlus võib ebasoodsalt mõjutada süsteemi jõudlust.

Teisest küljest võib harvemini korduv pakett-töö, mis on plaanitud ajale, mil süsteemi koormus on väike, aidata parandada süsteemi jõudlust. Kuid liiga harv pakktöötlus ei pruugi vastata kasutajate nõudmistele õigeaegsete teatiste osas.

Seetõttu tuleb muutuspõhiste sündmuste pakktöötluse sageduse seadistamisel arvestada teatiste õigeaegsuse ja kogu süsteemi jõudluse vahelist tasakaalu. Sellised kaalutlused on veelgi olulisemad, kui teatisereegleid loovate isikute arv suureneb. Sagedus ei mõjuta töödeldavate sündmuste arvu. Ent mida rohkem on reegleid loovaid kasutajaid, seda rohkem tuleb kontrolle teha. Seda tüüpi andmevahetus võib mõjutada süsteemi jõudlust.

#### <a name="the-risks-of-low-batch-frequency"></a>Väikese sagedusega pakett-töö riskid

Muutuspõhiste sündmuste vähese sagedusega pakktöötlus võib põhjustada olukorra, kus andmed, mis on olulised teatisereegli tingimuste suhtes, võivad muutuda enne pakett-töö käivitamist. Seetõttu võivad teatised kaotsi minna.

Näiteks on teatisereegel seadistatud käivitama teatise juhul, kui sündmus on **Kliendi kontaktandmete muutumine** ja tingimuseks on **Klient = BB**. Teisisõnu, kui muudetakse kliendi BB kliendikontakti, logitakse sündmus. Siiski on pakktöötluse süsteem seadistatud selliselt, et pakktöötlus käivitatakse harvemini kui andmesisestus. Kui kliendi nimi on muudetud **BB-st** **AA-ks** enne sündmuse töötlust, ei ühti enam reegli tingimus **klient = BB** andmebaasis olevate andmetega. Seetõttu ei looda hilisemal sündmuse töötlusel teatist.

### <a name="set-up-processing-for-change-based-alerts"></a>Muutusepõhiste teatiste töötlemise seadistamine

1. Avage **Süsteemihaldus** &gt; **Perioodilised ülesanded** &gt; **Teatised** &gt; **Muutuspõhised teatised**.
2. Sisestage asjakohane teave dialoogiboksi **Muutuspõhised teatised**.

## <a name="batch-processing-for-due-date-events"></a>Tähtajaliste sündmuste pakktöötlus

Rakendus Finance and Operations tuvastab kõik tähtaegadest tingitud sündmused ja neid sündmusi võrreldakse teatisereeglites seadistatud tingimustega. Kui sündmus kattub reegli tingimustega, loob pakktöötlus teatise.

### <a name="frequency-for-due-date-events"></a>Tähtajaliste sündmuste sagedus

Võimalik, et soovite seadistada tähtajaliste sündmuste jaoks pakett-tööd, mida käivitatakse süsteemi koormuse tasakaalustamiseks kas öösiti või kindlal päevasel kellaajal. Soovitatav on seadistada pakett-töö selliselt, et seda käivitataks vähemalt üks kord päevas. Kui teatisi tuleks väljastada võimalikult varakult, siis tuleks pakktöötlus seadistada toimuma võimalikult vahetult pärast süsteemi kuupäeva muutmist. Tähtajaliste sündmuste teatiste loomiseks pärast seda, kui tähtajaliste sündmuste pakett-töö on juba toimunud, võib pakett-töö samal päeval uuesti käitada.

Näiteks on pakett-töö teatud päeval käivitatud. Seejärel loote ostutellimuse, millel on tähtaeg, mis peaks teatise samal päeval käivitama. Sel päeval teatise saamiseks peate pakett-töö pärast ostutellimuse loomist uuesti käivitama. Kui aga pakett-tööd samal päeval uuesti ei käivitata, siis tuvastab järgmise päeva pakett-töö kõik eelmisel päeval töötlemata jäänud tähtajalised sündmused.

> [!NOTE]
> Isegi kui pakktöötlus toimub rohkem kui korra päevas, ei dubleerita teatist sama tähtajalise sündmuse ja tingimuste jaoks. Kõigi saabunud tähtaegade puhul luuakse teatisi ainult juhul, kui muutused on süsteemis toimunud pärast pakett-töö viimast käivitamist.

### <a name="batch-processing-window"></a>Pakktöötluse aken

Ettevõtte teatisereeglite töötlemine võidakse peatada mitmel põhjusel. Nende põhjuste hulka kuuluvad puhkused, süsteemi tõrked või muud probleemid, mis takistavad mõneks ajaks pakett-tööde käitamise.

Vältimaks tähtajaliste teatiste muutumist aegunuks seetõttu, et pakett-tööd pole mitu päeva käivitatud, saate seadistada pakktöötluse akna. Pakktöötluse akent saab kasutada, et takistada pakett-töö käivitamist määratud päevade arvu jooksul.

Pakktöötluse akna seadistamisel saadetakse teatis teatisereegli töötlemise kohta ka juhul, kui teatis ületab tähtaja kriteeriumides määratud ajalimiidi. Teatise väljastamist jätkatakse seni, kuni pole ületatud ajalimiidis määratud perioodi ega pakktöötluse akent. Kuid teatist ei saadeta, kui ületatakse ajalimiidiks määratud periood ja pakktöötluse aken.

### <a name="set-up-processing-for-due-date-alerts"></a>Tähtajapõhiste teatiste töötlemise seadistamine

1. Avage **Süsteemihaldus** &gt; **Perioodilised ülesanded** &gt; **Teatised** &gt; **Tähtajateatised**.
2. Sisestage asjakohane teave dialoogiboksi **Tähtajateatised**.
