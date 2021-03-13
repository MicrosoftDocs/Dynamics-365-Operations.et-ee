---
title: Tehingumeilide kohandamine tarneviisi alusel
description: Selles teemas kirjeldatakse, kuidas seadistada kohandatud meilimalle kindlate teatisetüüpide ja tarneviiside jaoks Microsoft Dynamics 365 Commerce'is.
author: stuharg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: f4ecb990cfe792e92142f922c43c71ef8494e117
ms.sourcegitcommit: da17648c296b22d517eadb2f71c7803672e5648d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031844"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a>Tehingumeilide kohandamine tarneviisi alusel

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas seadistada kohandatud meilimalle kindlate teatisetüüpide ja tarneviiside jaoks Microsoft Dynamics 365 Commerce'is.

Tehingumeile saab nüüd kohandada teatisetüübi (nt **Tellimus on loodud**, **Tellimus on pakitud** või **Tellimus on arveldatud**) ja tarneviisi (nt üleöö, kauplusest kättesaamine või tänaval kättesaamine) kombinatsiooni jaoks. Kohandatud tehingumeilid võimaldavad jaemüüjatel täita klientide tellimusi viisil, mis sobib tellimuse tarneviisiga. Näiteks sündmust „Tellimus on pakitud“ saab kohandada nii, et see annab juhiseid tänaval kättesaamise kohta sellistele klientidele, kes valisid tänaval kättesaamise. Teise võimalusena võib see anda kättetoimetaja ja tarnimise teavet klientidele, kes otsustavad oma tellimuse tarnida.

> [!NOTE]
> Kohandatud tehingumeilide funktsiooni kasutamiseks peate esmalt sisse lülitama funktsiooni **Kohanda tehingumeilimalle tarneviisi järgi**, minnes Commerce'i peakontoris jaotisse **Tööruumid \> Funktsioonihaldus**.

Meile saab kohandada tarneviisi järgi järgmiste teatisetüüpide korral.

- **Tellimuse tühistamine** – see meiliteatise tüüp on uus.
- **Tellimus loodud**
- **Tellimus on kinnitatud.**
- **Tellimus on arveldatud** – see meiliteatise tüüp on uus. Seda saab kasutada teatisetüübi **Tellimus on lähetatud** asemel, mis saadab teatise iga arvesündmuse kohta, mille tarneviis on lähetamine (mitte järeletulemine, kaasavõtmine ega elektrooniline tarneviis).
- **Tellimus on komplekteeritud**
- **Tellimus on pakitud**
- **Tellimus on järeletulemiseks valmis** – seda teatisetüüpi saab kohandada tarneviisi järgi ainult siis, kui funktsioon **Mitme järeletulemispõhise tarneviisi tugi** on sisse lülitatud. Sellisel juhul on see teatisetüüp funktsionaalselt samaväärne teatisetüübiga **Tellimus on pakitud**.
- **Makse nurjus**
- **Asendustellimus on loodud**

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a>Meilimallide konfigureerimine kindlate tarneviiside jaoks

Selle toimingu puhul eeldatakse, et olete juba loonud uued kohandatud meilimallid ja lisanud need lehele **Organisatsiooni meilimallid**. Lisateavet meilimallide loomise ja üleslaadimise kohta leiate teemast [Meilimallide loomine tehingusündmuste jaoks](email-templates-transactions.md).

Meilimallide konfigureerimiseks kindlate tarneviiside jaoks Commerce'i peakontoris toimige järgmiselt.

1. Avage **Commerce'i meiliteatise profiil**.
1. Valige jaotises **Jaemüügisündmuse teatise sätted** olemasolev teatisetüüp.
1. Samal ajal kui teatisetüüp on ikka valitud, valige **Konfigureeri tarneviise**.
1. Valige dialoogiboksis **Tarneviisid** suvand **Uus**.
1. Valige tarneviis uuel real väljal **Tarneviis**.
1. Valige väljal **Meili ID** meilimall, mille soovite vastendada tarneviisiga.
1. Märkige ruut **Aktiivne**.
1. Täiendavate tarneviiside lisamiseks korrake samme 4–7.
1. Kui olete lõpetanud, valige **OK**.

> [!NOTE]
> - Kui müügitellimuse ridade tarneviise on mitu, kasutatakse vaikemalli. Vaikemall on mall, mis on lehel **Commerce'i meiliteatise profiil** vastendatud teatisetüübiga.
> - Kui müügitellimusel on tarneviis, mida pole kohandatud meilimalli jaoks konfigureeritud, kasutatakse vaikemeilimalli.

## <a name="additional-resources"></a>Lisaressursid

[Kõnekeskuse tellimuste loomine](tasks/create-call-center-orders.md)

[Kassas tarneviisi muutmine](pos-change-delivery-mode.md)
