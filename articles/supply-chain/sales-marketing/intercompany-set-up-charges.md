---
title: Kontsernisiseste tellimuste tasude seadistamine
description: See artikkel selgitab kontsernisiseste tellimuste tasude seadistamist
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 27633e09bfcf41fbbe5449b0d3b5f283eaf7ee13
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673658"
---
# <a name="set-up-charges-on-intercompany-orders"></a>Kontsernisiseste tellimuste tasude seadistamine

[!include [banner](../../includes/banner.md)]

Saate seadistada tasud, mis lisatakse kontsernisisestele tellimustele. Kui kontsernisisesele müügitellimusele lisatakse tasu, sünkroonitakse see automaatselt kontsernisisese ostutellimusega. See toimib kahepoolselt – kontsernisiseselt müügitellimuselt ostutellimusele ja vastupidi.

Tasudega saate lisada ka kontsernisisesele müügitellimusele kasumi, määratledes tasu kontsernisisese protsendina.

Kulude suhtes kontsernisiseste tellimuste seadistamisel lubate algse müügitellimuse netosummast kontsernisisese müügitellimuse sisemise kasumi arvutamisel. Soovite seda võib-olla teha juhul, kui teie kontsernisisene hankija müüb teile omahinnaga. Järgmises protseduuris kirjeldatakse, kuidas teha seda kontsernisiseste klientide puhul. Saate kasutada sama protseduuri hankijate puhul.

1. Minge jaotisse **Müügireskontro \> seadistus \> Tasud \> Kliendi tasugrupid**.
1. Looge tasugrupp.
1. Avage **Müügireskontro \> Kliendid \> Kõik kliendid**. Valige kliendi konto link. Valige toimingupaanil vahekaart **Klient** ja seejärel kiirkaart **Müügitellimus**.
1. Välja redigeerimise lubamiseks klõpsake tegumiribal **Redigeeri**. Valige väljal **Tasugrupp** kontsernisisene tasugrupp, mille häälestasite 2. etapis.
1. Minge jaotisse **Müügireskontro \> Seadistus \> Tasud \> Automaatsed tasud**.
1. Tasude seadistamiseks täitke vastavad väljad.
1. Valige väljal **Kliendisuhe** kontsernisisene tasugrupp, mille häälestasite 2. etapis.
1. Kiirkaardi **Read** väljal **Kategooria** valige **Kontsernisisene protsent**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
