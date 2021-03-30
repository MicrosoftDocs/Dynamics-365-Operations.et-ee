---
title: Komplekteerimise ja pakkimise tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada komplekteerimisel ja pakkimisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
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
ms.openlocfilehash: 01e33b63e09a035f5243bd57faf53b522737c987
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223238"
---
# <a name="troubleshoot-picking-and-packing"></a>Komplekteerimise ja pakkimise tõrkeotsing

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lahendada komplekteerimisel ja pakkimisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a>Kuvatakse järgmine tõrketeade: "Dimensiooni asukohta ei saa jätta tühjaks, kui on seatud dimensiooni seerianumber."

### <a name="issue-description"></a>Probleemi kirjeldus

See tõrketeade kuvatakse, kui loote seeriaüksusele üleviimistellimuse, kasutades ladu, mis on lubatud täiustatud laohalduse (WMS) jaoks, ja proovite pärast töö lõpetamist saadetist kinnitada.

### <a name="issue-resolution"></a>Probleemi lahendamine

**Lao vastuvõtu vaikimisi asukoht** on "päritolu" lao transiidilao jaoks on tühi. Probleemi lahendamiseks määrake transiidilaos vaikimisi vastuvõtu asukoht. Veenduge, et see asukoht on identifitseerimisnumbritega kontrollitav.

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a>Kuvatakse järgmine tõrketeade: "Vigane identifitseerimisnumber".

### <a name="issue-description"></a>Probleemi kirjeldus

See tõrketeade kuvatakse laorakenduses, kui skaneerite identifitseerimisnumbri või asukoha.

### <a name="issue-resolution"></a>Probleemi lahendamine

Veenduge, et identifitseerimisnumbri ID on olemas identifitseerimisnumbrite tabelis ja et identifitseerimisnumbril olevad kaubad ja kogused on saadaval (ehk need ei ole blokeeritud).

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a>Kuvatakse järgmine tõrketeade: "Välja 'koorma kaal' (=-%1) võib sisaldada ainult positiivseid numbreid. Uuendus on tühistatud."

### <a name="issue-description"></a>Probleemi kirjeldus

Te saate selle tõrketeate, kui on avatud töö töödeldes tööd pakkimisasukohtadest vaheasukohtadesse või vaheasukohtadest dokkimisasukohtadesse.

### <a name="issue-resolution"></a>Probleemi lahendamine

Selle probleemi lahendamiseks minge **Süsteemi administreerimise \> Perioodilised ülesanded \> Andmebaas \> Järjepidevuse kontroll** ja käivitage protsess **Lao koormuse kaalu järjepidevuse kontrollimiseks**.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>Kuvatakse järgmine tõrketeade: "Kogus on kehtetu kauba %1 korral."

### <a name="issue-description"></a>Probleemi kirjeldus

Te saate selle tõrketeate, kui püüate sooritada *tükeldatud komplekteerimist* mitme partii üleselt.

### <a name="issue-resolution"></a>Probleemi lahendamine

Laotööline peab laorakenduses kasutama *Lühikese komplekteerimise* protsessi. Kui proovite komplekteerida mitut partiid samast asukohast, saate laorakenduses kasutada ka **Täielikku** valikut.

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a>Ma ei saa liigutada kaupa asukohta, mis on identifitseerimisnumbri järgi kontrollitud.

### <a name="issue-description"></a>Probleemi kirjeldus

Koormal ei saa vähendada komplekteeritud koguseid.

### <a name="issue-resolution"></a>Probleemi lahendamine

Varasematel versioonidel ei saa koormal vähendada komplekteeritud koguseid. Siiski saate nüüd komplekteerimise tühistada identifitseerimisnumbri järgi kontrollitud asukohta. Peate koormaliinile määrama nii **Asukoha** väärtuse kui ka **Identifitseerimisnumbri** väärtuse **Komplekteeritud koguse vähendamise** lehel.

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a>Kas ma saan printida saatelehe või pakkimise sisu lao järgi?

### <a name="issue-description"></a>Probleemi kirjeldus

Soovite printida saatelehe või pakendi sisu lao või saidi alusel **Töö auditi malli rea uuendamise** lehel.

### <a name="issue-resolution"></a>Probleemi lahendamine

Kui prindite dokumendi prindihalduse sätete abil, piirake prindihalduse kaudu ulatus (sait/ladu), selle asemel, et valida **Redigeeri printimissätted** käsk **Töö auditi malli rea uuendamise** lehel.

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>Pärast müügitellimusest sisestamist ei saa saatelehte tühistada.

### <a name="issue-description"></a>Probleemi kirjeldus

Kui komplekteerimislehe ja saatmise protsessid on WMS-i jaoks lubatud, ei saa te saatelehte pärast müügitellimusest sisestamist tühistada.

### <a name="issue-resolution"></a>Probleemi lahendamine

WMS-i jaoks lubatud kaupade sisestatud saatelehtede korrigeerimiseks peab sisestus olema tehtud koormast, mitte otse tellimusest. Microsoft on seda probleemi hinnanud ja on määranud, et see on funktsiooni piirang. Üldiselt võib Müügitellimus, mis on komplekteeritud ja veetud laohalduse protsesside kaudu, olla saatelehega – uuendatud koormast või saadetisest ja müügitellimuse dokumendist. Kuid saatelehe uuendamisel müügitellimuse dokumendilt ei saa saatelehe tühistamist siiski teha koorma-või müügitellimusest. Seetõttu soovitame kasutada koormast saatelehe sisestamist. Sellisel juhul lubatakse tagasivõttu, mis tuleb teha koormast.

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a>Kuvatakse järgmine veateade: „Kogumi jaoks ei leidu piisavalt tööd”.

### <a name="issue-description"></a>Probleemi kirjeldus

Kui kasutate *Süsteemi suunatud kogumi komplekteerimise* protsessi, kui konfigureerite kogumi profiili, kus näiteks 10 positsiooni saab komplekteerida, toimib protsess plaanipäraselt, kui on piisavalt tööd, et komplekteerida 10 positsiooni. Kuid kui komplekteerimiseks on ainult kaheksa positsiooni, kuvatakse see tõrketeade, sest ühe kogumi jaoks ei ole piisavalt tööd.

### <a name="issue-resolution"></a>Probleemi lahendamine

Probleemi lahendamiseks redigeerige kogumi profiili ja seadke suvandi **Aktiveeri positsioone** väärtuseks *Ei*.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]