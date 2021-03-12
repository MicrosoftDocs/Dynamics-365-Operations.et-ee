---
title: Hankija kannete loendi leht
description: Selles teemas antakse teavet rakenduse Microsoft Dynamics 365 Finance hankija kannete loendilehe kohta.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 17059dc2343df66e899a3c22908875be6b6de4ef
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993234"
---
# <a name="vendor-transactions-list-page"></a>Hankija kannete loendi leht

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Kuva tasakaalustused

Nupp **Kuva tasakaalustused** toimingupaanil annab kiire juurdepääsu tasakaalustuste ajaloole ja üksikasjalikku lisateavet kogu tasakaalustuskande kohta. Saate ka kuvada lisakandeid, mis on seotud valitud kandega kas seetõttu, et need olid osa samast tasakaalustusest või kuna need on maksed, mis loodi samas makse töölehes.

1. Valige suvandid **Ostureskontro \> Kõik hankijad**.
2. Valige hankija, kellel on kanded, ja seejärel valige toimingupaani vahekaardil **Hankija** suvand **Kanded**.
3. Valige uuritav kanne ja seejärel valige toimingupaanil suvand **Kuva tasakaalustused**.

    Avaneb dialoogiboks **Kuva tasakaalustused**, kus kuvatakse valitud kande ja kõik dokumendid, mis on selle suhtes tasakaalustatud. See dialoogiboks meenutab tasakaalustuste ajaloo vaadet, aga sisaldab kõiki seotud dokumente.

4. Selles dialoogiboksis saate teha mitmesuguseid toiminguid. Valige üks või mitu kannet ja seejärel valige üks järgmistest nuppudest.

    - **Kuva seotud** – kuvab kõik hankija maksetöölehe kanded ja päevaraamatu kanded, mis loodi töölehtedes, milles loodi loendis kuvatud dokumendid. Näiteks makse kuvamisel kuvatakse kõik maksetöölehel, milles see loodi, olevad maksed. Arve või makse kuvamisel, mis loodi päevaraamatus, kuvatakse kõik päevaraamatus, milles see loodi, olevad dokumendid. Peale selle kuvatakse kõik nende dokumendiloendiga seotud tasakaalustused. Seotud maksete vaatamise ajal muutub nupu sildiks **Kuva tasakaalustused**. Valige suvand **Kuva tasakaalustused**, et kuvada ainult need kanded, mis kuvati dialoogiboksi **Kuva tasakaalustused** avamisel.
    - **Kuva ajalugu** – kuvatakse kannete tasakaalustamisajalugu. Valige dialoogiboksi sulgemiseks suvand **Sule**.
    - **Kuva raamatupidamine** – kuvatakse kõik valitud dokumentidega seotud kanded. Valige dialoogiboksi sulgemiseks suvand **Sule**.
    - **Ekspordi** – valitud kanded eksporditakse Microsoft Excelisse.
    - **Kannete tasakaalustamine** – see nupp kuvatakse ainult siis, kui valitud algdokument ei olnud täielikult tasakaalustatud. Selle nupu valimisel kuvatakse dialoogiboks **Kannete tasakaalustamine**, kus saate valida tasakaalustamiseks kanded.
    - **Tasakaalustamise tühistamine** – see nupp kuvatakse ainult siis, kui valitud algdokument oli täielikult tasakaalustatud. Selle nupu valimisel kuvatakse dialoogiboks **Tasakaalustamise tühistamine**, kus saate selle dokumendi tasakaalustamised tühistada.

## <a name="global-transactions"></a>Globaalsed kanded

See **Globaalsete kannete** nupp kuvatakse ka **Hankija kannete** loendilehel. See nupp võimaldab kuvada kõik hankija kanded kõigis juriidilistes isikutes. Loendilehel **Hankija kanded** kuvatakse kanded ainult nende juriidiliste isikute puhul, millele kasutajal on tema turbesätete alusel juurdepääs.

Loendilehel kuvatakse kõik nende hankijate kanded, kellel on sama osapoole ID mis hankijal, kellega alustasite. Näiteks kui hankijal US-001 ühes juriidilises isikus on sama osapoole ID mis hankijal DE-001 teises juriidilises isikus, kuvatakse kõik kanded mõlema hankija ID kohta.

Loendilehe **Hankija kanded** menüüd erinevad olenevalt kande juriidilisest isikust. Näiteks kui mõni funktsioon on saadaval ainult Šveitsi juriidilistele isikutele, kuvatakse selle funktsiooni menüüsuvandid ainult Šveitsi kande valimisel.

Selle funktsiooni kasutamiseks tehke järgmist.

