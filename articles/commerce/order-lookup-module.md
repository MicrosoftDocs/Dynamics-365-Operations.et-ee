---
title: Tellimuse otsingu moodul
description: See artikkel katab tellimuse otsingumooduli ja selgitab selle konfigureerimist moodulis Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 8c60ed0c334bf09916dd633302c6d813ea6f16b6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281450"
---
# <a name="order-lookup-module"></a>Tellimuse otsingu moodul

[!include [banner](includes/banner.md)]

See artikkel katab tellimuse otsingumooduli ja selgitab selle konfigureerimist moodulis Microsoft Dynamics 365 Commerce.

Tellimuse otsingumoodul annab vormi, mille abil kliendid saavad otsida tellimusi, mis nad e-kaubanduse saidile paigutasid. Seda kasutatakse osana [Luba tellimuse otsing külalise väljaregistreerimise](order-lookup-guest.md) funktsioonist. Tellimuse otsingumoodulit saab kasutada tellimuste otsimiseks, mis esitati e-kaubanduse saidi, müügikoha (POS) või kõnekeskuse kaudu. Vorm saab tuua tellimusi, mille on esitanud nii külaliskasutajad kui ka registreeritud kasutajad.

Järgmine näide näitab tellimuse otsingumooduli renderdatud vormi näidet. Kui kliendid täidab vormi ja valite käsu **Otsi tellimust**, suunatakse need ümber tellimuse üksikasjade lehele.

![Tellimuse otsingumooduli vorm lehel.](./media/OrderLookup_module.PNG)

## <a name="order-lookup-module-properties"></a>Tellimuse otsingu mooduli atribuudid

| Atribuudi nimi     | Väärtus     | Kirjeldus |
|-------------------|-----------|-------------|
| Päis           | Tekst      | Vormi ülaosas kuvatav pealkiri (nt "Otsi oma tellimust"). |
| Rikastekst         | Rikastekst | Pealkirja all kuvatav valikuline selgitav tekst. |
| Tellimuse oleku tüüp | Loend      | <p>Valige teabe tüüp, mida vorm kliendilt lisaks tellimuse kinnituse ID-le taotleb. Praegu toetatakse järgmisi väärtusi:</p><ul><li><b>E-post</b> - Vorm sisaldab välja, kus kliendid saavad sisestada meiliaadressi, mida nad tellimuse sisestamisel kasutavad.</li><li><b>Pole</b> – Vorm ei taotle lisaks tellimuse kinnituse ID-le teavet.</li></ul> |

## <a name="add-an-order-lookup-module-to-a-page"></a>Lehele tellimuse otsingu mooduli lisamine

Tellimuse otsingumooduli saab lisada mis tahes e-kaubanduse saidi kehale. Kui soovite kasutada tellimuste otsingumoodulit, et lubada tellimuste otsingut külalise väljaregistreerimiseks, lisage see kindlasti lehele, mis ei nõua kasutaja sisselogimist. Lehekülje **Sisselogimise vajadus?** seadete leidmiseks Commerce'i saidi koostaja puuvaates valige **vaikelehe (Nõutav)** pesa ja vaadake paremal paanil lehe allossa.

## <a name="additional-resources"></a>Lisaressursid

[Tellimuse otsingu lubamine külaliste väljaregistreerimiseks](order-lookup-guest.md)

[Mooduliteegi ülevaade](starter-kit-overview.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
