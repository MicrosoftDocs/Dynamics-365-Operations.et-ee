---
title: "Vaba kaubavaru mobiilne tööruum rakendusele Microsoft Dynamics 365 for Operations"
description: "Vaba kaubavaru mobiilne tööruum aitab saada alati ja kõikjal mobiilseid ülevaateid reserveeritud ja vabadest kaubavarudest."
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

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Vaba kaubavaru mobiilne tööruum rakendusele Microsoft Dynamics 365 for Operations

Vaba kaubavaru mobiilne tööruum aitab saada alati ja kõikjal mobiilseid ülevaateid reserveeritud ja vabadest kaubavarudest. 

<a name="prerequisites"></a>Eeltingimused
-------------

| Eeltingimus                                                         | Kirjeldus                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Lugege teavet Microsoft Dynamics 365 for Operationsi mobiiliplatvormi kohta | [Dynamics 365 for Operationsi mobiilne platvorm](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                   |
| Dynamics 365 for Operations                                          | Keskkond, millesse on installitud Microsoft Dynamics 365 for Operationsi versioon 1611 ja Microsoft Dynamics for Operationsi platvormivärskendus 3 (november 2016). |
| Kiirparanduse KB 3215650                                                    | Installige kiirparandus, et lubada rakenduses Microsoft Dynamics 365 for Operations sisestatud tööruumid.                                       |
| Mobiilne seade, kuhu on installitud rakendus Dynamics 365 for Operations | Laadige mobiilirakenduste poest alla rakendus Dynamics 365 for Operations.                                                                           |

## <a name="introduction"></a>Sissejuhatus
Tavaliselt on ettevõtetel iga päev mitu laosaadetist ja sissetulekut. Need liikumised muudavad pidevalt vaba kaubavaru olekut. Vaba kaubavaru mobiilne tööruum aitab näha ettevõtteülest vaba kaubavaru olekut, et saaksid enda valitud mobiilsel seadmel viimaseid ülevaateid varude andmetest. Olenemata sellest, kas töötate laos, ostu- või müügiosakonnas, tootmises või juhtkonnas või teil on teised rollid, pääsete vaba kaubavaru andmetele alati ja kõikjal juurde. Mobiilne tööruum annab viivitamatu ülevaate vaba kaubavaru olekust rajatiste lõikes ja võimaldab vaadata vaba kaubavaru erinevates rajatistes, praegusi materjali reserveeringuid ja reserveerimata vaba kaubavaru. Saate sisestada vaba kaubavaru päringute esitamiseks ka kaubakoode ja teha olemasolevate toodete ning variantide filtreeritud otsingut. Konkreetsemalt pakub mobiilne tööruum järgmisi funktsioone.

-   Saate otsida tootekoodi või tootenime järgi tooteid, mille vaba kaubavaru olekut on vaja vaadata.
-   Valitud toodete puhul saate vaadata järgmisi andmeid.
    -   Vaba kaubavaru laoala järgi
    -   Vaba kaubavaru lao järgi
    -   Vaba kaubavaru asukoha järgi
    -   Vaba kaubavaru partii järgi (partii kaudu juhitavate toodete puhul)
    -   Vaba kaubavaru varude oleku järgi

<!-- -->

-   Toodete vaba kaubavaru näidatakse järgmiselt.
    -   Füüsiliste varude järgi (see vaade kajastab kogu summat).
    -   Füüsiliste reserveeritud kaupade järgi (see vaade kajastab reserveeritud summat).
    -   Vabade füüsiliste varude järgi (see vaade kajastab vaba kogust, millel puuduvad reserveeringud).

## <a name="get-started"></a>Alusta
Mobiilsel seadmel alustamiseks tehke järgmist.

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

## <a name="view-the-onhand-inventory-for-a-product"></a>Toote vaba kaubavaru vaatamine
1.  Valige oma mobiilses seadmes tööruum **Vaba kaubavaru**.
2.  Valige **Kauba vaba kaubavaru kontrollimine**. Näete loendit toodetest, mis on laaditud teie rakendusse ühenduseta kasutamiseks. Vaikimisi on laaditud 50 kaupa, kuid saate seda arvu muuta. Lisateavet leiate eelnevaks lugemiseks mõeldud käsiraamatust.
3.  Kui teie kaupa pole loendis, valige **Otsi lisa**, et kasutada Dynamics 365 for Operationsis veebiotsingut. Otsige tootekoodi järgi või lülituge toote nime järgi otsimisse.
4.  Valige toode. Kui kaubal on pilt, siis kuvatakse see pilt.
5.  Tehke vaba kaubavaru oleku vaatamiseks üks järgmistest valikutest.
    -   Kuva vaba kaubavaru laoala järgi
    -   Kuva vaba kaubavaru lao järgi
    -   Kuva vaba kaubavaru asukoha järgi
    -   Kuva vaba kaubavaru partii järgi (partii kaudu juhitavate toodete puhul)
    -   Kuva vaba kaubavaru varude oleku järgi

    Toodete vaba kaubavaru näidatakse järgmiselt.
    -   Füüsiliste varude järgi (see vaade kajastab kogu summat).
    -   Füüsiliste reserveeritud kaupade järgi (see vaade kajastab reserveeritud summat).
    -   Vabade füüsiliste varude järgi (see vaade kajastab vaba kogust, millel puuduvad reserveeringud).




