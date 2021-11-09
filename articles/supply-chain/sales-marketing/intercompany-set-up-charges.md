---
title: Kontsernisiseste tellimuste tasude seadistamine
description: See artikkel selgitab kontsernisiseste tellimuste tasude seadistamist
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 3786df5ce185fa8433d7c69bed5bef09b4983b8b
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548222"
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