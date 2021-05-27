---
title: Kvaliteedijuhtimise testi muutujad
description: See teema kirjeldab, kuidas luua testi muutujaid, mida saab kasutada kvaliteettellimuste testidel Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5102d09f5762a390d6fd3aadafcb2ed23820982
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021704"
---
# <a name="quality-management-test-variables"></a>Kvaliteedijuhtimise testi muutujad

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas luua testi muutujaid, mida saab kasutada kvaliteettellimuste testidel Microsoft Dynamics 365 Supply Chain Management.

Peate määrama muutuja ja tema väljundid iga kvalitatiivse katse jaoks, mis on määratud lehel **Testid**. (Kvalitatiivsete testide puhul on **Tüüp** väljal lehel **Testid** määratud *Suvand*.)

Kvalitatiivse testiga seotud testmuutuja võimalike tulemuste seadistamiseks, muutmiseks ja vaatamiseks kasutage lehte **Testi muutujad**. Iga tulemuse jaoks määrate te väljundolekuks *Läbitud* või *Nurjunud*, mis näitab, kas test on läbitud või nurjunud, kui see tulemus on testi tulemusena valitud. Kasutage lehte **Testgrupid** katsemuutuja ja vaikeväärtuse määramiseks kindlale kvalitatiivse katse väljundile.

Iga testmuutuja jaoks soovitame määratleda vähemalt kaks tulemust: ühe, mille väljundolek on *Läbitud* ja teine, mille väljundolek on *Nurjunud*. Muutujate ja väljundite koguarvu, mida saab määratleda, ei ole piiratud. Lisaks võivad mitmed testid tulemuste registreerimiseks kasutada samu testimuutujaid.

## <a name="examples-of-test-variables"></a>Testmuutujate näited

### <a name="example-1"></a>Näide 1

Tootmisettevõte sooritab kaks katset toodetud materjalidega. Ühes testis seostatakse pH-tase värviribaga. Vastuvõetav pH-tase on heledamates värvides ja vastuvõetamatud pH-tasemed on tumedates värvides. Teises testis viiakse läbi mitu visuaalset kontrolli ja kvaliteettöötajad kasutavad oma hinnangut, et teha kindlaks, kas kaup läbib või nurjub visuaalse kontrolli.

### <a name="example-2"></a>Näide 2

Küpsiseid valmistav tootmisettevõte kasutab valmistoote kontrollkatset. Sellel kontrollkatsel on mitu muutujat. Üks muutuja on maitse ja selle muutuja võimalikud väärtused on hea ja halb. Teine muutuja on värvus ja võimalikud tulemused on liiga tume, liiga hele ja õige.

## <a name="create-a-test-variable"></a>Uue testmuutuja loomine

Testmuutuja loomiseks toimige järgmiselt.

1. Avage **Varude haldus \> Seaded \> Kvaliteedijuhtimine \> Testmuutujad**.
1. Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida. Seejärel määrake uuel real järgmised väljad.

    - **Muutuja** – Sisestage muutuja kordumatu ID või nimi.
    - **Kirjeldus** – Sisestage muutuja detailne kirjeldus.

1. Kui uus rida on endiselt valitud, valige tegevuspaanil **Väljundid**.
1. Ruudustiku rea lisamiseks valige **Testmuutujate väljundid** lehe tegevuspaanil suvand **Uus**. Seejärel määrake uuel real järgmised väljad.

    - **Väljund** – Sisestage väljundi kordumatu ID või nimi.
    - **Kirjeldus** – Sisestage väljundi detailne kirjeldus.
    - **Väljundi olek** – Iga tulemuse jaoks määrate te väljundolekuks *Läbitud* või *Nurjunud*, mis näitab, kas test on läbitud või nurjunud, kui see tulemus on testi tulemusena valitud.

1. Korrake eelmist sammu iga täiendava väljundi puhul. Veenduge, et vähemalt ühel väljundil on väljundolek *Läbitud* ja vähemalt ühel on väljundolek *Nurjunud*.
1. Sulgege lehed.

## <a name="additional-resources"></a>Lisaressursid

- [Kvaliteedijuhtimise testvahendid](quality-test-instruments.md)
- [Kvaliteedijuhtimise testid](quality-tests.md)
- [Kvaliteedijuhtimise testgrupid](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
