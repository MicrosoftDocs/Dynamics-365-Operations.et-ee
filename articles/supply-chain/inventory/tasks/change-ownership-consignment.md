---
title: Kaubavaru omandiõiguse muutmine tootmise nõudluse põhjal
description: See protseduur näitab, kuidas määrata saadetise varude omanikuks hankija asemel teie juriidiline isik, kui on olemas nõudlus tootmises olevate varude järele.
author: yufeihuang
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e735a9003f2859ed173f399525297506ec458e8d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565827"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a>Kaubavaru omandiõiguse muutmine tootmise nõudluse põhjal

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas määrata saadetise varude omanikuks hankija asemel teie juriidiline isik, kui on olemas nõudlus tootmises olevate varude järele. See omandiõiguse muutmine toimub varude omandiõiguse muutmise töölehe sisestamisega. Omandiõiguse muutmise töölehe ridu saab luua käsitsi või (nagu selles salvestises näidatud) olemasoleva tootmise nõudluse põhjal. Tavaliselt teeb seda tööde järelevaataja. Saate seda protseduuri kasutada demoettevõttes USMF või oma andmeid kasutades. Kui kasutate oma andmeid, siis veenduge, et teil oleksid olemas järgmised eeltingimused: varude töölehe nimi, mis on seadistatud varude omandiõiguse muutmiseks, füüsiliselt registreeritud hankijale kuuluvad vabad kaubad ja vähemalt üks materjali tootmistellimuse rida. See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.

> [!NOTE]
> Väljaminevate saadetiste protsesse ei toetata valmiskujul ja automaatset omandiõiguse päeviku töötlemist ei toetata.

## <a name="create-an-inventory-ownership-journal"></a>Varude omanikuvahetuse töölehe loomine
1. Minge jaotisse Varud > Töölehe sisestused > Kaubad > Varude omanikuvahetus.
2. Klõpsake valikut Uus.
    * Varude omanikuvahetuse töölehe kaudu määratakse saadetise varude omanikuks hankija asemel praegune juriidiline isik. Omanikuvahetuseks vabastatakse hankijale kuuluv vaba kaubavaru ja vormistatakse siis selle varu sissetulek praeguses juriidilises isikus.  
3. Sisestage või valige väärtus väljal Nimi.
    * Saate valida ainult neid laotöölehtede nimesid, mille töölehe tüüp on Omanikuvahetus.  
4. Klõpsake nuppu OK.
5. Klõpsake suvandit Funktsioonid.
6. Klõpsake valikut Tootmistellimustest töölehe ridade loomine.
    * Saate alustada omanikuvahetuse protsessi, esitades päringu kõigi tootmise ridade kohta, millel on tooraine tarbimise nõue.  
7. Tehke valik väljal Kaasatavad lao väljamineku olekud.
    * See valik võimaldab filtreerida laokannete väljastamisoleku järgi. Näiteks saate luua töölehe read varudele, mille füüsilised olekud on Komplekteeritud ja Reserveeritud.  
8. Jaotise kaasamiseks laiendage kirjeid.
    * Selles jaotises saate rakendada täiendavat filtreerimist. Näiteks saate valida kindla toormaterjali kuupäeva.  
9. Klõpsake nuppu OK.

## <a name="post-the-inventory-ownership-change-journal"></a>Varude omanikuvahetuse töölehe sisestamine
1. Klõpsake valikut Sisesta.
    * Töölehe sisestamisel vabastatakse hankijale kuuluvad varud, kasutades viidet Omanikuvahetus. Seejärel saadakse varud vabade varudena, kasutades laokannet, mida uuendatakse ostutellimuse toote sissetulekuga. Pange tähele, et luuakse ainult sisestatud töölehega seotud kanded. Ühtegi eeldatavat laokannet ei looda.  
2. Klõpsake nuppu OK.
3. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]