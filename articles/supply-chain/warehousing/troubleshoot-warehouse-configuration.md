---
title: Lao konfiguratsiooni tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada müügipakkumistega Microsoft Dynamics 365 Supply Chain Management rakenduse konfigureerimisel tekkivaid probleeme.
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
ms.openlocfilehash: 1fe285f05e5f1ddcb7bd206290b9954cbdaffc75
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5487093"
---
# <a name="troubleshoot-warehouse-configuration"></a>Lao konfiguratsiooni tõrkeotsing

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lahendada müügipakkumistega Microsoft Dynamics 365 Supply Chain Management rakenduse konfigureerimisel tekkivaid probleeme.

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a>Kuvatakse järgmine tõrketeade: "Identifitseerimisnumber või asukoht on kehtetu."

### <a name="issue-description"></a>Probleemi kirjeldus

See tõrketeade kuvatakse, kui skaneerite identifitseerimisnumbri või asukoha.

### <a name="issue-resolution"></a>Probleemi lahendamine

Veenduge, et identifitseerimisnumber ei ole reserveeritud muuks. See probleem tekkis, kui väärtus, mida kasutaja laos skaneeris, oli nii kehtiv asukoht kui ka kehtiv identifitseerimisnumber. See probleem lahendati versioonis 10.0.11.

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a>Kuvatakse järgmine tõrketeade: "Selle asukoha kohta peab määrama identifitseerimisnumbri."

### <a name="issue-description"></a>Probleemi kirjeldus

See tõrketeade kuvatakse, kui loote üleviimistellimuse, kasutades ladu, mis on lubatud täiustatud laohalduse (WMS) jaoks, ja proovite pärast töö lõpetamist saadetist kinnitada.

### <a name="issue-resolution"></a>Probleemi lahendamine

**Lao vastuvõtu vaikimisi asukoht** on "päritolu" lao transiidilao jaoks on tühi. Probleemi lahendamiseks määrake transiidilaos vaikimisi vastuvõtu asukoht. Veenduge, et see asukoht on identifitseerimisnumbritega kontrollitav.

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a>Kuvatakse järgmine tõrketeade: "Töömalli rida ei saa varude oleku muutmiseks luua, kuna töö tüüp on kehtetu. Valige mõni muu töö tüüp."

### <a name="issue-description"></a>Probleemi kirjeldus

Töömalli puhul ei saa valida *Varude oleku muutust* **Töö tüübi** veerus **Töömalli detailide** jaotises.

### <a name="issue-resolution"></a>Probleemi lahendamine

Selline käitumine on nii kavandatud. *Varude oleku muutmise* töö tüüpi kasutatakse ainult süsteemi protsessidega. Seda ei saa konfigureerida. Kuna töö tüüpide loend on fikseeritud kui loendamine, ei saa lisakirjeid **Töö tüübi** rippmenüüst välja filtreerida.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>Kuvatakse järgmine tõrketeade: "Kogus on kehtetu kauba 1% korral."

### <a name="issue-description"></a>Probleemi kirjeldus

Kogus ei kehti *tk* kauba kohta, kui on komplekteerimisel töö, millel on mitu identifitseerimisnumbrit ühes asukohas.

### <a name="issue-resolution"></a>Probleemi lahendamine

Veenduge, et väljastatud toote või tootevariandi väljad **Toote seeria ID** ja **Ühiku teisendused** on õigesti seadistatud.

Võtke arvesse, et tõrketeadet on parandatud versioonis 10.0.15 (vt [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). Uus veateade on: "Kogus ei ole kehtetu. Eeldatud %1 %2."

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Asukoha direktiivides müügitellimuse komplekteerimistöö kohta, ei hinda mitu SKU-suvandit mitme asukoha direktiivi tegevusi.

### <a name="issue-description"></a>Probleemi kirjeldus

*Müügitellimuste* töötellimuse tüübi ja *Komplekteerimise* töötüübid ei hinda mitme asukoha direktiivi tegevust, kui on valitud **Mitu SKU-d**. Hinnatakse ainult esimese asukoha direktiivi tegevust.

### <a name="issue-resolution"></a>Probleemi lahendamine

Uus funktsioon *Hinda mitme SKU-ga asukoha direktiivide kõiki tegevusi* on lisatud versiooni 10.0.15 (vt [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Selle funktsiooniga hinnatakse kõiki mitme SKU-ga asukoha direktiivide tegevusi. Kui vajate seda funktsiooni, kasutage selle sisselülitamiseks [Funktsiooni haldamist](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a>Ma ei saa kasutada lao rakendust osalise komplekteerimise tegemiseks.

### <a name="issue-description"></a>Probleemi kirjeldus

Ostu-ja üleviimistellimuste puhul ei saa kaupu vahele jätta ja teha osalist komplekteerimist.

### <a name="issue-resolution"></a>Probleemi lahendamine

Lehel **Mobiilse seadme menüükäsud** seadistage iga müügitellimuse või üleviimistellimuse töötlemiseks seadistatud menüükäsu kohta suvand **Luba tükeldamine** FasTab-is **Üldine** väärtuseks *Jah*.

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a>Kuidas ma saan muuta varude olekut osalise töökoguse kohta?

### <a name="issue-description"></a>Probleemi kirjeldus

Soovite teha varude oleku muutust partii osaliseks koguseks.

### <a name="issue-resolution"></a>Probleemi lahendamine

Selleks, et võimaldada töötajatel seda muudatust teha, saate luua menüü-üksuse lao rakendusele. **Mobiilse seadme menüü-üksused** lehel looge (või redigeerige) menüü-üksus, millel on järgnevad seaded:

- **Režiim:** *töö*
- **Kasuta olemasolevat tööd:** *Ei*
- **Töö loomise protsess:** *Liigutamine*
- **Kuva varude olek:** *Jah*

Vajadusel saate seadistada lehel muid välju.

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a>Asukohaprofiili laadimissildade halduse profiil ei takista varude tüüpide segamist.

### <a name="issue-description"></a>Probleemi kirjeldus

Kasutate *saadetise konsolideerimispoliitikaid*. Olete seadistanud *asukohaprofiili* jaoks *laadimissildade halduse profiili*, kuid töö loomisel segatakse varude tüübid lõppasukohas.

### <a name="issue-resolution"></a>Probleemi lahendamine

Laadimissildade halduse profiilid nõuavad töö eelnevat tükeldamist. Teisisõnu eeldab laadimissildade halduse profiil, et tööpäises pole mitut asetamise kohta.

Selleks, et laadimissildade halduse profiil saaks varude segamist tõhusalt hallata, tuleb seadistada tööpäise piir.

Selles näites on meie laadimissildade halduse profiil konfigureeritud nii, et **Varude tüübid, mida ei tohiks segada** on määratud olekusse *Saadetise ID*, ja me seadistame selle jaoks tööpäise piiri:

1. Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.
1. Redigeerimiseks valige **Töökäsu tüüp** (nt *Ostutellimused*).
1. Valige redigeeritav töömall.
1. Valige Toimingupaanil nupp **Päringu redigeerimine**.
1. Avage vahekaart **Sortimine** ja lisage rida järgmiste sätetega.
    - **Tabel** - *Ajutised töökanded*
    - **Tuletatud tabel** - *Ajutised töökanded*
    - **Väli** - *Saadetise ID*
1. Valige nupp **OK**.
1. Naasete lehele **Töömallid**. Valige toimingupaanilt suvand **Tööpäise piirid**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Märkige ruut, mis on seotud **Välja nimi** *Saadetise ID-ga*.
1. Valige toimingupaanil nupp **Salvesta**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
