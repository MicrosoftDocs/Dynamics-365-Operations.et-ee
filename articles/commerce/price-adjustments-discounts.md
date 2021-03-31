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
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d64632d7726fa5093bd04232790cae3f75938ae5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231219"
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]