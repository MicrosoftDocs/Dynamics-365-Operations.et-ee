---
title: Kliendi kannete loendi leht
description: See teema annab teavet rakenduse Microsoft Dynamics 365 Finance kliendi kannete loendilehe kohta.
author: mikefalkner
manager: aolson
ms.date: 08/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 948f83d56e560cc21205294c15de4b2097d2ad2e
ms.sourcegitcommit: e544c51a68ad5daf748c0e877bdbde094ad40bd2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2020
ms.locfileid: "4442585"
---
# <a name="customer-transactions-list-page"></a>Kliendi kannete loendi leht

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Kuva tasakaalustused

Nupp **Kuva tasakaalustused** toimingupaanil annab kiire juurdepääsu tasakaalustuste ajaloole ja üksikasjalikku lisateavet kogu tasakaalustuskande kohta. Saate ka kuvada lisakandeid, mis on seotud valitud kandega kas seetõttu, et need olid osa samast tasakaalustusest või kuna need on maksed, mis loodi samas makse töölehes.

1. Valige suvandid **Müügireskontro \> Kõik kliendid**.
2. Valige klient, kellel on kanded, ja seejärel valige toimingupaani vahekaardil **Klient** suvand **Kanded**.
3. Valige uuritav kanne ja seejärel valige toimingupaanil suvand **Kuva tasakaalustused**.

    Avaneb dialoogiboks **Kuva tasakaalustused**, kus kuvatakse valitud kande ja kõik dokumendid, mis on selle suhtes tasakaalustatud. See dialoogiboks meenutab tasakaalustuste ajaloo vaadet, aga sisaldab kõiki seotud dokumente.

4. Selles dialoogiboksis saate teha mitmesuguseid toiminguid. Valige üks või mitu kannet ja seejärel valige üks järgmistest nuppudest.

    - **Kuvaga seotud** – kuvab kõik kliendi maksetöölehe kanded ja päevaraamatu kanded, mis loodi töölehtedes, milles loodi loendis kuvatud dokumendid. Näiteks makse kuvamisel kuvatakse kõik maksetöölehel, milles see loodi, olevad maksed. Arve või makse kuvamisel, mis loodi päevaraamatus, kuvatakse kõik päevaraamatus, milles see loodi, olevad dokumendid. Peale selle kuvatakse kõik nende dokumendiloendiga seotud tasakaalustused. Seotud maksete vaatamise ajal muutub nupu sildiks **Kuva tasakaalustused**. Valige suvand **Kuva tasakaalustused**, et kuvada ainult need kanded, mis kuvati dialoogiboksi **Kuva tasakaalustused** avamisel.
    - **Kuva ajalugu** – kuvatakse kannete tasakaalustamisajalugu. Valige dialoogiboksi sulgemiseks suvand **Sule**.
    - **Kuva raamatupidamine** – kuvatakse kõik valitud dokumentidega seotud kanded. Valige dialoogiboksi sulgemiseks suvand **Sule**.
    - **Ekspordi** – valitud kanded eksporditakse Microsoft Excelisse.
    - **Kannete tasakaalustamine** – see nupp kuvatakse ainult siis, kui valitud algdokument ei olnud täielikult tasakaalustatud. Selle nupu valimisel kuvatakse dialoogiboks **Kannete tasakaalustamine**, kus saate valida tasakaalustamiseks kanded.
    - **Tasakaalustamise tühistamine** – see nupp kuvatakse ainult siis, kui valitud algdokument oli täielikult tasakaalustatud. Selle nupu valimisel kuvatakse dialoogiboks **Tasakaalustamise tühistamine**, kus saate selle dokumendi tasakaalustamised tühistada.

## <a name="global-transactions"></a>Globaalsed kanded

See **Globaalsete kannete** nupp kuvatakse ka loendilehel **Kliendi kanded**. See nupp võimaldab kuvada kõik kliendi kanded kõigis juriidilistes isikutes. Loendilehel **Kliendi kanded** kuvatakse kanded ainult nende juriidiliste isikute puhul, millele kasutajal on tema turbesätete alusel juurdepääs.

Loendilehel kuvatakse kõik nende klientide kanded, kellel on sama osapoole ID mis kliendil, kellega alustasite. Näiteks kui kliendil US-001 ühes juriidilises isikus on sama osapoole ID mis kliendil DE-001 teises juriidilises isikus, kuvatakse kõik kanded mõlema kliendi ID kohta.

Loendilehe **Kliendi kanded** menüüd erinevad olenevalt kande juriidilisest isikust. Näiteks kui mõni funktsioon on saadaval ainult Šveitsi juriidilistele isikutele, kuvatakse selle funktsiooni menüüsuvandid ainult Šveitsi kande valimisel.

