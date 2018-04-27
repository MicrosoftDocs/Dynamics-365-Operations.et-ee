---
title: "Teenuse Microsoft Dynamics 365 for Talent võimaluste laiendamine"
description: "Kui olete loonud Microsoft PowerAppse, saate need rakendused käivitada teenuses Microsoft Dynamics 365 for Talent olevate linkide kaudu."
author: rschloma
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 51eb4288f5b6c732755007c1dcd8c4db090ccc0a
ms.contentlocale: et-ee
ms.lasthandoff: 03/07/2018

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a>Teenuse Microsoft Dynamics 365 for Talent võimaluste laiendamine

[!INCLUDE [banner](includes/banner.md)]

Kui olete loonud Microsoft PowerAppse, saate need rakendused käivitada teenuses Microsoft Dynamics 365 for Talent olevate linkide kaudu. Rakendustele juurdepääsu seadistamiseks peate teenuses Talent konfiguratsiooni lehel seadistama teavet, konfiguratsiooni lehe saate avada tööruumis **Süsteemihaldus**.

## <a name="configuring-embedded-powerapps-within-talent"></a>Manustatud PowerAppsi konfigureerimine teenuses Talent
Kasutage lehte **Manustatud Microsoft PowerAppsi seadistamine**, et konfigureerida teenuse Talent lehed käivitama PowerAppsi rakendusi. Lehe **Manustatud Microsoft PowerAppsi seadistamine** avamiseks avage tööruum **Süsteemihaldus** ja seejärel avage vahekaart **Lingid**. Valige **Microsoft PowerApps** grupist **Seadistamine**. 

Sellel lehel saab sisestada või seadistada järgmist teavet. 

 -  Iga PowerAppsi rakenduse kirjeldav nimi või identifikaator.
 -  Kordumatu ID (GUID) iga rakenduse jaoks, mille lisate teenuse Talent lehel. Rakenduse ID on saadaval PowerAppsi saidil [powerapps.com](http://powerapps.com/). 
 -  Leht, millelt kasutajad saavad avada rakendust või aruannet. Mõned teenuse Talent lehed ei toeta manustatud PowerAppsi ja Power BI aruandeid. 

 > [!NOTE]
 >  Sisestage lehe sisemine nimi, mitte lehe ülaosas olev kuvatav nimi. Sisemise nime leidmiseks avage leht, mille sisemist nime te vajate ja paremklõpsake lehel mis tahes kohas. Menüü avanemisel liikuge üksuse **Vormi teave** kohale. Sisemise vormi nimi kuvatakse menüüs üksuse **Vormi teave** kõrval.
 
-   Määrake vormi juhtelement, millelt rakendus saab hankida konteksti andmeid. Näiteks võib rakendus kasutada andmeid töötaja kohta. Kui sisestate väljal **Kontekst** lehe **Töötaja**, avaneb leht **Töötaja** rakenduse käivitamisel. Kirje valikus **Kontekstiväli** on valikuline. 
-   Määrake dialoogiboksi suurus, milles PowerAppsi rakendus edaspidi töötab. Dialoogiboksid on määratud kui „väikesed” või „suured”, et optimeerida kasutajaliidest, kui teie rakendus töötab vastavalt telefonis või suuremas seadmes. 


Samuti saate määrata, milliste juriidiliste isikute jaoks on rakendus saadaval, või saate selle kõigile oma juriidilistele isikutele kättesaadavaks teha. Vaikimisi on teie PowerAppsi rakendused saadaval kõigile juriidilistele isikutele.

## <a name="opening-an-application"></a>Rakenduse avamine
Kui olete konfigureerinud manustatud PowerAppsi rakendused, lisatakse teie määratud rakenduste lingid teenuses Talent olevatele lehtedele. Rakenduse avamiseks klõpsake linki. 



