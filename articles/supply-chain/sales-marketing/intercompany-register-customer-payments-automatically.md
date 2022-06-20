---
title: Kontsernisiseste kliendiarve maksete automaatne registreerimine
description: See artikkel selgitab, kuidas kontsernisisestele kliendiarvetele makseid automaatselt registreerida
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4e8f784cd310026f0a647a0f509999e11ab26ce5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878783"
---
# <a name="register-payments-automatically-for-intercompany-customer-invoices"></a>Kontsernisiseste kliendiarve maksete automaatne registreerimine

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management loob kontsernisisese kliendiarve sisestamisel kliendikande. See kliendikanne jääb avatuks kuni tasakaalusta lõpuni, mis tähendab, et see on makstud. Seonduva kontsernisisese ostutellimuse arve uuendamisel luuakse kliendikandele vastav hankijakanne. See hankijakanne jääb samuti avatuks kuni tasakaalustamiseni. Erinevuste riski alandamiseks luuakse ja sisestatakse ostureskontro maksetöölehe sisestamisel müügireskontro maksetööleht.

1. Avage jaotis **Müük ja turundus \> Kliendid \> Kõik kliendid**.
1. Toimingupaani vahekaardil **Üldine** valige suvand **Kontsernisisene**.
1. Kontsernisiseste müügireskontro maksete seadistamiseks **Kontsernisisesel** lehel müügitellimuste jaoks valige **Müügitellimuse poliitika** link.
1. Valige **Maksetöölehe** väljal müügireskontro maksetööleht, kuhu soovite registreerida kontsernisisesed hankijamaksed. Saate selle seadistada lehel **Müügireskontro parameetrid**.
1. Kui soovite töölehele automaatselt sisestada, märkige ruut **Sisesta tööleht automaatselt**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
