---
title: Lao seadistamine
description: Selles teemas kirjeldatakse lao seadistamist, mida kasutatakse uue kanaliga Microsoft Dynamics 365 Commerce'is.
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
ms.openlocfilehash: 67c0bb169bee8a7ea90edb4db7233111a8ee6e34
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993649"
---
# <a name="warehouse-set-up"></a>Lao seadistamine


[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse lao seadistamist, mida kasutatakse uue kanaliga Microsoft Dynamics 365 Commerce'is.

## <a name="overview"></a>Ülevaade

Iga ärikanal nõuab, et sellega oleks seotud konfigureeritud ladu. Järgmised protseduurid annavad minimaalse konfiguratsiooni, mis on vajalik ärikanalile lao seadistamiseks. Lisainfot lao seadistamise kohta vaadake jaotisest [Laohalduse ülevaade](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).

## <a name="configure-a-warehouse-site"></a>Laoala konfigureerimine

Enne lao seadistamist peate konfigureerima laoala.

Laoala konfigureerimiseks toimige järgmiselt.

1. Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Saidid**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage väärtus väljale **Sait**.
1. Sisestage väärtus väljale **Nimi**.
1. Määrake jaotises **Üldine** sobiv **Ajavöönd**.
1. Sisestage aadress väljale **Aadressid**.
1. Valige toimingupaanil nupp **Salvesta**.

Järgmine pilt näitab laoala näidet.

![Laoala näide](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a>Lao seadistamine

Lao seadistamiseks toimige järgmiselt.

1. Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Laod**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage väärtus väljale **Ladu**.  Kui see on 1:1 vastendamine poega, kaaluge poe nime või piirkondliku jaotuskeskuse nime kasutamist.
1. Sisestage väärtus väljale **Nimi**.
1. Valige ripploendist **Sait** eelnevalt loodud laoala.
1. Valige väljal **Tüüp** väärtus **Vaikimisi**.
    - Kui soovite seadistada **Vahelao**, peate esmalt järgima neid samme, et luua täiendav ladu, kus **Tüüp** on seadistatud väärtusele **Vaheladu**.
    - Kui soovite seadistada **Transiitlao**, peate esmalt järgima neid samme, et luua täiendav ladu, kus **Tüüp** on seadistatud väärtusele **Transiit**.
1. Valige toimingupaanil nupp **Salvesta**.

## <a name="set-up-inventory-aisles"></a>Saate häälestada lao riiuliridu.

Riiuliridade seadistamiseks toimige järgmiselt.

1. Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Asukoha seadistus \> Riiuliread**.
1. Valige toimingupaanil nupp **Uus**.
1. Valige ripploendist **Ladu** eelnevalt loodud ladu.
1. Sisestage väljale **Riiulirida** nimi (nt "Vaik").
1. Sisestage väljale **Nimi** nimi (nt "Vaikimisi riiulirida").
1. Valige toimingupaanil nupp **Salvesta**.

## <a name="set-up-warehouse-inventory-locations"></a>Lao varude asukohtade häälestamine

Standardsete, kahjustatud ja tagastatud lao varude asukohtade seadistamiseks järgige neid samme.

1. Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Laod**.
1. Valige varem loodud ladu.
1. Valige tegevuspaanil nupp **Redigeeri**.
1. Valige tegevuspaanilt **Ladu** ja seejärel valige **Varude asukoht**.
1. Valige toimingupaanil nupp **Uus**. Ripploend **Ladu** peaks minema vaikimisi teie uude lattu.
    1. Sisestage kasti **Riiulirida** varem määratud riiulirea nimi. 
    1. Seadistage **Käsitsi värskendamine** väärtusele **Jah**
    1. Sisestage lao nimi kasti **Asukoht**.
    1. Valige toimingupaanil nupp **Salvesta**.
 1. Valige toimingupaanil nupp **Uus**.  Ripploend **Ladu** peaks minema vaikimisi teie uude lattu.
    1. Sisestage kasti **Riiulirida** varem määratud riiulirea nimi.  
    1. Seadistage **Käsitsi värskendamine** väärtusele **Jah**
    1. Sisestage "Kahjustatud" kasti **Asukoht**.
    1. Valige toimingupaanil nupp **Salvesta**.
 1. Valige toimingupaanil nupp **Uus**.  Ripploend **Ladu** peaks minema vaikimisi teie uude lattu.
    1. Sisestage kasti **Riiulirida** varem määratud riiulirea nimi. 
    1. Seadistage **Käsitsi värskendamine** väärtusele **Jah**
    1. Sisestage "Tagastused" kasti **Asukoht**.
    1. Valige toimingupaanil nupp **Salvesta**.
    
Järgmine pilt näitab San Francisco lao varude asukoha seadistust.

![Varude asukoha seadistuse näide](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a>Lao seadistamise lõpetamine

Lao seadistamise lõpetamiseks järgige järgmisi etappe.

1. Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Laod**.
1. Valige varem loodud ladu.
1. Valige tegevuspaanil nupp **Redigeeri**.
1. Jaotises **Varude ja laohaldus**.
    1. Seadistage **Vaikimisi vastuvõtu asukoht** eespool loodud asukohale.
    1. Valige **Vaikimisi väljastamise asukoht** eespool loodud asukohale.
1. Sisestage lao aadress jaotisesse **Aadressid**.
1. Jaotises **Jaemüük**. 
    1. Sisestage kasti **Vaikimisi tagastuste asukoht** eelnevalt loodud tagastuste asukoht.
    1. Sea **Kauplus** väärtusele **Jah**.
    1. Seadistage **Kaal** väärtusele **1.00**. 
    1. Sisestage kasti **Laoala dimensioonid** eelnevalt loodud vaikimisi asukoht.
1. Seadistage jaotises **Ladu** **Füüsilise negatiivse laovaru** väärtuseks **Jah**.
1. Valige toimingupaanil nupp **Salvesta**.

Järgmine pilt näitab konfigureeritud lao üksikasju.

![Konfigureeritud lao näide](media/warehouse-sample.png)

## <a name="additional-resources"></a>Lisaressursid

[Laohalduse ülevaade](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[Kanalite ülevaade](channels-overview.md)

[Kanali seadistamise eeltingimused](channels-prerequisites.md)

[Jaemüügikanali seadistamine](channel-setup-retail.md)
    
[Veebikanali häälestamine](channel-setup-online.md)

[Kõnekeskuse kanali seadistamine](channel-setup-callcenter.md)





