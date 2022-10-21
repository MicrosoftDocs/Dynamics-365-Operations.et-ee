---
title: Arve hõivamise lahenduse ülevaade
description: See artikkel annab teavet arve hõivamise lahenduse kohta.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76441220b93744527f412110db536601a2fa1dd9
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690978"
---
# <a name="invoice-capture-solution"></a>Arve hõivamise lahendus

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

See artikkel annab teavet arve hõivamise lahenduse kohta, mis loob automaatselt hankijaarved digitaalse arve piltidest.

Ostureskontro (AP) osakond haldab ja töötleb saadud kaupade ja teenuste arveid. AP raamatupidaja kinnitab hankijaarvete andmed järgmistel põhjustel:

- Lisa panuse vältimiseks, kui perioodi sulgemisel on vaja korrigeerimisi või parandusi
- Hankija arvetele õigeaegselt tasumine ja finantskahjumi ärahoidmine vea või pettuse tõttu

Optilise märgituvastuse (OCR) poolt on möödunud aastate jooksul olnud erinevates majandusharudes enim kasutusel. Nüüd on levinud digiteeritavad prinditud tekstid, nii et neid saaks elektrooniliselt redigeerida, otsida, salvestada tihendatult ja kuvada võrgus. Digitaalteksti saab kasutada masinaprotsessides, nagu kaasarvutus, masina tõlge, tekstist-kaasatuseni, võtmeandmed ja tekstikaevandamine.

Sisulise teabe (AI) tehnoloogia on võimaldanud tänapäevastel OCR-lahendustel lugeda erinevate hankijate erinevaid arvevorminguid ilma inimese sekkumiseta. Rohkem ettevõtteid tunnistab, et nad saavad kokku salvestada panuse ja parandada täpsust, töötledes arveid automatiseerimise kaudu, selle asemel et teha käsitsi töötlemist.

## <a name="system-landscape"></a>Süsteemi horisontaalpaigutus

Järgmine näide näitab arve hõivamise lahenduse põhikomponente ja samme.

[![Arvehõive lahenduse komponendid ja etapid](./media/Invoice-capture2.png)](./media/Invoice-capture2.png)

## <a name="required-roles"></a>Nõutavad rollid

Järgmine tabel näitab rolle, mis on vajalikud arve hõivamise lahenduse häälestamiseks ja kasutamiseks.

| Roll          | Toimingud | Süsteemid | Rollinimed |
|---------------|---------|---------|-----------|
| Administraator | <ul><li>Saate häälestada keskkondi Microsoft Power Platform.</li><li>Lahenduste juurutamine sees Microsoft Power Platform</li><li>Seadistage ühendused Dynamics 365 ja AI Builder.</li><li>Seadistage Azure Data Lake Storage asukohad.</li></ul> | <ul><li>Dynamics 365</li><li>Microsoft Power Platform</li><li>Azure Data Lake Storage</li></ul> | <ul><li>Dynamics 365 administraator</li><li>Power Platform-i administraator</li><li>Talletuslao andmete omanik</li></ul> |
| AI tegija      | <ul><li>Voogude haldamine.</li><li>Looge kohandatud AI-mudelid.</li></ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Kodanik tegijad</li></ul> |
| AP ametnik      | <ul><li>Vaadake üle ja tehke toimingud hankija arve paigutamisalas.</li><ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Uus AP-ametniku roll Power Platform</li></ul> |
| AP ametnik      | <ul><li>Tehke igapäevaseid toiminguid AP-ametnikuna.</li><li>Liikuge hankija arve jaotusalale.</li></ul> | <ul><li>Dynamics 365</li></ul> | <ul><li>Ostureskontro ametnik</li></ul> |
  
Lisateavet arve hõivamise installimise kohta vt arve hõivamise [installimine](../accounts-payable/install-invoice-capture.md).  
