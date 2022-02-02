---
title: Müügireskontro sisestamine
description: See teema kirjeldab sisestuste konfigureerimisviise Müügireskontros ja pakub näiteid sisestuskonfiguratsioonidest.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustPaymMode, CustCashDiscount, CommissionPosting, MarkupTable\_Cust, CustPaymFee
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e664c42461e4f2995cac9a747d85d0f2a0fdf85
ms.sourcegitcommit: 96f936267d3f314f06da6ce6f809eba2ec3b205f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/24/2022
ms.locfileid: "8021587"
---
# <a name="accounts-receivable-posting"></a>Müügireskontro sisestamine

[!include [banner](../includes/banner.md)]

Müügireskontro mooduli **esmaseks** sisestusreegliks on kliendi sisestusreeglid. See sisestusrikkumine määratleb summakonto, mida kasutatakse kliendi saldode pearaamatusse sisestamisel. Summakonto on põhikonto. Seda nimetatakse ka Müügireskontro kaubanduskontoks.

Lisateavet leiate teemast [Kliendi sisetamise profiil](../accounts-receivable/customer-posting-profiles.md).

Müügireskontros on saadaval kliendi sisestusreeglite kõrval mitu sisestuskonfiguratsiooni. Järgmised jaotised annavad lisateavet nende teiste sisestuskonfiguratsioonide kohta.

## <a name="posting-accounts-for-methods-of-payment"></a>Makseviiside sisestuskontod

Makseviisid määratlevad, kuidas makse pearaamatusse sisestatakse. Samuti kontrollivad nad makseväljundi käitumist. Tavaliselt luuakse üks makseviis iga maksetüübi kohta, mida teie organisatsioon aktsepteerib (nt sularaha, tšekk, krediitkaart, rahakorraldus ja rahaülekanne).

Kiirkaardi Üldine jaotises Sisestamine olevad väljad kontrollivad, **kuidas makse** **pearaamatusse** sisestatakse. Peate esmalt valima väärtuse väljal **Konto** tüüp. Valitud kontotüüp juhib maksekonto **välja** käitumist. Soovitame teil väljal Konto tüüp valida pank ja **seejärel valida pangakonto** **·** **maksekonto** väljal. Selline lähenemine on kasulik, et süsteem sisestab makse panga alamdgerisse, mis toetab vastavusseviimist ja muid sularahaga seotud protsesse. Järgnev tabel näitab näidet sisestusreeglite konfiguratsiooni kohta, kui kasutate moodulit **Sularaha ja panga** haldus.

| Sisestamistüüp | Konto tüüp | Põhikonto nime näide | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Kirjeldus |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Pank | Pank | Contoso pank | Varaga seotud pangakonto | Krediit | Ei | Iga makseviisi puhul sisestage põhikonto **maksekonto** väljale. |

Kui te ei plaani kasutada sularaha- ja pangahaldust, peaksite väljal Konto tüüp valima pearaamatu ja valima seejärel maksekonto **väljal** **·** **põhikonto**. Järgmine tabel näitab näidet sisestusreeglite konfiguratsiooni kohta, kui te ei kasuta sularaha ja panga haldust.

| Sisestamistüüp | Konto tüüp | Põhikonto nime näide | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Kirjeldus |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Ledger | Ledger | 100100: Contoso pank | Vara | Krediit | Ei | Iga makseviisi puhul sisestage põhikonto **maksekonto** väljale. |

## <a name="bridging-accounts"></a>Vaheldamiskontod

Vaheldamine on kaheastmeline protsess, mida kasutatakse maksete sisestamisel. See on valikuline funktsioon, mida saab kasutada näiteks nullsaldoga pangakontodega. See võib kindlustada sujuvama ja õigeaegselt panga vastavusseviimise protsessi. Esimeses astmes sisestatakse makse ajutisele kontole (ajutine konto). Teises sammus tühistatakse sisestatud kirje ja sisestatakse pangakontole, kui makse tühjendab panga. Järgnev tabel näitab näidet sisestusreeglite konfiguratsiooni kohta ajutiselt sisestamiseks.

| Sisestamistüüp | Põhikonto näide | Põhikonto nime näide | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Kirjeldus |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Pearaamatu tööleht | 130725 | Laekumata raha | Kohustus | Debiteeri | Jah | Iga makseviisi puhul sisestage põhikonto väljale **Bridging** account. |

Lisateavet vt "Sildmaksete [seadistamine ja protsess".](../accounts-receivable/set-up-and-process-bridged-payments.md)

## <a name="posting-accounts-for-customer-cash-discounts"></a>Kliendi skontode sisestamine skontodele

Kui teie organisatsioon pakub klientidele skontosid kiirmakse eest, peate konfigureerima skonto koodid ja määrama, kuidas allahindlused pearaamatusse sisestada. Kliendi skonto sisestamiseks kasutatava põhikonto määratlemiseks on saadaval mitu võimalust.

