---
title: Ostureskontro sisestused
description: See teema kirjeldab sisestuste konfigureerimisviise Ostureskontros ja pakub näiteid sisestuskonfiguratsioonidest.
author: rachel-profitt
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPosting, VendPaymMode, VendCashDiscount, MarkupTable\_Vend, VendPaymFee
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb3ebad31c9f41e405b9fc31a0f71df05fa1cc60
ms.sourcegitcommit: 10b85a09e8a550155a69aa2a8877a7c88b887242
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/20/2022
ms.locfileid: "8014481"
---
# <a name="accounts-payable-posting"></a>Ostureskontro sisestamine

[!include [banner](../includes/banner.md)]

Ostureskontro mooduli **esmane** sisestusprofiil on hankija sisestusreeglid. See sisestusreegliga määratletakse summakonto, mida kasutatakse hankijasaldode pearaamatusse sisestamisel. Summakonto on põhikonto. Seda nimetatakse ka ostureskontro kaubanduskontoks.

Lisateavet vt hankija [sisestusreeglitest](../accounts-payable/vendor-posting-profiles.md).

Ostureskontros on lisaks hankija sisestusreeglitele saadaval mitu sisestuskonfiguratsiooni. Järgmised jaotised annavad lisateavet nende teiste sisestuskonfiguratsioonide kohta.

## <a name="methods-of-payment-posting-accounts"></a>Makseviiside sisestuskontod

Makseviisid määratlevad, kuidas makse pearaamatusse sisestatakse. Samuti kontrollivad nad makseväljundi käitumist. Tavaliselt luuakse üks makseviis iga maksetüübi kohta, mida teie organisatsioon teeb (nt sularaha, tšekk, krediitkaart, rahakorraldus ja kreedit).

Makseviiside lehe (Ostureskontro > Makseseadistus > Makseviisid) jaotise Üldine väljad kontrollivad, kuidas makse **pearaamatusse** **·** **·** **sisestatakse**. Peate esmalt valima väärtuse väljal **Konto** tüüp. Valitud kontotüüp juhib maksekonto **välja** käitumist. Soovitame teil väljal Konto tüüp valida pank ja **seejärel valida pangakonto** **·** **maksekonto** väljal. Selline lähenemine on kasulik, et süsteem sisestab makse panga alamdgerisse, mis toetab vastavusseviimist ja muid sularahaga seotud protsesse. Järgnev tabel näitab näidet sisestusreeglite konfiguratsiooni kohta, kui kasutate moodulit **Sularaha ja panga** haldus.

| Sisestamistüüp | Konto tüüp | Maksekonto nime näide | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Kirjeldus |
|--------------|--------------|------------------------------|--------------|---------------|------------------|-------------|
| Pank | Pank | Ameerika Pank | Varaga seotud pangakonto | Debiteeri | Ei | Iga makseviisi puhul sisestage põhikonto **maksekonto** väljale. |

Kui te ei plaani kasutada sularaha- ja pangahaldust, peaksite väljal Konto tüüp valima pearaamatu ja seejärel valima **põhikonto** **·** **maksekonto** väljal. Järgmises tabelis on toodud sisestusreeglite konfiguratsiooni näide, kui te ei **kasuta sularaha ja panga** haldust.

| Sisestamistüüp | Konto tüüp |Maksekonto näide | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Kirjeldus |
|--------------|--------------|------------------------|--------------|---------------|------------------|-------------|
| Ledger | Ledger | 100100: Ameerika Pank | Vara | Debiteeri | Ei | Iga makseviisi puhul sisestage põhikonto **maksekonto** väljale. |

## <a name="bridging-accounts"></a>Vaheldamiskontod

Vaheldamine on kaheastmeline protsess, mida kasutatakse maksete sisestamisel. See on valikuline funktsioon, mida saab kasutada näiteks nullsaldoga pangakontodega. See võib kindlustada sujuvama ja õigeaegselt panga vastavusseviimise protsessi. Esimeses astmes sisestatakse makse ajutisele kontole (ajutine konto). Teises sammus tühistatakse sisestatud kirje ja sisestatakse pangakontole, kui makse tühjendab panga. Järgnev tabel näitab näidet sisestusreeglite konfiguratsiooni kohta ajutiselt sisestamiseks.

| Sisestamistüüp | Põhikonto näide | Põhikonto nime näide | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Kirjeldus |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Pearaamatu tööleht | 130725 | Laekumata raha | Kohustus | Debiteeri | Jah | Iga makseviisi puhul sisestage põhikonto väljale **Bridging** account. |

Lisateavet vt "Sildmaksete [seadistamine ja protsess".](../accounts-receivable/set-up-and-process-bridged-payments.md)

## <a name="customer-cash-discounts-posting-accounts"></a>Kliendi skontode sisestuskontod

