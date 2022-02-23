---
title: Hinnakorrigeerimised ja allahindlused
description: Selles artiklis käsitletakse hinna korrigeerimisi ja allahindlusi Dynamics 365 Commerceis.
author: scott-tucker
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0c2adaa5cd935d5b593bfbb3215d3466fcafab7b
ms.sourcegitcommit: 1d74636bf9db5fb33e998322899504b709b4f89f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/19/2020
ms.locfileid: "4584311"
---
# <a name="price-adjustments-and-discounts"></a>Hinnakorrigeerimised ja allahindlused

[!include [banner](includes/banner.md)]

Selles artiklis käsitletakse hinna korrigeerimisi ja allahindlusi Dynamics 365 Commerceis.

Rakenduses Commerce saate korrigeerida toodete hindu ja seadistada allahindlusi, mida rakendatakse kassas, kõnekeskuse müügitellimuses või võrgutellimuses rea kaubale või kandele. Hinna korrigeerimisi ja allahindlusi saab siduda hinnagruppidega. Nii hinnakorrigeerimiste kui ka allahindluste puhul saate määrata ühe alguskuupäeva ja lõppkuupäeva või korduva perioodi, allahindluskoodi ja veel mõningaid atribuute. 

Hinna korrigeerimisi ja allahindlusi saab rakendada toodetele, variantidele või kategooriatele. Kui tootele rakendub rohkem kui üks allahindlus, võib klient saada ühe allahindlustest või kombineeritud allahindluse, olenevalt allahindluse konfiguratsioonist. Commerce rakendab automaatselt allahindluse või allahindluste kombinatsiooni, mis annab kliendile parima hinna. Hinna korrigeerimise või allahindluse seadistamisel kontrollige kindlasti, kas hinnagrupid on määratud õigetele kanalitele, kataloogidele, alluvustele või püsikliendiprogrammidele, millele soovite allahindluse rakendada. Ning kui soovite automaatselt allahindluse ID luua, saate enne uue hinna korrigeerimise või allahindluse määratlemist lehel **Kaubanduse parameetrid** seadistada numbriseeriad.

> [!NOTE]
> Saate hinna korrigeerimist või allahindlust kustutada. Statistiline teave läheb siiski kaduma.

## <a name="types-of-discounts"></a>Allahindluste tüübid

Allahindlusi on mitut tüüpi.

- **Lihtne allahindlus** – üksik protsent või summa.
- **Koguse allahindlus** – allahindlus, mis rakendub kahe või enama toote ostmisel.
- **Segamise ja sobitamise allahindlus** – allahindlus, mis rakendub teatud tootekombinatsiooni ostmisel.
- **Läve allahindlus** – allahindlus, mis rakendub, kui kande kogusumma on teatud summast suurem.
- **Maksevahendil põhinev allahindlus** – allahindlus, mis rakendub, kui kande kogusumma on suurem kui määratud summa ja makse puhul kasutatakse kindlat maksetüüpi (nt sularaha, krediit- või deebetkaarti).
- **Saatmise allahindlus** – allahindlus, mis rakendub, kui kande kogusumma on suurem kui määratud summa ja tellimusel kasutatakse kindlat tarneviisi (nt kahepäevane saatmine või öine saatmine).

Nii hinna korrigeerimisi kui ka allahindlusi saab seostada hinnagruppidega. Seejärel saab hinnagruppe seostada kanalite, kataloogide, alluvuste ja püsikliendiprogrammidega.
