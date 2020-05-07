---
title: Kuluarvestuse teenuse kasutamise alustamine
description: See teema hõlmab kuluarvestuse teenuse litsentsi üksikasju ja installijuhiseid.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: cbbce7eaac264973bf0b95ad5175bf70ed2b4ae9
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276908"
---
# <a name="get-started-with-the-cost-accounting-service"></a>Kuluarvestuse teenuse kasutamise alustamine

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> Selles teemas kirjeldatud funktsioon on saadaval privaatsete eelväljaannete osana. Teema sisu ja selles kirjeldatav funktsioon võivad muutuda. Lisateavet eelväljaannete kohta vt teemast [Ühe versiooni teenuse värskenduste KKK](../../fin-ops-core/fin-ops/get-started/one-version.md).

Kuluarvestuse teenus võimaldab teil teha mitut laoarvestust teie seadistatud kuluarvestuse pearaamatutes. Te seostate iga kuluarvestuse pearaamatu *reegliga*. Reegel on järgmist tüüpi raamatupidamispoliitikate kogumik.

- Kuluobjekt
- Sisendi mõõtmise alus
- Kuluvoo eeldus
- Kuluelement

> [!NOTE]
> Isegi kui olete kuluarvestuse teenuse sisse lülitanud, saate jätkuvalt samamoodi Microsoft Dynamics 365 Supply Chain Managementis laoarvestust teha.

Kuluarvestuse teenus on lisandmoodul. Selle funktsioonide kättesaadavaks tegemiseks peate selle installima teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu. Seejärel saate valida, kas hinnata seda testimiskeskkonnas enne selle sisselülitamist töökeskkondades.

Kuluarvestuse teenus ei toeta praegu kõiki kulude haldamise funktsioone, mida Dynamics 365 Supply Chain Management hõlmab. Seega on oluline, et hindaksite, kas hetkel saadaolev funktsioonide komplekt vastab teie nõuetele.

## <a name="licensing"></a>Litsentsimine

Kuluarvestuse teenus litsentsitakse koos standardsete laoarvestuse funktsioonidega, mis on saadaval teenuse Supply Chain Management jaoks. Te ei pea kuluarvestuse teenuse kasutamiseks ostma täiendavat litsentsi.

## <a name="install-the-add-in"></a>Lisandmooduli installimine

> [!IMPORTANT]
> Kuluarvestuse teenuse kasutamiseks peab teil olema LCS-i toega suure kättesaadavusega keskkond (mitte OneBoxi keskkond) ning Dynamics 365 Supply Chain Managementi versioon 10.0.11 või uuem.

Kuluarvestuse teenuse kasutamiseks installige kuluarvestuse teenuse lisandmoodul teenuse Supply Chain Management jaoks, nagu kirjeldatakse järgmises toimingus.

1. Logige teenusesse LCS sisse.

1. Avage suvand **Eelvaate funktsiooni haldamine**.

1. Valige plussmärk (**+**).

1. Sisestage väljale **Kood** kuluarvestuse teenuse lisandmooduli beetavõti. (Võti saadeti teile e-posti teel.)

1. Valige **Tühista blokeerimine**.

1. Avage LCS-i keskkond, kuhu soovite teenuse lisada.

1. Avage **Kõik üksikasjad**.

1. Kerige alla kiirkaardini **Keskkonna lisandmoodulid**.

1. Valige **Installi uus lisandmoodul**.

1. Valige **Kuluarvestuse teenus**.

1. Täitke paigaldusjuhendit ja nõustuge nõuete ja tingimustega.

1. Valige **Installi**.

1. Peaksite nägema kiirkaardil **Keskkonna lisandmoodulid**, et kuluarvestuse teenust installitakse. Mõne minuti pärast peaks olek **Installimine** muutuma olekuks **Installitud**. (Selle muudatuse nägemiseks võib olla vaja lehte värskendada.) Pärast seda on kuluarvestuse teenus kasutamiseks valmis.

## <a name="set-up-the-integration"></a>Integratsiooni seadistamine

Kuluarvestuse teenuse ja Dynamics 365 Supply Chain Managementi vahel integratsiooni seadistamiseks tehke järgmist.

1. Avage **Süsteemihaldus > Funktsioonihaldus**.

1. Valige **Otsi värskendusi**.

1. Avage vahekaart **Kõik** ja otsige funktsiooni nimega *Kuluarvestuse teenus*.

1. Valige **Luba kohe**.

1. Avage **Kuluhaldus > Kuluarvestuse teenus > Seadistamine > Kuluarvestuse teenuse parameetrid > Integratsiooni parameetrid**.

1. Sisestage väljale **Avalduse ID** järgmine kood:<br> 08231eb2-a501-4edb-b3c5-aede5e5e0c3f

1. Sisestage väljale **Andmeteenuse lõpp-punkt** järgmine URL:<br>https://operationsdataservice.operations365.dynamics.com/

1. Sisestage väljale **Kuluarvestuse teenuse lõpp-punkt** järgmine URL:<br>https://costaccountingservice.operations365.dynamics.com/

1. Kuluarvestuse teenus on nüüd kasutamiseks valmis.

## <a name="related-resources"></a>Seotud ressursid

[Kuluarvestuse teenuse avaleht](cost-accounting-service-home.md)