Kui teie organisatsioon saab hankijalt skontosid kiirmakse eest, peate konfigureerima skonto koodid ja määrama, kuidas allahindlused pearaamatusse sisestada. Kliendi skonto sisestamiseks kasutatava põhikonto määratlemiseks on saadaval mitu võimalust.

Lisateavet vt [skontolt.](../cash-bank-management/cash-discounts.md)

## <a name="payment-fee-posting-accounts"></a>Maksetasu sisestamise kontod

Maksetasud lasevad teil automaatselt lisada hankija maksele tasu, kui rakendub tingimuste kogum. Maksetasud saab maksta hankijale või need saab sisestada teie pangakontole kuluna. Järgmisena on toodud mõned näited.

- Hankija maksab krediitkaardiga maksmisel 3 protsenti makse kogusummast.
- Teie pangaarved $1.00 tasu iga töödeldav pangaülekande eest ja tasu on kuludesse kanda.

Hankija maksetasu konfigureerimisel, kui seate välja Tasu väärtuseks Hankija, ei ole põhikonto väli saadaval ja süsteem kasutab hankija sisestusreeglit **tasu** **·** **sisestamiseks**. Kui seate välja Tasu väärtuseks Pearaamat, tuleb väli Põhikonto **seada** **·** **põhikontole**, kuhu maksetasu sisestatakse. Tavaliselt on selleks põhikontoks kulukonto. Järgmine tabel näitab näidet maksetasu sisestamise sisestusreeglite konfiguratsiooni kohta.

| Sisestamistüüp | Põhikonto näide | Põhikonto nime näide | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Kirjeldus |
|--------------|----------------------|---------------------------|--------------|----------------|------------------|-------------|
| Pearaamatu tööleht | 618190 | Pangatasu kulu | Kulu | Debiteeri | Ei | Kui **väljal** Tasu on valitud **pearaamat**, valige see konto **maksetasu** lehe väljal **Põhikonto**. |

Lisateavet vt [Hankija käitluslõivude määratlemine](../accounts-payable/tasks/define-vendor-payment-fees.md).

## <a name="charges-code-posting-accounts"></a>Kulude koodi sisestamise kontod

Kui peate lisaks rea kaupadele jälgima ostusummasid, saate kasutada kulude koode. Näiteks võib teie tarnija nõuda teilt veo- ja käsitsemistasu või see võib kuluda mõned veo- ja käsitsemistasud ettevõttesiseselt. Saate määrata, kas need summad sisestatakse kulukontodele või lisatakse kaupade maksumusele.

Kulude koodid saate luua müügireskontro ja ostureskontro jaoks. Tasude koodi konfigureerimisel peate määratlema sisestamise. Sisestamine kontrollib nii deebetkontot kui ka kreeditkontot. Kui loote kulude koode, saate valida sisestustüübi, mida kasutatakse iga kulukoodi puhul. Järgmises tabelis on toodud tavalised ostureskontro tasukoodide näited lehel **Tasukoodid**.

| Sisestamistüüp | Põhikonto näide | Põhikonto nime näide | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Kirjeldus |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Ostutasu | Jätke väli tühjaks. | Pole kohaldatav | Kaup | Debiteeri | Ei | **Näide kauba ostutasu kohta:** </p><ul><li>**Deebeti tüübi** väli = **Kaup**</li><li>  **Kreediti** tüübi väli = **Klient/Hankija**.</li><li> Kauba sisestamine kasutab lao sisestusreeglite põhikontot. |
| Tellimus, veos | 600120 | Veos sisse | Tulu | Debiteeri | Ei | **Näide hankijale makstud veose kohta:** </p><ul><li>**Deebetitüübi** väli = **pearaamatukonto**</li><li> **Kreediti** tüübi väli = **Klient/Hankija** |
| Tagasimakse\* | 503160 | Hankija tagasimakse (hankija COGS)| Kulu | Krediit | Ei | **Hankija tagasimakse näide:**</p><ul><li>**Deebeti** tüübi väli = **Klient/Hankija**</li><li>**Kreediti** tüübi väli = **pearaamatukonto** |

\* Tagasimakse näite puhul kasutatakse sisestamist ainult juhul, kui kulude kood lisatakse ostutellimuse päisele või reale. Täpsemad tagasimaksefunktsioonid, mis on Dynamics 365 Supply Chain Management Microsoftis saadaval, tagab tagasimaksete juhtimise ja automatiseerimise. Lisateavet vt hankija [tagasimaksetest](../../supply-chain//procurement/vendor-rebates.md).

Eelmises tabelis on toodud kolm tüüpilist sisestustüüpide näidet, mida saab kulude koodide puhul kasutada. Seda tuleks kasutada juhise ja valimi valikuna. See ei anna põhjalikku loendit võimalikest kombinatsioonidest või sisestustüüpidest, mida saab kasutada.

Lisateavet vt teemast Kulude [koodi](../accounts-receivable/create-charges-codes.md) loomine.
