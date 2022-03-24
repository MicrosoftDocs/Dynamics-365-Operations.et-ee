---
title: Ootamatu erinevus taotluse ja seansi andmete vahel testimise ajal
description: Ootamatu erinevus lao rakenduse ülesande valideerimistulemuste taotluse ja seansi andmete vahel.
author: mamuszal
ms.date: 03/11/2022
ms.topic: troubleshooting
ms.search.form: WHSValidatorRunInstance_executeRun
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mamuszal
ms.search.validFrom: 2022-03-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: da8f0506a76b0d0cc02bfc2e1bff01b4ddccb578
ms.sourcegitcommit: 941119133be1765f653d5d5270dfdf58466e1d07
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/17/2022
ms.locfileid: "8456952"
---
# <a name="unexpected-difference-between-request-and-session-data-during-testing"></a>Ootamatu erinevus taotluse ja seansi andmete vahel testimise ajal

Tõrkekood: WarehouseMobileDeviceRequestInputValidationError

## <a name="symptoms"></a>Sümptomid

Kui kasutate laorakenduse ülesande [kinnitamise raamistikku](/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/warehouse-app-task-validation-rsat), tagastab kontrollija järgmise tõrketeate:

> Ootamatu erinevus taotluse ja seansi andmete vahel. Rikub lao mobiilsete seadmete XML-protokolli. REQUEST_XML_TAMPERING

## <a name="cause"></a>Põhjus

Tõrge ilmneb, kui testkäivituses edukalt käitatud viimase astme väljund ei vasta järgmise sammu salvestatud sisendile. Selline olukord võib tekkida, kuna toimingu kinnitaja ei kasuta järgneva sammu sisendina eelmise sammu väljundit. Selle asemel kasutatakse iga sammu puhul sisendina salvestatud XML-i.

Enamasti ilmneb tõrge, kui käivitate ülesande uuesti, kuid test nõuab teatud kirjeid, mida sama ülesande eelmine käitus muutis või eemaldas.

## <a name="resolution"></a>Lahendus

Laorakenduse ülesande valideerimistesti käitamine ei ole idempotenttoiming, vaid muudab aluseks olevaid andmeid. Seetõttu peate enne ülesande uuesti käivitamist lähtestama asjakohased andmed.

1. Vaadake üle viimase eduka katsesamme väljund XML, et määratleda, kus teie test välja jätti.
1. Kontrollige katset ja veenduge, et kõik nõutud müügitellimused, üleviimistellimused, tööpäised ja muud kirjed on endiselt olemas ja on oodatud olekus.
1. Saate puuduvaid või muudetud kirjeid uuesti luua või redigeerida. Teise võimalusena looge uus katseseadistus ja kujundage katse, et kasutada kehtivaid olemasolevaid kirjeid.
