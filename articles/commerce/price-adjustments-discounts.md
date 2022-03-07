---
title: Hinnakorrigeerimised ja allahindlused
description: Selles artiklis käsitletakse hinna korrigeerimisi ja allahindlusi Dynamics 365 Commerceis.
author: scott-tucker
ms.date: 06/11/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 96a695df250cda514b7bd8b9716c0f03fb2bfd28d3af4daedaf1335c3099fbb6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748494"
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

> [!NOTE]
> Segamise ja sobitamise allahindlusel ning läve allahindlusel on omadused, mille nimed on vastavalt "Mitteallahindlusega toodete loendamine" ja "Mitteallahindluskõlblike toodete loendamine künnise suunas". Kui need atribuudid on lubatud, võib kaup, mis ei vasta allahindluse saamise tingimustele, siiski aidata allahindlust kvalifitseeruda, kuid abikõlbmatu kaup ei saa allahindlust. 
> 
> Näiteks kui loote segamis- ja sobitamishinnaalandi kahe reaga A ja B, kus klient peaks saama mõlemalt kaubalt 10% allahindlust, kuid kaubal A on märgitud konfiguratsioon "Takista kõiki allahindlusi", siis tavaliselt peataks see kauba A kaasamise allahindlusesse. Kui aga atribuut "Loenda mitteallahindlusega tooteid" on lubatud, saab kaupa A kasutada segamise ja sobitamise allahindluse saamiseks, kuid 10% allahindlust rakendatakse ainult kaubale B. Sarnane loogika kehtib läve allahindluse kohta. 
>
> Kuid omadusel "Loenda mitteallahindlusega tooted künnise suunas" on täiendav võimalus võrreldes segu omadusega "Loe mitteallahindlusega tooteid" ja sobita allahindlused. Kui lävi hinnaaland on lubatud ja kui on olemas kaup, millel on olemasolev allahindlus, mis takistaks kaubal muid allahindlusi, siis kvalifitseeruks selle kauba eest makstud hind künnise saavutamisele, kuid see kaup ei saa täiendavat allahindlust.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
