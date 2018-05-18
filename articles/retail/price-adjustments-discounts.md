---
title: Hinnakorrigeerimised ja allahindlused
description: "Selles artiklis käsitletakse hinna korrigeerimisi ja allahindlusi Microsoft Dynamics 365 for Retailis."
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9220cc12abf7134d425e088939d20ea03239a75a
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="price-adjustments-and-discounts"></a>Hinnakorrigeerimised ja allahindlused

[!include [banner](includes/banner.md)]

Selles artiklis käsitletakse hinna korrigeerimisi ja allahindlusi Microsoft Dynamics 365 for Retailis.

Dynamics 365 for Retailis saate korrigeerida toodete hinda ja seadistada ka allahindlusi, mida rakendatakse kassas, kõnekeskuse müügitellimuses või võrgutellimuses reakaubale või kandele. Hinna korrigeerimisi ja allahindlusi saab siduda hinnagruppidega. Nii hinnakorrigeerimiste kui ka allahindluste puhul saate määrata ühe alguskuupäeva ja lõppkuupäeva või korduva perioodi, allahindluskoodi ja veel mõningaid atribuute. Hinna korrigeerimisi ja allahindlusi saab rakendada toodetele, variantidele või kategooriatele. Kui tootele rakendub rohkem kui üks allahindlus, võib klient saada ühe allahindlustest või kombineeritud allahindluse, olenevalt allahindluse konfiguratsioonist. Dynamics 365 for Retail rakendab automaatselt allahindluse või allahindluste kombinatsiooni, mis annab kliendile parima hinna. Hinna korrigeerimise või allahindluse seadistamisel kontrollige kindlasti, kas hinnagrupid on määratud õigetele kanalitele, kataloogidele, alluvustele või püsikliendiprogrammidele, millele soovite allahindluse rakendada. Ning kui soovite automaatselt allahindluse ID luua, saate enne uue hinna korrigeerimise või allahindluse määratlemist lehel **Jaemüügiparameetrid** seadistada numbriseeriad. **Märkus.** Saate hinna korrigeerimise või allahindluse kustutada. Statistiline teave läheb siiski kaduma.

### <a name="types-of-discounts"></a>Allahindluste tüübid

Jaemüügi allahindlusi on nelja tüüpi.

-   **Lihtne allahindlus** – üksik protsent või summa.
-   **Koguse allahindlus** – allahindlus, mis rakendub kahe või enama toote ostmisel.
-   **Segamise ja sobitamise allahindlus** – allahindlus, mis rakendub teatud tootekombinatsiooni ostmisel.
-   **Läve allahindlus** – allahindlus, mis rakendub, kui kande kogusumma on teatud summast suurem.

Nii hinna korrigeerimisi kui ka allahindlusi saab seostada hinnagruppidega. Seejärel saab hinnagruppe seostada kanalite, kataloogide, alluvuste ja püsikliendiprogrammidega.




