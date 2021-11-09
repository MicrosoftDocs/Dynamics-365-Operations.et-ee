---
title: Kontsernisiseste kliendiarve maksete automaatne registreerimine
description: See teema selgitab kontsernisiseste kliendiarve maksete automaatset registreerimist
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: ffc5c7bf44989fbcc18e940b5a7c9df81260d770
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548223"
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