Lisateavet vt [skontolt.](../cash-bank-management/cash-discounts.md)

## <a name="posting-accounts-for-payment-fees"></a>Maksetasude kontode sisestamine

Maksetasud lasevad teil automaatselt lisada tasu kliendi maksele, kui rakendub tingimuste kogum. Maksetasud saab kliendilt nõuda või need saab sisestada teie pangakontole kuluna. Järgmisena on toodud mõned näited.

- Te maksate klientidelt 3 protsenti makse kogusummast, kui nad maksavad krediitkaardiga.
- Teie pangaarved $1.00 tasu iga töödeldav pangaülekande eest ja ülekandetasu on kuluks esitatud.

Kliendi maksetasu konfigureerimisel, kui seate välja Tasu väärtuseks Klient, ei ole põhikonto väli saadaval ja süsteem kasutab tasu sisestamiseks **kliendi** **·** **sisestusreeglit**. Kui seate välja Tasu väärtuseks Pearaamat, tuleb väli Põhikonto **seada** **·** **põhikontole**, kuhu maksetasu sisestatakse. Tavaliselt on selleks põhikontoks kulukonto. Järgmine tabel näitab näidet maksetasu sisestamise sisestusreeglite konfiguratsiooni kohta.

| Sisestamistüüp | Põhikonto näide | Põhikonto nime näide | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Kirjeldus |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Pearaamatu tööleht | 618190 | Pangatasu kulu | Kulu | Debiteeri | Ei |  Kui **väljal** Tasu on valitud **pearaamat**, valige maksetasu **jaoks see konto väljal** Põhikonto. |

Lisateabe saamiseks vt [Kliendi käitluslõivude loomine](../accounts-receivable/tasks/establish-customer-payment-fees.md).

## <a name="posting-accounts-for-charges-codes"></a>Kulude koodide sisestuskontod

Kui peate lisaks rea kaupadele jälgima ka müügisummasid, saate kasutada kulude koode. Näiteks võite nõuda oma klientidelt veo- ja käsitsemistasu või võite kuluda mõned veo- ja käsitsemistasud ettevõttesiseselt. Saate määrata, kas need summad sisestatakse kulukontodele või lisatakse kaupade maksumusele.

Kulude koodid saate luua müügireskontro ja ostureskontro jaoks. Tasude koodi konfigureerimisel peate määratlema sisestamise. Sisestamine kontrollib nii deebetkontot kui ka kreeditkontot. Iga teie valitud lisakulude koodi puhul saate valida kasutatava sisestustüübi. Järgmises tabelis on toodud müügireskontro kulude koodide tavalised näited.

| Sisestamistüüp | Põhikonto näide | Põhikonto nime näide | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Kirjeldus |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Maksetasu | 411400 | Tulu – Tasud | Tulu | Krediit | Ei | **Näide mitterahaliste vahendite kohta:** kliendi deebeti-/hankija- ja pearaamatu kreeditkonto |
| Tellimus, veos | 403500 | Tulu – Veos | Tulu | Krediit | Ei | **Kliendi esitatud veose näide: kliendi** deebeti-/hankija- ja pearaamatu kreeditkonto |
| Tagasimakse\* | 403200 | Allahindlus | Tulu | Debiteeri | Ei | **Kliendi tagasimakse näide: pearaamatu** deebetkonto ja kreediti klient/hankija |

\* Tagasimakse näite puhul kasutatakse sisestamist ainult juhul, kui kulude kood lisatakse ostutellimuse päisele või reale. Täpsemad tagasimaksefunktsioonid, mis on Dynamics 365 Supply Chain Management Microsoftis saadaval, tagab tagasimaksete juhtimise ja automatiseerimise. Lisateavet vt kliendi [tagasimaksetest](../../supply-chain/sales-marketing/tasks/process-customer-rebates.md).

Eelmises tabelis on toodud kolm tüüpilist sisestustüüpide näidet, mida saab kulude koodide puhul kasutada. Seda tuleks kasutada juhise ja näidisna. See ei anna põhjalikku loendit võimalikest kombinatsioonidest või sisestustüüpidest, mida saab kasutada.

Lisateavet vt teemast Kulude [koodi](../accounts-receivable/create-charges-codes.md) loomine.

## <a name="posting-accounts-for-commissions"></a>Komisjonitasu sisestuskontod

Vajadusel saate süsteemi konfigureerida arvutama komisjonitasusid antud müügitellimuse müügiesindaja või müügiesindajate grupi jaoks. Selle funktsiooni lubamisel peate konfigureerima komisjonitasu arvutamiseks kasutatava sisestuskonto. Seda konfigureeritakse müügi- ja **turundusmooduli** **komisjonitasu sisestamise** lehel.

Lisateabe saamiseks vt müügi [komisjonitasu reeglite](../../supply-chain/sales-marketing/tasks/set-up-sales-commission-rules.md) seadistamist.