1. Valige suvandid **Ostureskontro** \> **Kõik hankijad**.
2. Valige hankija ja seejärel valige toimingupaani vahekaardil **Hankija** grupis **Kanded** suvand **Globaalsed kanded**.

## <a name="more-transaction-filters"></a>Rohkem kannetefiltreid

Avatud kandeid kuvav filter on asendatud uue filtriga, mis võimaldab kuvada rohkem kannete kombinatsioone. Väljal **Kuva** on saadaval järgmised suvandid.

- **Kõik** – kuvatakse kõik valitud hankijate kanded (avatud ja suletud).
- **Suletud** – kuvatakse ainult täielikult tasakaalustatud ja suletud kanded.
- **Avatud** – kuvatakse ainult kanded, mis pole täielikult tasakaalustatud.
- **Avatud, sealhulgas sulgemise kuupäev või pärast kuupäeva** – kuvatakse ainult kanded, mis pole täielikult tasakaalustatud teie määratud kuupäeval või pärast seda. Selle suvandi valimisel saate muuta filtri kõrval kuvatavat kuupäeva. Kanded, mille puhul on suvandi **Viimase tasakaalustuse kuupäev** väärtus teie määratud kuupäeval või pärast seda, kuvatakse loendis isegi siis, kui need kanded on tänase kuupäeva seisuga täielikult tasakaalustatud. Saldo näitab siiski saldot tänase, mitte valitud kuupäeva seisuga.

Valuutateisenduse kannete varjamiseks valige märkeruut **Peida valuuta ümberhindamised**.

## <a name="modify-due-dates-and-discount-dates"></a>Kuupäevade ja allahindluskuupäevade muutmine

Saate värskendada avatud kliendikannete kuupäevi ja allahindluskuupäevi. Väljaandes 8.1 saate lisada loendilehele **Hankija kanded** tähtajad. Klõpsates loendilehel **Hankija kanded** tähtaega, saate muuta dialoogiboksis **Tähtaja ja skonto kuupäevade värskendamine** ka tähtaegu, allahindluskuupäevi, maksetingimusi ja skonto tingimusi.

### <a name="activate-the-feature"></a>Funktsiooni aktiveerimine

Loendilehele **Hankija kanded** tähtaegade lisamiseks ja kande maksesätete muutmiseks dialoogiboksi **Tähtaja ja skonto kuupäevade värskendamine** abil tehke järgmist.

1. Valige suvandid **Ostureskontro \> Seadistus \> Ostureskontro parameetrid**.
2. Seadke vahekaardil **Tasakaalustused** suvandi **Kuva tähtaeg ja luba redigeerimine** sätteks **Jah**.
3. Selle funktsiooni lubamiseks on hankijakannetele lisatud uued väljad. Need väljad täidetakse uue kande lõpuleviimisel. Need täidetakse ka siis, kui avate dialoogiboksi **Tähtaja ja skonto kuupäevade värskendamine**. Kui seate suvandi **Kuva tähtaeg ja luba redigeerimine** sätteks **Ei**, kuvatakse dialoogiboks **Makseteabe värskendamine**.  Olemasolevate kannete kohe uuendamiseks valige suvand **Värskenda kõiki olemasolevaid kandeid**. Teise võimalusena väljade täitmiseks ainult uute kannete puhul valige suvand **Jätka värskendamiseta**.

Nüüd lisatakse tähtaeg loendilehele **Hankija kanded**, nii et teil on kannete tähtaega ja skonto kuupäevi lihtsam muuta.

### <a name="modify-the-payment-settings"></a>Maksesätete muutmine

Loendilehel **Hankija kanded** kuvatakse kõik hankija kanded. Kande tähtaja valimisel kuvatakse dialoogiboks. Selles dialoogiboksis kuvatakse tähtaja ja skonto arvutuste aluskuupäev, maksetingimused, skonto tingimused ja skonto kuupäevad.

Igal väljal on kandele selle redigeerimisel erinev mõju.

- **Aluskuupäeva redigeerimine** – tähtaega ja allahindluskuupäevi muudetakse nii, et aluskuupäev on dokumendi kuupäev.
- **Tähtaja redigeerimine** – muudetakse ainult tähtaega.
- **Allahindluskuupäevade redigeerimine** – muudetakse ainult allahindluskuupäevi.
- **Maksetingimuste redigeerimine** – tähtaega muudetakse aluskuupäeva ja maksetingimuste alusel.
- **Skonto tingimuste redigeerimine** – skontosid muudetakse aluskuupäeva ja skonto tingimuste alusel.

Kui olete maksesätete redigeerimise lõpetanud, valige muudatuste salvestamiseks käsk **Sule**.
