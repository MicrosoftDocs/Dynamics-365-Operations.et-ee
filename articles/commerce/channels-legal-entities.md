---
title: Juriidiliste isikute loomine
description: See teema kirjeldab, kuidas luua Microsoft Dynamics 365 Commerce'is juriidilisi isikuid, mis tulevad enne kanalite loomist luua ja konfigureerida.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 016b67631a53139d12d65dfaf594f49b030326b1
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478208"
---
# <a name="create-legal-entities"></a>Juriidiliste isikute loomine

[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas luua Microsoft Dynamics 365 Commerce'is juriidilisi isikuid, mis tulevad enne kanalite loomist luua ja konfigureerida.

Juriidiline isik on registreeritud või õigusliku struktuuriga organisatsioon. Juriidilised isikud võivad sõlmida juriidilisi lepinguid ja on kohustatud koostama oma tegevuse kohta aruandeid.

Ettevõte on juriidiline isik. Ettevõtted on praegu ainsad juriidilised isikud, mida saate luua, ja iga juriidiline isik on seostatud ettevõtte ID-ga. See seos on olemas, kuna mõni programmi funktsioonivaldkond kasutab oma andmemudelis ettevõtte ID-d või atribuuti *DataAreaId*. Neis funktsioonivaldkondades kasutatakse ettevõtteid andmeturbe piirina. Kasutajad pääsevad juurde ainult selle ettevõtte andmetele, millesse nad parasjagu sisse on loginud. 

Kanali loomisel peate määrama, millise juriidilise isiku juurde kanal kuulub.

## <a name="create-a-new-legal-entity"></a>Uue juriidilise isiku loomine

Uue juriidilise isiku loomiseks Dynamics 365 Commerce'is toimige järgmiselt.

1. Avage navigatsioonipaneelil **Moodulid \> Peakontori seadistus \> Juriidilised isikud**.
1. Valige toimingupaanil nupp **Uus**. Paan **Uus juriidiline isik** kuvatakse paremal.
1. Sisestage väärtus väljale **Nimi**.
1. Sisestage väärtus väljale **Ettevõte**.
1. Sisestage või valige väärtus väljale **Riik/regioon**.
1. Valige nupp **OK**. 

   ![Juriidilise isiku loomine](media/legal-entities.png)

1. Esitage jaotises **Üldine** juriidilise isiku kohta järgmised üldandmed. 
   1. Sisestage otsingunimi, kui otsingunimi on nõutav. Otsingunimi on alternatiivne nimi, mida saab kasutada selle juriidilise isiku otsimiseks. 
   1. Valige, kas seda juriidilist isikut kasutatakse konsolideeritud ettevõttena.
   1. Valige, kas seda juriidilist isikut kasutatakse elimineerimise ettevõttena. 
   1. Valige üksusele **vaikekeel**. 
   1. Valige üksusele **ajavöönd**.
1. Tehke jaotises **Aadressid** valik **Muuda**, et sisestada aadressiteave, nagu tänavanimi, majanumber, sihtnumber ja linn.
1. Jaotisse **Kontaktteave** sisestage teave selliste sidepidamise viiside kohta nagu meiliaadressid, URL-id ja telefoninumbrid.
1. Sisestgae jaotisse **Seaduslik aruandlus** registreerimisnumbrid, mida kasutatakse seadusandlikuks aruandluseks.
1. Sisestage jaotisse **Registreerimisnumbrid** mis tahes teave, mis on juriidilise isiku puhul nõutav.
1. Sisestage jaotisse **Pangakonto teave** juriidilise isiku pangakontod ja registreerimisnumbrid.
1. Sisestage jaotisesse **Väliskaubandus ja logistika** tarneteave juriidilise isiku kohta.
1. Jaotises **Numbriseeriad** saate vaadata numbriseeriaid, mis on seostatud juriidilise isikuga. Alguses on see tühi.
1. Jaotises **Armatuurlaua pilt** saate vaadata või muuta logo ja armatuurlaua pilti, mis on seostatud juriidilise isikuga.
1. Sisestage jaotisesse **Maksu registreerimine** registreerimisnumbrid, mida kasutatakse maksuhalduritele teatamiseks.
1. Sisestage jaotises **Maks 1099** juriidilisele isikule teave 1099.
1. Sisestage jaotisesse **Maksuteave** juriidilise isiku maksuteave.
1. Valige käsk **Salvesta**.

Järgmine pilt näitab näitliku juriidilise isiku üksikasju.

![Juriidilise isiku üldine jaotis](media/legal-entities-general.png)
   
## <a name="additional-resources"></a>Lisaressursid

[Organisatsioonide ja organisatsioonihierarhiate ülevaade](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Organisatsioonihierarhia kavandamine](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Organisatsiooni hierarhiad](channels-org-hierarchies.md)

[Kanalite ülevaade](channels-overview.md)

[Kanali seadistamise eeltingimused](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
