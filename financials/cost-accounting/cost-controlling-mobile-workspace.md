---
title: "Kulujuhtimise mobiilne tööruum rakendusele Microsoft Dynamics 365 for Operations"
description: "Kulujuhtimise mobiilse tööruumi abil saavad kulukeskuse haldurid näha kulukeskuse jõudlust igal ajal ja igas kohas."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 53 - 04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 84740472-494f-444c-9b74-f83b7342fd25
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 8136efb1d2669c39fcc0f80b60e80ecae983d5d8
ms.lasthandoff: 03/31/2017


---

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Kulujuhtimise mobiilne tööruum rakendusele Microsoft Dynamics 365 for Operations

Kulujuhtimise mobiilse tööruumi abil saavad kulukeskuse haldurid näha kulukeskuse jõudlust igal ajal ja igas kohas. 

<a name="prerequisites"></a>Eeltingimused
-------------

| Eeltingimus                                                         | Kirjeldus                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lugege teavet Microsoft Dynamics 365 for Operationsi mobiiliplatvormi kohta | [Dynamics 365 for Operationsi mobiilne platvorm](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | Veenduge, et kasutaksite keskkonda, millesse on installitud Microsoft Dynamics 365 for Operationsi versioon 1611 ja Microsoft Dynamics for Operationsi platvormivärskendus 3 (november 2016). |
| Kiirparanduse KB 3215650                                                    | Installige kiirparandus, et lubada rakenduses Microsoft Dynamics 365 for Operations sisestatud tööruumid.                                                                       |
| Mobiilne seade, kuhu on installitud rakendus Dynamics 365 for Operations | Laadige mobiilirakenduste poest alla rakendus Dynamics 365 for Operations.                                                                                                      |

## <a name="introduction"></a>Sissejuhatus
Kulujuhtimise mobiilne tööruum annab kiire ülevaate kulukeskuste praegusest jõudlusest, võrreldes tegelikke kulusid eelarvestatud kuludega. Saate üksikute kuluelementide olekuid ka sügavuti uurida.

### <a name="example"></a>Näide

Töövõtja saab kutse rahvusvahelisele konverentsile. Organisatsioon peab katma kõik reisikulud. Töövõtja küsib oma juhilt, kas ta saab konverentsil osaleda. Juht avab oma mobiiltelefonis kiiresti kulukeskuse mobiilse tööruumi, et näha, kas tal on töövõtja konverentsil osalemiseks olemas eelarvevahendid.

### <a name="data-security"></a>Andmeturve

Kulujuhtimise tööruumis olevad andmed on kaitstud kasutaja identimisteabega. Ainult kulukeskuse juhil on õigus näha oma kulukeskuse andmeid. Juurdepääsu turbetaset hallatakse kuluarvestuse moodulis. Kuluarvestajad määratlevad kulujuhtimise mobiilse tööruumi konfiguratsiooni kuluarvestuse moodulis. Kui tööruum on avaldatud rakenduses Microsoft Dynamics 365 for Operations, on see saadaval Dynamics 365 for Operationsi mobiilirakenduses. See tagab, et kõik organisatsiooni kulukeskuse juhid näevad andmeid samas vormingus.

### <a name="actions-views-and-links"></a>Toimingud, vaated ja lingid

Kulujuhtimise mobiilne tööruum rakendusele Microsoft Dynamics 365 for Operations võimaldab kasutada järgmisi toiminguid, vaateid ja linke.

-   Tegevused 
    -   Valige paigutuse valimiseks suvand **Konfiguratsioonid**.
    -   Valige suvand **Kuluobjektid**, et valida kulukeskused, mille põhjal soovite andmeid filtreerida. **Märkus.** Loend kuvatakse vastavalt kuluarvestuse moodulis antud juurdepääsutasemele.

<!-- -->

-   Olenevalt jaotises **Toimingud** tehtud valikutest ja kuluarvestuse moodulis konfigureeritud parameetritest saate vaadata kaartidel järgmist teavet. Pange tähele, et summa kuvatakse samas vormingus: tegelik, eelarve, hälve ja hälbe %. 
    -   Tegelik võrreldes eelarvega (praegune periood)
    -   Tegelik võrreldes parandatud eelarvega (praegune periood)
    -   Tegelik võrreldes eelarvega (eelmine periood)
    -   Tegelik võrreldes parandatud eelarvega (eelmine periood)
    -   Tegelik võrreldes eelarvega (aasta tänaseni)
    -   Tegelik võrreldes parandatud eelarvega (aasta tänaseni)

<!-- -->

-   Lingid
    -   Praeguse perioodi üksikasjad.
    -   Eelmise perioodi üksikasjad.
    -   Aasta tänaseni üksikasjad.

Linkidest ühe valimisel kuvatakse kaart kuluelemendi kohta. Kaartidel olev summa kuvatakse järgmises vormingus: tegelik, eelarve, eelarvehälve, eelarvehälbe %, parandatud eelarve, parandatud eelarvehälve ja parandatud eelarvehälbe %.  [![kulujuhtimine](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="get-started"></a>Alusta
Mobiilses seadmes kulujuhtimise mobiilirakenduse kasutamise alustamiseks tehke järgmist.

1.  Laadige mobiilirakenduste poest alla rakendus Microsoft Dynamics 365 for Operations ja installige see.
2.  Käivitage rakendus oma seadmes.
3.  Sisestage Dynamics 365 URL.
4.  Sisestage ettevõte, millesse soovite sisse logida. Näiteks sisestage **USMF**.
5.  Esmakordsel sisselogimisel palutakse teil sisestada oma Microsoft Dynamics 365 for Operationsi konto kasutajanimi ja parool. Sisestage oma identimisteave. Pärast sisselogimist näete oma ettevõtte jaoks saadaolevaid tööruume.

Tööruumide vaatamiseks mobiilirakenduses peate soovitud tööruumid esmalt avaldama rakenduses Microsoft Dynamics 365 for Operations.

1.  Käivitage Dynamics 365 for Operations.
2.  Minge jaotisse **Süsteemihaldus** &gt; **Seadistus** &gt; **Süsteemi parameetrid**.
3.  Valige suvand **Mobiilirakenduse haldamine**.
4.  Valige tööruum **Kulujuhtimine**, et avaldada see mobiiliplatvormile.
5.  Valige käsk **Avalda tööruum**.
6.  Värskendage seadet, et näha avaldatud tööruume.

## <a name="view-the-performance-of-your-cost-center"></a>Kulukeskuse jõudluse vaatamine
1.  Valige oma mobiilses seadmes tööruum **Kulujuhtimine**.
2.  Valige suvand **Kuluobjekti juhtimine**.
3.  Klõpsake valikut **Toimingud**.
4.  Klõpsake kulujuhtimise paigutuse valimiseks valikut **Konfiguratsiooni valimine**.
5.  Klõpsake nuppu **Valmis**.
6.  Klõpsake valikut **Toimingud**.
7.  Valige suvand **Kuluobjekti valimine**, et valida kulukeskused, millele on teil juurdepääs antud.
8.  Klõpsake nuppu **Valmis**.
9.  Kulukeskuse üldise jõudluse vaatamine.
10. Klõpsake valikut **Praeguse perioodi üksikasjad**.
11. Saate vaadata üksikute kuluelementide jõudlust.
12. Samuti saate otsida kindlaid kuluelemente.



