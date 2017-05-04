---
title: "Müügitellimuste mobiilne tööruum rakendusele Microsoft Dynamics 365 for Operations"
description: "Müügitellimuste mobiilse tööruumiga saate end oma müügitellimustega kõikjal ja alati kursis hoida."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267134
ms.assetid: dbc6dc39-b535-42d3-9fbd-4724597388ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 851c53e1c53fb37488ed86e25e3ede83ca0541db
ms.lasthandoff: 03/31/2017


---

# <a name="sales-orders-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Müügitellimuste mobiilne tööruum rakendusele Microsoft Dynamics 365 for Operations

Müügitellimuste mobiilse tööruumiga saate end oma müügitellimustega kõikjal ja alati kursis hoida. 

<a name="prerequisites"></a>Eeltingimused
-------------

| Eeltingimus                                                         | Kirjeldus                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lugege teavet Microsoft Dynamics 365 for Operationsi mobiiliplatvormi kohta | [Dynamics 365 for Operationsi mobiilne platvorm](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | Veenduge, et kasutaksite keskkonda, millesse on installitud Microsoft Dynamics 365 for Operationsi versioon 1611 ja Microsoft Dynamics for Operationsi platvormivärskendus 3 (november 2016). |
| Kiirparandus KB 3215650                                                    | Installige kiirparandus, et lubada rakenduses Microsoft Dynamics 365 for Operations sisestatud tööruumid.                                                                       |
| Mobiilne seade, kuhu on installitud rakendus Dynamics 365 for Operations | Laadige mobiilirakenduste poest alla rakendus Dynamics 365 for Operations.                                                                                                      |

## <a name="overview"></a>Ülevaade
see mobiilne tööruum pääseb juurde Dynamics 365 for Operationsi rakendusele ja võimaldab teil vaadata iga müügitellimuse kohta üksikasjalikke andmeid nagu tellimuse olek, kliendi kontaktandmed ja tellimuse vastuvõtja andmed. Mobiilne tööruum annab müügitellimustest kiirülevaate. Saate vaadata müügitellimusi klientide kaupa või vaadata kõiki müügitellimusi või vaadata konkreetse müügitellimuse andmeid. Mobiilne tööruum pakub kahte vaadet, mis aitavad teil müügitellimusi põhjalikult analüüsida.

### <a name="view-all-sales-orders"></a>Kõigi müügitellimuste kuvamine

Selles vaates loetletakse kõik müügitellimused.

-   Mõne järgmise filtri abil saate valida müügitellimused, mida vaadata soovite.
    -   Otsing müügitellimuse alusel
    -   Otsing kliendikonto järgi
    -   Otsing kliendi nime järgi
    -   Otsing oleku järgi
    -   Otsing väljastamisoleku järgi
    -   Otsing loomise kuupäeva ja kellaaja järgi

<!-- -->

-   Pärast müügitellimuste valimist saate konkreetsete tellimuste andmeid vaadata. Täpsemalt saate vaadata järgmist.
    -   Kliendi nimi ja aadressiandmed
    -   Erinevad müügitellimuse kuupäevad, nt soovitud lähetuskuupäev ja kinnitatud lähetuskuupäev
    -   Tellimuse vastuvõtja kontaktandmed
    -   Kliendi kontaktandmed
    -   Tellimuse read
    -   Saadetised, mis näitavad, kuidas ja millal müügitellimus on teele pandud

### <a name="view-orders-for-a-customer-"></a>Kuva kliendi tellimused** **

Selles vaates on loetletud müügitellimused kliendi kohta.

-   Mõne järgmise filtri abil saate vaadata kliendi tellimusi.
    -   Otsing nime alusel
    -   Otsing konto alusel

<!-- -->

-   Pärast kliendi valimist saate vaadata järgmist.
    -   Kliendi nimi ja grupp
    -   Kliendi kontaktandmed
    -   Kliendi müügitellimused ja müügitellimuste andmed:
        -   Kliendi nimi ja aadressiandmed
        -   Erinevad müügitellimuse kuupäevad
        -   Tellimuse vastuvõtja kontaktandmed
        -   Kliendi kontaktandmed
        -   Tellimuse read
        -   Saadetised, mis näitavad, kuidas ja millal müügitellimused on teele pandud

## <a name="get-started"></a>Alusta
Mobiilses seadmes müügitellimuste mobiilse tööruumi kasutamise alustamiseks tehke järgmist.

1.  Laadige mobiilirakenduste poest alla rakendus Microsoft Dynamics 365 for Operations ja installige see.
2.  Käivitage rakendus oma seadmes.
3.  Sisestage Dynamics 365 URL.
4.  Sisestage ettevõte, millesse soovite sisse logida. Näiteks sisestage **USMF**.
5.  Esmakordsel sisselogimisel palutakse teil sisestada oma Microsoft Dynamics 365 for Operationsi konto kasutajanimi ja parool. Sisestage oma identimisteave. Pärast sisselogimist näete oma ettevõtte jaoks saadaolevaid tööruume.

Tööruumide vaatamiseks mobiilirakenduses peate soovitud tööruumid esmalt avaldama rakenduses Microsoft Dynamics 365 for Operations.

1.  Käivitage Dynamics 365 for Operations.
2.  Minge jaotisse **Süsteemihaldus** &gt; **Seadistus** &gt; **Süsteemi parameetrid**.
3.  Valige suvand **Mobiilirakenduse haldamine**.
4.  Valige tööruum mobiiliplatvormile avaldamiseks.
5.  Valige käsk **Avalda tööruum**.
6.  Värskendage seadet, et näha avaldatud tööruume.

## <a name="view-information-about-sales-orders-for-a-customer"></a>Kliendi müügitellimuste kohta teabe kuvamine
1.  Valige oma mobiilses seadmes tööruum **Müügitellimused**.
2.  Valige **Kuva kliendi tellimused**.
3.  Kasutage teavet **Konto **või **Kliendi nimi **soovitud kliendi leidmiseks.
4.  Valige klient.
5.  Valige **Kontaktandmed** või **Müügitellimused**.
6.  Kui on valitud **Müügitellimused**, kuvatakse kliendi müügitellimused.
7.  Valige **Müügitellimus**.
8.  Siin saate vaadata teavet müügitellimuse ridade ja saadetiste kohta, kliendi kontaktandmeid ja tellimuse vastuvõtja kontaktandmeid.




