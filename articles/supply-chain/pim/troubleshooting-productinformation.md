---
title: Tooteteabe tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada tooteteabega töötamisel tekkivaid probleeme.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4c505ccfd1998acd40dbae715c7fa572e315af2e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007512"
---
# <a name="troubleshoot-product-information"></a>Tooteteabe tõrkeotsing

Selles teemas kirjeldatakse, kuidas lahendada tooteteabega töötamisel tekkivaid probleeme.

## <a name="i-cant-delete-a-released-product"></a>Väljastatud toodet ei saa kustutada.

### <a name="issue-description"></a>Probleemi kirjeldus

Väljastatud toote ja kõigi selle variante saate kustutada ainult siis, kui väljastatud tootel pole seotud kandeid.

### <a name="issue-resolution"></a>Probleemi lahendamine

Väljastatud toote või toote koondandmete kustutamiseks toimige järgmiselt.

1. Sulgege kaupade kõik avatud kanded.
1. Vähendage varude väärtuseks 0 (null).
1. Teostage lao sulgemine.
1. Kustutage toote koondandmetest kõik toote variandid, mida soovite kustutada.

## <a name="can-i-change-the-item-number-of-a-released-product"></a>Kas ma saan muuta väljastatud toote kaubakoodi?

Enamikul juhtudel ei saa muuta väljastatud toodete kaubakoode, kuna see muudatus põhjustab teabe riknemist. Kaubakoodi saate muuta ainult siis, kui peate parandama andmete korruptsiooni, mille põhjustas selle väljastatud toote esmase võtme ümbernimetamine, nagu on mainitud [eemaldatud või iganenud funktsioonid Finance and Operations 10.0.0 platvormi uuendusega 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).

