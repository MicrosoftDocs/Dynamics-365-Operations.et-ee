---
title: Kontsernisiseste tellimuste tasude seadistamine
description: See artikkel selgitab, kuidas seadistada kontsernisiseste tellimuste kulusid.
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
ms.openlocfilehash: 7b84c0bac6c31139170a99afc65cd08d70bd018e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885837"
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
