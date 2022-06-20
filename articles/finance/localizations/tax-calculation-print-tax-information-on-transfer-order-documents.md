---
title: Maksuinfo trükkimine ülekandekorralduse dokumentidele
description: See artikkel selgitab, kuidas maksuarvutusteenusega määratletud maksuteavet saab printida üleviimistellimuse dokumentidele.
author: Kai-Cloud
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-10-12
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: ca7a610162c539a0ecd74cf9e663f08ea80a7e44
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855198"
---
# <a name="print-tax-information-on-transfer-order-documents"></a>Maksuinfo trükkimine ülekandekorralduse dokumentidele

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas printida maksuteavet üleviimistellimuse dokumentidele. Euroopa Liidu (EL) käibemaksu (KM) regulatsiooni alusel ühendusesisese tarne ja ühendusesisese soetusena käsitatavate laoülekandmiste puhul saate ülekandekorralduse vormiarvedokumendi printida. 

Ülekandekorralduse dokumentidele lisatakse järgmised maksualased andmed:

- Varude ülekandmise nimed ning saatja- ja saatmisaadressid
- Hankija ja saaja maksukohustuslasena registreerimise numbrid
- Tarnitud kauba ühikuhind ja maksustatav summa
- Maksukood, -määr, -summa ja -direktiivid

Nende andmete konfigureerimiseks peate tegema järgmised peamised sammud.

1. [Lubage ja seadistage ülekandekorralduste maksufunktsioon](tasks/Tax-feature-support-for-transfer-order.md).
2. [Looge ja seadistage juriidilisele isikule mitu maksuregistrinumbrit](emea-multiple-vat-registration-numbers.md).
3. Seadistage maksukoodides maksuvabastuse kood, kirjeldus, maksudirektiivid ja prindikood. Näiteks luuakse ja sünkroonitakse kolm maksukoodi 365 Finantsis Microsoft Dynamics : **NL-Exempt**, **BE-RC-21** ja **BE-RC+21**.

    1. Rakenduses Finance minge **Maks** \> **Seadistamine** \> **Käibemaks** \> **Käibemaksuvabastuse koodid**.
    2. Valige **Muuda** ja sisestage **EÜ**-vabastuskoodi kirjeldus. Näiteks sisestage **Maksuvabad EÜ saadetised maksuregistri numbriga**.
    3. Valige suvandid **Maks** \> **Kaudsed maksud** \> **Käibemaks** \> **Käibemaksukoodid**.
    4. Valige maksukood **BE-RC-21** ja seejärel **Maksudirektiivid**.
    5. Valige suvand **Uus**.
    6. Sisestage väljale **Keel** väärtus **EN-US**. Seejärel sisestage väljale **Tekst** **Kauba üleandmist käsitlev dokument EL-i käibemaksudirektiivi 2006/112/EÜ artikli 138.2 punkti c tähenduses**.
    7. Sulgege leht.
    8. Valige kiirkaardil **Üldine** väljal **Prindi** suvand **Käibemaksumäär**.
    8. Valige **NL-vabastus** maksukood ja seejärel kiirkaardil **Üldine** väljal **Prindi** valige **Käibemaksumäär**.

    > [!NOTE] 
    > Maksukoodi, -määra ja -vabastuse kirjeldust ei prindita ülekandekorralduse dokumentidele, kui maksukoodi jaoks ei säilitata vabastuskoodi kirjeldust ega maksujuhiseid.

## <a name="print-the-transfer-order---shipment-document"></a>Prindi ülekandekorraldus – saatedokument

Pärast ülekande saatmist järgige ülekandetellimuse – saatedokumendi printimiseks järgmisi samme.

1. Avage **Varud** \> **Päringud ja aruanded** \> **Ülekandekorraldused** \> **Saatmine**.
2. Vahekaardi **Parameetrid** rühmas **Prindi** lubage **Maksuteave**.
3. Valige vahekaardil **Kaasatavad kirjed** **Filtreeri**, valige ülekandekorralduse number ja seejärel **OK**.
4. Valige ülekandekorralduse printimiseks **OK** – saatedokument.

## <a name="print-the-transfer-order---receipt-document"></a>Prindi ülekandekorraldus – kviitungi dokument

Pärast ülekande saamist järgige ülekandetellimuse – kviitungi printimiseks järgmisi samme.

1. Avage **Varud** \> **Päringud ja aruanded** \> **Ülekandekorraldused** \> **Saamine**.
2. Vahekaardi **Parameetrid** rühmas **Prindi** lubage **Maksuteave**.
3. Valige vahekaardil **Kaasatavad kirjed** **Filtreeri**, valige ülekandekorralduse number ja seejärel **OK**.
4. Valige ülekandekorralduse printimiseks **OK** – kviitung.

## <a name="print-the-transfer-overview-document"></a>Printige ülekande ülevaatedokument

Edastamise ülevaatedokumendi printimiseks järgige neid samme.

> [!NOTE]
> Maksuteave on saadaval ainult siis, kui ülekandekorraldus on saadetud või vastu võetud.

1. Avage **Varud** \> **Päringud ja aruanded** \> **Ülekandekorraldused** \> **Saatmise ülevaade**.
2. Vahekaardi **Parameetrid** rühmas **Prindi** lubage **Maksuteave**.
3. Valige vahekaardil **Kaasatavad kirjed** **Filtreeri**, valige ülekandekorralduse number ja seejärel **OK**.
4. Edastamise ülevaatedokumendi printimiseks valige **OK**.

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