Kui soovite redigeerida väljastatud toodete kaubakoode, siis [hääletage selle idee poolt ideede portaalis](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a>Toote vaikimisi tühjendamise põhimõtet ei sisestata koosluse reale.

### <a name="issue-description"></a>Probleemi kirjeldus

Kui lisate koosluse reale kauba, ei kasuta süsteem kaubale seadistatud vaikimisi tühjendamise põhimõtte teavet. Teisisõnu ei kuvata kauba tühjendamise põhimõtet **Koosluse real**.

### <a name="issue-resolution"></a>Probleemi lahendamine

Kui määrate koosluse rea jaoks tühjendamise põhimõtte, rakendub see koosluse reale. Kui tühjendamise põhimõte on tühi või kui see pole seatud koosluse reale, rakendub koosluse reale endiselt kaubale seadistatud tühjendus, kuigi seda ei ole koosluse real kuvatud.

Microsoft Dynamics 365 Supply Chain Management rakenduse muude funktsioonide vaike-loogika ei tööta tavaliselt sel viisil. Praegust käitumist ei saa aga muuta. Vastasel korral võidakse mõned olemasolevad kohandused, mis sellele tuginevad, katki minna.

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a>Süsteem võimaldab mul salvestada erinevatele kaupadele või erinevate dimensioonidega samale kaubale dubleeritud vöötkoode.

Süsteem ei jõusta praegu kordumatuid vöötkoode ja selle piirangu lisamine oleks murranguline muutus. Microsoftil on tõestus selle kohta, et see muudatus rikub mõningate olemasolevate klientide paigaldused. Siiski kaalume laiemat kujunduse muudatust, et seda funktsiooni tulevikus lubada.

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a>Kauba kirje mallide redigeerimisel kuvatakse järgmine tõrketeade: "Lao asukohta ei saa luua, kuna kaupa ei ole laos. Laos olevate kaupade puhul peab seostatud kauba mudeli grupis olema valitud laos olev toode. "

### <a name="issue-description"></a>Probleemi kirjeldus

See probleem ilmneb juhul, kui te järgite neid samme, et proovida luua malli kauba jaoks, mida ei ole laos.

1. Avage väljastatud toode, mida ei ole laos.
1. Toiminguriba vahekaardil **Valikud** valige suvand **Teabe salvestamine**.
1. Valige **Teabe salvestamine** dialoogiaknas **Ettevõtte kontode mall**.

Sellisel juhul kuvatakse järgnev veateade:

> Lao asukohta ei saa luua, kuna kaupa ei ole laos. Laos olevate kaupade puhul peab seostatud kauba mudeli grupis olema valitud laos olev toode.

### <a name="issue-resolution"></a>Probleemi lahendamine

Toote mallide loomise protsess nõuab täiendavat toote-spetsiifilist loogikat. Seetõttu ei saa selleks otstarbeks kasutada üldist **Ettevõte kontode mallid** nuppu. Selle asemel toimige järgmiselt.

1. Avage väljastatud toode.
1. Toiminguribal valige **Toote** vahekaardil **Uus** grupis **Mall \> Loo jagatud mall**.

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a>Toote atribuutides lisatud vaikimisi abiteksti ei sisestata väljastatud tootesse.

Kirjeldus ja abitekst, mis lisatakse toote atribuutidele, ei ole kuvatud ega sisestatud vaikimisi väljastatud toodetes. Selline käitumine on nii kavandatud.

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a>Vaikimisi sisestatav kogus erineb, kui see on registreeritud kooslusest ja kui see on registreeritud koosluse versioonist.

### <a name="issue-description"></a>Probleemi kirjeldus

Kui lisate kauba kooslusele, seatakse koguse väärtuseks 1, selle asemel, et näidata **Min tellimuse kogus** väljal defineeritud kogust valitud toote **Vaikimisi valitud sätete** lehel. Kuid kui lisate kauba koosluse versioonist ning kaup ja variant on valitud, võtab vaikimisi sisestatud kogus arvesse minimaalset kogust, mis on määratud kindla dimensiooni jaoks määratud vaikimisi tellimuse sätetes.

### <a name="issue-resolution"></a>Probleemi lahendamine

Selline käitumine on oodatud. Kuid seejuures on teada probleem, et see loogika erinev koosluses ja koosluse versioonis. Sellegipoolest ei muudeta seda käitumist, kuna muudatus võib mõjutada paljude erinevate klientide stsenaariume.

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a>Väljastatud toote üksikasjades ei saa muuta manustatud pilte, mis laaditi alla toote dokumendi manuste andmete üksusest.

### <a name="issue-description"></a>Probleemi kirjeldus

See probleem võib ilmneda, kui manustate pildi kaubale, kasutades *Toote dokumendi manustes* olevaid andmeid. Sel juhul kuvatakse kauba pilt kauba kohta. Kui aga valite **Muuda pilti**, ei kuvata üleslaetud piltide loendis mitte midagi. Lisaks ei kuvata kaubale manuseid.

### <a name="issue-resolution"></a>Probleemi lahendamine

*EcoResProductDocumentAttachmentEntity* üksus (*Toote dokumendi manused*) impordib dokumendi manused *toodetele*, kuid mitte *väljastatud toodetele*. (Väljastatud tooted on tuntud ka kui *kaubad*.) Kui soovite vaadata kauba manuseid **Väljastatud toote üksikasjade** lehel, peate selle asemel kasutama *EcoResReleasedProductDocumentAttachmentEntity* üksust (*Väljastatud toote dokumendi manused*).

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a>Microsoft Flow ühendus näitab järgmist tõrketeadet: "Värskendamine pole välja"ProductNumber" jaoks lubatud."

### <a name="issue-description"></a>Probleemi kirjeldus

See probleem ilmneb juhul, kui proovite uuendada välja **Tootenumber**, kasutades *Väljastatud toodete* üksust V2 ja Microsoft Flow rakendust.

### <a name="issue-resolution"></a>Probleemi lahendamine

Selline käitumine on oodatud. Väljastatud toote tootenumbri redigeerimise võimalus eemaldati Dynamics 365 Finance and Operations 10.0.0 platvormiuuendusega 24, et aidata vältida andmete korruptsiooni. Erandjuhtudel, kui peate parandama rikutud andmeid, mille põhjustas väljastatud toote peamise võtme ümbernimetamine, võtke ühendust Microsofti tugiteenusega selle piirangu ajutise eemaldamise taotlemiseks.

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a>Ma ei saa luua väljastatud toote varianti teises juriidilises isikus.

### <a name="issue-description"></a>Probleemi kirjeldus

Kui proovite väljastada toote koondandmeid, millel pole variante, ja seejärel luua igas juriidilises isikus (ettevõttes) variandid, nagu need on nõutud, ei saa te variante väljastada kasutades selleks variantide soovitusi. Samuti ei saa te variante käsitsi luua.

### <a name="issue-resolution"></a>Probleemi lahendamine

Selline käitumine on nii kavandatud. Toote koondandmete seoseid ja dimensioone, mida koondandmed saavad rakendada, hoitakse ühiskasutataval tasemel. Seetõttu ei saa te luua saadaolevaid dimensioone ühise toote koondandmetele kindlas juriidilises isikus, kus need dimensioonid väljastatakse, ja seejärel korrata protsessi igas juriidilises isikus, kus dimensioone nõutakse. Selle asemel peate muutma oma väljastusprotsessi, et kohanduda kavandatud protsessiga.

Siin on toodete väljastamise protsess.

1. Looge ühiskasutatava toote koondandmed ja dimensioonid, mida saab juriidilistele isikutele väljastada.
1. Väljastage tooted juriidilistele isikutele kasutades variantide soovitusi või lisage väljastatavad kombinatsioonid käsitsi.

Teise võimalusena saate väljastatud toote luua otse.

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a>Kui ma vabastan variandi teises ettevõttes, kuvatakse järgmine tõrketeade: "Toote variant koos määratud dimensioonidega on juba loodud."

### <a name="issue-description"></a>Probleemi kirjeldus

Kui toote variant on juba väljastatud ettevõttes A ja proovite selle väljastada ettevõttes B, kasutades nuppu **Uus**, mis asub **Väljastatud toote variandid** lehel, kuvatakse järgmine tõrketeade:

> Määratud dimensioonidega tootevariant on juba loodud.

### <a name="issue-resolution"></a>Probleemi lahendamine

**Uus** nupp **Väljastatud toote variandid** lehel loob variandi ja väljastab selle ettevõtte kontekstis. Kui variant on juba loodud, ei saa te kasutada nuppu **Uus**, et see väljastada teises ettevõttes.

Probleemi lahendamiseks avage **Toote koondandmed** ja valige **Väljasta toode**, et väljastada olemasolev variant soovitud ettevõttes.
