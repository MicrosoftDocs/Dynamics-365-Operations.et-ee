---
title: Hooldusobjektigrupid
description: Objektigrupid on kasulikud objektide kohta käivate andmete sortimiseks ja filtreerimiseks aruannetes ja statistikas kasutamiseks.
author: ShylaThompson
manager: tfehr
ms.date: 05/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9d19e29dbddb0bccf3221cc82e6dbb2c05f7e85
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5266075"
---
# <a name="service-object-groups"></a>Hooldusobjekti grupid 

[!include [banner](../includes/banner.md)]

Objektigrupid on kasulikud objektide kohta käivate andmete sortimiseks ja filtreerimiseks aruannetes ja statistikas kasutamiseks. Näiteks saate grupeerida objekte geograafilise asukoha või tüübi järgi.

## <a name="group-by-geographical-location"></a>Grupeeri geograafilise asukoha järgi

Saate kasutada seda grupeerimismeetodit, et näidata, kus asuvad erinevad objektid, mida teie ettevõte teenindab. Objektide grupeerimine geograafilise asukoha järgi võib olla kasulik ka siis, kui peate näiteks tuvastama objektid, millele juba selles konkreetses riigis/regioonis hooldust osutate.

## <a name="example"></a>Näide

Klient Belgiast helistab teie teeninduskeskusesse ja soovib luua hooldusleppe objektile ABC. Olete lisanud geograafilise asukoha objektigrupi, Belgia, kõigile Belgias teenindavatele objektidele. Kasutades seda gruppi filtrina, saate kiiresti otsida, et näha, kas ABC on kirjena teie rakenduses juba olemas või peate seadistama uue objekti. 

## <a name="group-by-type"></a>Grupeeri tüübi järgi

Saate kasutada seda grupeerimismeetodit, et näidata, millist tüüpi objektidele teie ettevõtte hooldust osutab. Objektide grupeerimine tüübi järgi võib olla kasulik ka siis, kui soovite näiteks luua uue objekti, mis põhineb sarnastel, programmis olemasolevatel objektidel.

## <a name="example"></a>Näide

Klient helistab ja soovib sõlmida hooldusleppe õhukonditsioneeri, HIJ, kohta. Teil ei ole selle masina kohta veel kirjet. Küll aga olete seadistanud objektigrupi nimega Õhukonditsioneerid ja olete lisanud selle grupi kõigile õhukonditsioneer-objektidele. Seega saate kiiresti otsida ja tuvastada kõik muud õhukonditsioneer-masinad ja kasutada nende objektide malliteavet, et HIJ-ile hooldusleppe ridasid luua. Kasutades objektigruppe sel viisil saate kiiresti uusi objekte seadistada ja määrata, milliseid hooldustöid nende puhul teostada. 

## <a name="create-service-object-groups"></a>Hooldusobjektide gruppide loomine

Looge gruppe, millele saate määrata teenuseobjekte. Teenuseobjektid on laokaup ja muud tooted, mille jaoks teenuseid tehakse. Teenuseobjekte rühmitades saate luua aruandeid sarnaste ja seotud teenuseobjektide jaoks. Näiteks võib teenuseobjekti grupp koosneda kahest teenuseobjektist: üks teenuseobjekt on komplekt ja teine on teenus komplekti installimiseks.

Teenuseobjekti gruppide loomiseks tehke järgmist.

1. Klõpsake valikuid **Hooldushaldus > Häälestus > Hooldusobjektid > Teenuseobjekti grupid**.

2. Uue teenuseobjekti grupi loomiseks klõpsake käsku **Uus**.

3. Sisestage teenusobjekti grupi kordumatu nimi ja soovi korral kirjeldus.

Saate määrata teenusegruppi objekte, kasutades vormi **Teenuseobjektid**. 

## <a name="see-also"></a>Vt ka

[Teenuseobjektide loomine](create-service-objects.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]