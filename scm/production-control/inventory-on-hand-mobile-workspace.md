---
title: "Varude vaba mobiilne tööruum Microsoft Dynamics 365 toimingute App"
description: "Varude vaba mobiilne tööruumi aitab teil saavutada mobiilne teadmisi reserveeritud ja saadaval igal ajal ja igal pool."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 85058f55-e566-40e2-9234-42d3e4fe5ff6
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 2ad48765528e1d1c6e7c90417b54a248ec79f546
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Varude vaba mobiilne tööruum Microsoft Dynamics 365 toimingute App

Varude vaba mobiilne tööruumi aitab teil saavutada mobiilne teadmisi reserveeritud ja saadaval igal ajal ja igal pool. 

<a name="prerequisites"></a>Eeltingimused
-------------

| Eeltingimus                                                         | Kirjeldus                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Lugeda Microsoft Dynamics 365 toimingute mobiilne platvorm | [Dynamics 365 toimingute mobiilne platvorm](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                   |
| Dynamics 365 toiminguteks                                          | Keskkond, mis on Microsoft Dynamics 365 toiminguid versiooni 1611 ja Microsoft Dynamics toimingute platvormi update 3 (November 2016) |
| Käigultparanduse KB 3215650                                                    | Installige käigultparandus et tööruumid, mis on toodud teie Microsoft Dynamics 365 toiminguteks.                                       |
| Mobiilne seade, mis on toimingute App installitud Dynamics 365 | Lae toimingute rakenduse Dynamics 365 mobiilne app-store.                                                                           |

## <a name="introduction"></a>Sissejuhatus
Tavaliselt ettevõtted on mitu ühikud ja mitme sissetuleku varude iga päev. Need liikumised pidevalt olekuks vaba kaubavaru. Varude vaba mobiilne tööruumi saab näha risti-ettevõtte vaba kaubavaru oleku nii, et sa saaksid varude andmeid valitud mobiilsideseadme uusimaid teadmisi. Olenemata sellest, kas teil töötada lao, ostu, müügi, tootmise ja juhtimise või on teisi rolle, võite kasutada vaba kaubavaru andmeid igal ajal ja igal pool. Tööruumi mobiil annab vahetu ülevaate vaba staatuse vahendid ja võimaldab vaadata vaba kaubavaru vahendid, praeguse materjali broneerimine ja vaba kaubavaru. Võite sisestada kaubakoodide päringut vaba kaubavaru, ja saate filtreeritud otsida vaba tooteid või variandid. Täpsemalt mobiilne workspace pakub neid funktsioone:

-   Võite otsida toote number või toote nimi leida tooteid vaba kaubavaru oleku vaatamine.
-   Valitud toodete, kuvatakse järgmine teave:
    -   Vaba kaubavaru ühe koha
    -   Vaba kaubavaru lao kohta
    -   Vaba kaubavaru asukoha kohta
    -   Vaba kaubavaru partii (partii kontrollitud toodete puhul)
    -   Vaba kaubavaru kohta varude olek

<!-- -->

-   Toote vaba kaubavaru kuvatakse järgmiselt:
    -   Poolt inventuuri (see vaade kujutab endast kogusummat).
    -   Füüsiliselt reserveeritud (selles vaates esindab broneeritud summa).
    -   Saadaval füüsiliselt (see vaade on saadaval summa ei ole.)

## <a name="get-started"></a>Alusta
Algas mobiilne seade:

1.  Poest mobiilirakenduse alla laadida ja installida Microsoft Dynamics 365 toimingute app.
2.  Käivitada rakendus oma seadmes.
3.  Sisestage oma Dynamics 365 URL.
4.  Sisestage ettevõtte sisse logima. Sisestage **USMF**.
5.  Esimene kord, kui logite sisse, küsitakse kasutajanime ja parooli teie Microsofti Dynamics 365 operatsioonide tarbeks. Sisestage oma kasutajanimi ja parool. Pärast sisselogimist, näed saadaval tööruumid firmale.

Saate vaadata oma mobiilirakendus tööruumid, peab esmalt avaldama soovitud tööruumid toimingute rakenduse Dynamics 365.

1.  Käivitage Dynamics 365 toiminguteks.
2.  Mine **süsteemi halduse**&gt;**install**&gt;**süsteemi parameetrid**.
3.  Valige **Halda mobiilirakendus**.
4.  Valige tööruumis avaldada mobiilsel platvormil.
5.  Valige **avaldada tööruumi**.
6.  Värskendage seadme avaldatud tööruumid.

## <a name="view-the-onhand-inventory-for-a-product"></a>Vaata toote lao taastäitmise
1.  Mobiilsideseadmes, valige selle **vaba kaubavaru** tööruumi.
2.  Valige **kontrollige vaba kauba**. Näete nimekirja toodetest, mis on laaditud rakenduse ühenduseta kasutamiseks. Vaikimisi laaditakse 50 tootest, kuid seda numbrit saab muuta. Lisateabe saamiseks vt eelnevalt loe käsiraamat.
3.  Kui teie üksust pole loendis, valige **Otsi rohkem** online Otsi Dynamics 365 toiminguid teha. Otsing toote numbri järgi või aktiveerige Otsi toote nime järgi.
4.  Valige toode. Kui kaubale on pildi, pilt on näidanud.
5.  Tehke järgmised valikud saate vaadata vaba kaubavaru olekut:
    -   Vaata vaba ühe koha
    -   Vaadata vaba kaubavaru lao kohta
    -   Vaata vaba kohta asukohta
    -   Vaata vaba partii (partii kontrollitud toodete puhul)
    -   Vaata vaba kaubavaru oleku kohta

    Toote vaba kaubavaru kuvatakse järgmiselt:
    -   Poolt inventuuri (see vaade kujutab endast kogusummat).
    -   Füüsiliselt reserveeritud (selles vaates esindab broneeritud summa).
    -   Saadaval füüsiliselt (selles vaates esindab saadaoleva summa, mis ei ole.)




