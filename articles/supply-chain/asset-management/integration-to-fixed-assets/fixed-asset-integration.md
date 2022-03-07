---
title: Varahalduse integreerimine põhivaradega
description: Selles teemas selgitatakse, kuidas integreerida varahaldus- ja põhivarade mooduleid, et saaksite ühendada põhivarad varahooldusega.
author: johanhoffmann
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 40e4fdce50b335668a53d2efe53b7cf6c66f364f
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567579"
---
# <a name="integrate-asset-management-with-fixed-assets"></a>Varahalduse integreerimine põhivaradega

[!include [banner](../../includes/banner.md)]

Kui integreerite moodulid **Varahaldus** ja **Põhivarad**, saate ühendada põhivarad varahooldusega. Põhivarade kasutajad saavad seejärel luua varahoolduse uue või olemasoleva põhivara põhjal ning varahalduse kasutajad saavad seostada varahoolduse olemasoleva põhivaraga. See funktsioon muudab ka põhivarade kasutajatel selliste kulude vaatamise lihtsamaks, mis sisestati töökäskude kaudu seotud varahoolduse tööde jaoks.

> [!NOTE]
> Selles teemas viitab termin *varahooldus* mooduli **Varahaldus** varadele ning termin *põhivarad* mooduli **Põhivarad** varadele.

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a>Põhivaradest loodud varahoolduse töö vaikeasukoha määramine (valikuline)

See valikuline konfiguratsioon lubab teil määrata põhivaradest loodud varahoolduse töö jaoks vaikeasukoha. Tavaliselt viite selle konfiguratsiooni lõpule ainult üks kord, kui üldse.

Konfiguratsiooni lõpetamiseks järgige järgmisi etappe.

1. Avage **Varahaldus \> Seadistus \> Varahalduse parameetrid**.
1. Valige vaikeasukoht vahekaardi **Põhivarad** väljal **Töö asukoht**.
1. Valige toimingupaanil nupp **Salvesta**.

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a>Integreeritud varahoolduse ja põhivaradega töötamine

Selles jaotises on toodud tegevuste kogum erinevatest viisidest, kuidas töötada integreeritud varahalduse ja põhivarade funktsioonidega.

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a>Olemasoleva varahoolduse seostamine põhivaraga

Olemasoleva varahoolduse seostamiseks põhivaraga toimige järgmiselt.

1. Valige **Varahaldus \> Varad \> Kõik varad** (või **Aktiivsed varad**).
1. Valige vara.
1. Valige kiirkaardi **Põhivara** väljal **Põhivara kood** olemasolev põhivara.
1. Valige toimingupaanil nupp **Salvesta**.

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a>Valitud varahooldusega seotud põhivara kuvamine

Valitud varahooldusega seotud põhivara kuvamiseks toimige järgmiselt.

1. Valige **Varahaldus \> Varad \> Kõik varad** (või **Aktiivsed varad**).
1. Valige vara.
1. Valige link kiirkaardi **Põhivara** väljal **Põhivara kood**.

    Avatakse leht **Põhivara** valitud vara jaoks. (Tavaliselt leiate selle lehe siit: **Põhivarad \> Põhivarad \> Põhivarad**.)

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a>Valitud põhivaraga seotud varahoolduse kuvamine

Valitud põhivaraga seotud varahoolduse kuvamiseks toimige järgmiselt.

1. Avage **Põhivarad \> Põhivarad \> Põhivarad**.
1. Valige vara.
1. Seejärel valige toimingupaanil vahekaardi **Varahaldus** grupis **Kuva** suvand **Varahooldus**.

    Avatakse valitud põhivaraga seotud vara **Varahoolduse** leht. (Tavaliselt leiate selle lehe siit: **Varahaldus \> Varad \> Kõik varad**.)

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a>Põhivaraga seotud hoolduskulude kuvamine

Varahoolduse jaoks saab sisestada varahalduse töökäske ja neil kõigil on tavaliselt kulu. Kui põhivara seostatakse varahooldusega, saate seotud kulusid vaadata otse põhivara kaudu.

Põhivaraga seotud hoolduskulude kuvamiseks toimige järgmiselt.

1. Avage **Põhivarad \> Põhivarad \> Põhivarad**.
1. Valige vara.
1. Seejärel valige toimingupaanil vahekaardi **Varahaldus** grupis **Kuva** suvand **Hoolduskulu**.

    Avatakse **Hoolduskulu** leht, millel kuvatakse seotud kulud.

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a>Olemasolevale põhivarale uue varahoolduse loomine

Olemasolevale põhivarale uue varahoolduse loomiseks toimige järgmiselt.

1. Avage **Põhivarad \> Põhivarad \> Põhivarad**.
1. Valige vara.
1. Seejärel valige toimingupaanil vahekaardi **Varahaldus** grupis **Uus** suvand **Loo varahooldus**. (Kui see valik ei ole saadaval, võib varahooldus juba valitud põhivaraga seotud olla.)
1. Lõpetage vara loomine, nagu kirjeldatud jaotises [Vara loomine](../objects/create-an-object.md).

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a>Uue põhivara loomine ja sellele uue varahoolduse lisamine

Uue põhivara loomiseks ja sellele uue varahoolduse lisamiseks toimige järgmiselt.

1. Avage **Põhivarad \> Põhivarad \> Põhivarad**.
1. Valige toimingupaanil nupp **Uus**.
1. Lõpetage põhivara loomine, nagu kirjeldatud jaotises [Põhivara loomine](../../../finance/fixed-assets/tasks/create-fixed-asset.md).
1. Seejärel valige toimingupaanil vahekaardi **Varahaldus** grupis **Uus** suvand **Loo varahooldus**.
1. Lõpetage vara loomine, nagu kirjeldatud jaotises [Vara loomine](../objects/create-an-object.md).

### <a name="remove-the-association-between-two-assets"></a>Seose eemaldamine kahe vara vahelt

Mõnel juhul peate eemaldama seose varahoolduse ja selle põhivara vahelt. Näiteks kui soovite [luua uue varahoolduse](#new-maintenance-from-fixed) põhivarast, peate esmalt eemaldama kõik olemasolevad seosed.

Olemasoleva seose eemaldamiseks varahoolduse ja põhivara vahelt toimige järgmiselt.

1. Valige **Varahaldus \> Varad \> Kõik varad** (või **Aktiivsed varad**).
1. Leidke ja avage põhivara.
1. Eemaldage kiirkaardil **Põhivara** välja **Töö asukoht** väärtus.
1. Valige toimingupaanil nupp **Salvesta**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]