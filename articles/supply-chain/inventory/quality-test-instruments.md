---
title: Kvaliteedijuhtimise testvahendid
description: See artikkel kirjeldab, kuidas luua katsevahendeid, mida saab kasutada Microsofti kvaliteettellimuste katseteks Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 36b712e6a99a0625af28ef121d0c9c39c1e32603
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857659"
---
# <a name="quality-management-test-instruments"></a>Kvaliteedijuhtimise testvahendid

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas luua katsevahendeid, mida saab kasutada Microsofti kvaliteettellimuste katseteks Dynamics 365 Supply Chain Management.

Kasutate **Testvahendite** lehte, et määrata ja vaadata üksikasju seadmete kohta, mida kasutatakse kvaliteettellimustel testide sooritamiseks. Testvahendid on valikulised. Kuid need võivad aidata kvaliteeditöötajatel teada, millist seadet või tööriista nad peaksid konkreetse testi tegemiseks kasutama.

## <a name="test-instrument-example"></a>Testvahendi näide

Teete mitmesuguseid elektrikomponentide teste. Mõned testid on mõeldud komponentide väljundpingele, üks test nende temperatuurile ja üks test nende kaalu jaoks. Iga testi tegemiseks kasutatakse erinevaid tööriistu, seadmeid või varustust. Näiteks kasutatakse pinge mõõtmiseks pingemõõturit, temperatuuri mõõtmiseks termomeetrit ja kaalu mõõtmiseks kaalu. Kõiki neid seadmeid saate seadistada testimisinstrumentidena ja märkida mõõtühik, milles testitulemused tuleks salvestada. Näiteks registreeritakse pingemõõturi tulemused voltides, termomeetri tulemused registreeritakse Fahrenheiti või Celsiuse skaalal kraadides ning kaalumise tulemused registreeritakse naela või kilogrammina.

## <a name="create-a-test-instrument"></a>Testvahendi loomine

1. Avage **Varude haldus \> Seaded \> Kvaliteedijuhtimine \> Testvahendid**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida. Seejärel määrake uuel real järgmised väljad.

    - **Testvahendid** – Sisestage testvahendi kordumatu ID või nimi.
    - **Kirjeldus** – Sisestage testvahendi detailne kirjeldus.
    - **Ühik** – Valige mõõtühik, milles seade tulemuse annab. **Täpsus** väli seatakse automaatselt valitud ühiku põhjal.

1. Sulgege leht.

## <a name="additional-resources"></a>Lisaressursid

- [Kvaliteedijuhtimise test](quality-tests.md)
- [Kvaliteedijuhtimise testgrupid](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
