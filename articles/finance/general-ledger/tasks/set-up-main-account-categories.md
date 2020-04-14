---
title: Põhikonto kategooriate seadistamine
description: Selles teemas selgitatakse, kuidas seadistada põhikonto kategooriaid rakenduses Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e0a015283064af2287013bccc065b4467a308c5
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144785"
---
# <a name="set-up-main-account-categories"></a>Põhikonto kategooriate seadistamine

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse, kuidas seadistada põhikonto kategooriaid. Põhikonto kategooriaid kasutatakse vaikearuanneteks finantsaruandluses ja Power BI-s. Vaikimisi loodud põhikonto kategooriaid saab ümber nimetada, kuid mitte kustutada. Luua saab täiendavaid kontokategooriaid ning kasutada neid aruandluseks ja analüüsiks. Teemas kasutatakse demoettevõtet USMF.

## <a name="create-a-main-account-category"></a>Põhikonto kategooria loomine
1. Avage **Navigeerimispaan > Moodulid > Pearaamat > Kontoplaan > Kontod > Põhikontode kategooriad**.
2. Valige suvand **Uus**.
3. **Sisestage kordumatu nimi väljale Põhikonto kategooria.**
4. Sisestage väljale **Kirjeldus** põhikonto kategooria kirjeldus.
5. Valige väljal **Põhikonto tüüp** kategooriaga seotav põhikonto tüüp.

## <a name="link-main-accounts-to-account-category"></a>Põhikontode linkimine kontokategooriaga
1. Klõpsake suvandit **Põhikontode linkimine.**
2. Valige loendist põhikontod, mida põhikonto kategooriale määrata, kontrollides **lingitud** veeru välju. Põhikontode määramine põhikontode kategooriasse koondab kontode saldod, kui seda kategooriat kasutatakse finantsaruandluseks ja analüüsiks.  
3. Põhikontode valimiseks märkige või tühjendage suvand **Lingitud.**
4. Valige nupp **OK**.
5. Valige **Jah**.