Selle funktsiooni kasutamiseks tehke järgmist.

1. Valige suvandid **Müügireskontro \> Kõik kliendid**.
2. Valige klient ja seejärel valige toimingupaani vahekaardil **Klient** grupis **Kanded** suvand **Globaalsed kanded**.

## <a name="more-transaction-filters"></a>Rohkem kannetefiltreid 

Avatud kandeid kuvav filter on asendatud uue filtriga, mis võimaldab kuvada rohkem kannete kombinatsioone. Väljal **Kuva** on saadaval järgmised suvandid.

- **Kõik** – kuvatakse kõik valitud klientide kanded (avatud ja suletud).
- **Suletud** – kuvatakse ainult täielikult tasakaalustatud ja suletud kanded.
- **Avatud** – kuvatakse ainult kanded, mis pole täielikult tasakaalustatud.
- **Avatud, sealhulgas sulgemise kuupäev või pärast kuupäeva** – kuvatakse ainult kanded, mis pole täielikult tasakaalustatud teie määratud kuupäeval või pärast seda. Selle suvandi valimisel saate muuta filtri kõrval kuvatavat kuupäeva. Kanded, mille puhul on suvandi **Viimase tasakaalustuse kuupäev** väärtus teie määratud kuupäeval või pärast seda, kuvatakse loendis isegi siis, kui need kanded on tänase kuupäeva seisuga täielikult tasakaalustatud. Saldo näitab siiski saldot tänase, mitte valitud kuupäeva seisuga.

Valuutateisenduse kannete varjamiseks valige märkeruut **Peida valuuta ümberhindamised**.

## <a name="modify-due-dates-and-discount-dates"></a>Kuupäevade ja allahindluskuupäevade muutmine

Saate värskendada avatud kliendikannete kuupäevi ja allahindluskuupäevi. Väljaandes 8.1 saate lisada loendilehele **Kliendi kanded** tähtajad. Klõpsates loendilehel **Kliendi kanded** tähtaega, saate muuta dialoogiboksis **Tähtaja ja skonto kuupäevade värskendamine** ka tähtaegu, allahindluskuupäevi, maksetingimusi ja skonto tingimusi.

### <a name="activate-the-feature"></a>Funktsiooni aktiveerimine

Loendilehele **Kliendi kanded** tähtaegade lisamiseks ja kande maksesätete muutmiseks dialoogiboksi **Tähtaja ja skonto kuupäevade värskendamine** abil tehke järgmist.

1. Valige suvandid **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.
2. Seadke vahekaardil **Tasakaalustused** suvandi **Kuva tähtaeg ja luba redigeerimine** sätteks **Jah**.
3. Selle funktsiooni lubamiseks on kliendikannetele lisatud uued väljad. Need väljad täidetakse uue kande lõpuleviimisel. Need täidetakse ka siis, kui avate dialoogiboksi **Tähtaja ja skonto kuupäevade värskendamine**. Kui seate suvandi **Kuva tähtaeg ja luba redigeerimine** sätteks **Ei**, kuvatakse dialoogiboks **Makseteabe värskendamine**.  Olemasolevate kannete kohe uuendamiseks valige suvand **Värskenda kõiki olemasolevaid kandeid**. Teise võimalusena väljade täitmiseks ainult uute kannete puhul valige suvand **Jätka värskendamiseta**.

Nüüd lisatakse tähtaeg loendilehele **Kliendi kanded**, nii et teil on kannete tähtaega ja skonto kuupäevi lihtsam muuta.

### <a name="modify-the-payment-settings"></a>Maksesätete muutmine

Loendilehel **Kliendi kanded** kuvatakse kõik kliendi kanded. Kui valite mõne kande tähtaja, avaneb dialoogiboks **Tähtaja ja skonto kuupäevade värskendamine**. Selles dialoogiboksis kuvatakse tähtaja ja skonto arvutuste aluskuupäev, maksetingimused, skonto tingimused ja skonto kuupäevad.

Igal väljal on kandele selle redigeerimisel erinev mõju.

- **Aluskuupäeva redigeerimine** – tähtaega ja allahindluskuupäevi muudetakse nii, et aluskuupäev on dokumendi kuupäev.
- **Tähtaja redigeerimine** – muudetakse ainult tähtaega.
- **Allahindluskuupäevade redigeerimine** – muudetakse ainult allahindluskuupäevi.
- **Maksetingimuste redigeerimine** – tähtaega muudetakse aluskuupäeva ja maksetingimuste alusel.
- **Skonto tingimuste redigeerimine** – skontosid muudetakse aluskuupäeva ja skonto tingimuste alusel.

Kui olete maksesätete redigeerimise lõpetanud, valige muudatuste salvestamiseks käsk **Sule**.
