---
title: Kvaliteedijuhtimise testvahendid
description: See teema kirjeldab, kuidas luua testvahendeid, mida saab kasutada kvaliteettellimuste testidel Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
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
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 39624a9f00829e551fe3790a024155b6104318ef5cc1c582ab263c3868462063
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774098"
---
# <a name="quality-management-test-instruments"></a>Kvaliteedijuhtimise testvahendid

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas luua testvahendeid, mida saab kasutada kvaliteettellimuste testidel Microsoft Dynamics 365 Supply Chain Management.

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
