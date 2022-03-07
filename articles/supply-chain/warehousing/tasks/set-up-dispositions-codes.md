---
title: Likvideerimiskoodide seadistamine
description: See protseduur keskendub likvideerimiaskoosdi loomisele, mida saab kasutada mobiilses seadmes tagastustellimuse vastuvõtmisprotsessi puhul.
author: Mirzaab
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSDispositionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb83108c934e864da0df39ec4ee36a0bc7ba7588
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574061"
---
# <a name="set-up-dispositions-codes"></a>Likvideerimiskoodide seadistamine

[!include [banner](../../includes/banner.md)]

See protseduur keskendub likvideerimiaskoosdi loomisele, mida saab kasutada mobiilses seadmes tagastustellimuse vastuvõtmisprotsessi puhul. Likvideerimiskoodid on kogumik reegleid, mida saab kasutada kaupade vastuvõtmisel. Näiteks kui töö kasutaja kasutab kahjustatud kaupade vastuvõtmiseks mobiilset seadet, peab ta skannima kahjustatud kaupade likvideerimiskoodi. Vastuvõetud kaupade varude oleku, töömalli ja asukohakorralduse saab määratleda skannitud likvideerimiskoodi alusel. Ostutellimuse vastuvõtmisprotsessi ja tootmisetellimuse lõpetatuna teatamisel on likvideerimiskoodi kasutamine valikuline. Kui müügitellimuse tagastuse vastuvõtmisprotsessi puhul registreeritakse kaubad mobiilse seadme abil, on likvideerimiskoodi kasutamine kohustuslik.  Selle juhendi loomisel kasutati demoettevõtte USMF andmeid. See protseduur on mõeldud laohaldurile. 

1. Tehke valik Laohaldus > Seadistus > Mobiilne seade > Likvideerimiskoodid.
2. Klõpsake valikut Uus.
    * Saate luua kliendi tagastuste puhul kasutamiseks uue likvideerimiskoodi.  
3. Sisestage väärtus väljale Likvideerimiskood.
4. Valige väljal Varude olek see varude olek, kus esineb varude blokeerimine.
    * USMF-i kasutamisel valige suvand Blokeerimine. Saate lisada varude olekule likvideerimiskoodi, et tühistada selle vaikeolek tellimuseridadel.  
5. Sisestage väärtus väljale Töömall.
    * Valikuline: saate valida tagastustellimusega seostatud töömalli koodi. Kui ühtegi väärtust pole esitatud, lahendatakse töömall teie süsteemis konfigureeritud standardreeglitega. Töömalli valimine piirab protsesse, millega seda likvideerimiskoodi saab kasutada. Näiteks kui likvideerimiskoodil on töömall, mille töötellimuse olek on Ostutellimus, ei saa seda kasutada klientide tagastatud kaupade registreerimiseks.  
6. Sisestage väärtus väljale Tagastamise likvideerimiskood.
    * Tagastuse likvideerimiskood määratleb ülejäänud tagastustellimuse protsessi registreeritud kaupade puhul. Selles näites peaks klient saama kreeditarve. Lisage tagastuste likvideerimiskood, mis sisaldab tegevust Kreedit.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]