---
title: Koorma koostamise ja saadetiste tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada koorma koostamise ja saadetistega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c7dc9cc9de4d5089d497c36759931669ee2e9e55
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259502"
---
# <a name="troubleshoot-load-building-and-shipments"></a>Koorma koostamise ja saadetiste tõrkeotsing

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lahendada koorma koostamise ja saadetistega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a>Kuvatakse järgmine tõrketeade: "Te ei saa selle tellimuserea jaoks koorma rida luua, kuna see sisaldab varude dimensioone, mis on kehtetud..."

### <a name="issue-description"></a>Probleemi kirjeldus

Kui proovite tagastada müügitellimust lattu, kuvatakse järgmine tõrketeade:

> Te ei saa selle tellimuserea jaoks koorma rida luua, kuna see sisaldab varude dimensioone, mis on kehtetud. Te ei saa viidata varude dimensioonidele, mis asuvad reserveerimise hierarhias asukoha dimensiooni all. Eemaldage tellimuse realt kehtetud dimensioonid.

### <a name="issue-resolution"></a>Probleemi lahendamine

Kahjuks ei toeta toode koorma töötlemist müügiks tagastamise protsessiks. Seetõttu ei saa väljastada lattu tagastamise müügitellimust.

Müügitellimuste tehingutes ei saa viidata varude dimensioonidele, mis asuvad reserveerimise hierarhias **Location** dimensiooni all. Lahenduseks on eemaldada tellimuse realt kehtetud dimensioonid.

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a>Kuvatakse järgmine tõrketeade: "Üks rida on juba koormal. Ei ole võimalik lattu väljastada."

### <a name="issue-description"></a>Probleemi kirjeldus

Kui loote käsitsi koormaid või kui seadistate protsessi nii, et koormad on juba enne müügitellimuse rea sisestamist loodud, on eelduseks, et järgnev väljastus tehakse käsitsi ning kasutatakse koorma protsessi ja hinnangut.

Teises võimalikus stsenaariumis proovite teha automaatset väljastamist lattu, kuid voo protsessil ei õnnestunud tööd luua. Seetõttu luuakse avatud saadetis või koorem. See avatud saadetis või koorem blokeerib seejärel järgmised katsed tellimuse automaatselt väljastamiseks, kuni te kas kustutate avatud saadetise või koorma või töötlete uue voo käsitsi uuesti.

### <a name="issue-resolution"></a>Probleemi lahendamine

Saate väljastada müügitellimuse lehelt või teha automaatse väljastamise müügitellimuse lehelt ainult juhul, kui koormat pole enne lattu väljastamist olemas. Koorem luuakse automaatselt pärast voo töötlemist.

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a>Kuvatakse järgmine tõrketeade: "Saatelehe parandust ei saa töödelda. Saateleht sisaldab ainult kaupu, mille kohta kehtivad laohalduse protsessid, kuna need ei toeta saatelehe parandust."

### <a name="issue-description"></a>Probleemi kirjeldus

Pärast saatelehe sisestamist ei saa seda tühistada, kuna **Tühista** nupp ei ole saadaval. Samuti ei saa saatelehte parandada. Kui proovite, kuvatakse see tõrketeade.

### <a name="issue-resolution"></a>Probleemi lahendamine

Täpsema laohalduse (WMS) jaoks lubatud kaupade sisestatud saatelehtede korrigeerimiseks peate tegema sisestuse koormast, mitte otse tellimusest.

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a>Kuidas ma saan luua tööd voo asemel väljaminevatest koormatest?

### <a name="issue-description"></a>Probleemi kirjeldus

Siin on üks viis selle probleemi taasesitamiseks.

1. Looge väljaminev koorem müügitellimust või üleviimistellimust kasutades.
2. Väljasta koormus lattu.
3. Pange tähele, et komplekteerimise tööd pole veel loodud.

### <a name="issue-resolution"></a>Probleemi lahendamine

Kui töö tuleb luua kohe, kui koorem on väljastatud, tuleb teil voo mall vastavalt konfigureerida. Voo mallis seadke järgmised valikud väärtusele *Jah*:

- Automatiseeri voo loomine
- Töötle voogu lattu vabastamisel
- Automatiseeri voog vabastamine

## <a name="i-cant-re-release-a-partially-shipped-load"></a>Osaliselt saadetud koormat ei saa uuesti väljastada.

### <a name="issue-description"></a>Probleemi kirjeldus

Te ei saa osaliselt lähetatud koormat lattu väljastada. Kui teete lattu väljastamise, kuvatakse teade "Toiming lõpetatud", kuid midagi ei juhtu ja ülejäänud koguse jaoks tööd ei looda. See probleem ilmneb, kui kasutate transpordi koorma funktsiooni ja esineb puudulik reserveerimine.

### <a name="issue-resolution"></a>Probleemi lahendamine

[KB Issue 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Osaliselt saadetud koormaid saab uuesti levitada ja uuesti töödelda") on fikseeritud [versioonis 10.0.15](../get-started/whats-new-scm-10-0-15.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]