---
title: Väljaregistreerimise mooduli tõrke viitekoodid
description: See artikkel kirjeldab väljaregistreerimise mooduli tõrke viitekoode, mida näidatakse kasutajasuunas veateadetes moodulis Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 10/20/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: cd8269a71e56f23dbe3782ec3ffc69ec3ea6b151
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709373"
---
# <a name="checkout-module-error-reference-codes"></a>Väljaregistreerimise mooduli tõrke viitekoodid

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

See artikkel kirjeldab väljaregistreerimise mooduli tõrkekoode, mida näidatakse kasutajasuunas veateadetes moodulis Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce on juurutanud standardiseeritud tõrkeviited, mida saab võrgu klientidele esitatud võrgukanali väljaregistreerimise tõrgetesse kaasata. Rakenduse Commerce versiooni 10.0.31 ja hilisemate teadete väljaregistreerimise moodulis sisaldavad tõrkekoode ja ei näita võrgukliendile mittevajalikku teavet. Tõrkekoodid viitavad tõrkele, mis on selles artiklis üksikasjalikud.

Olenevalt ilmnenud tõrkest sisaldab selle artikli tabel järgmisi üksikasju:

- Tõrke põhjustanud tingimuse kirjeldus või täiendavad üksikasjad
- Teave keskkonna või maksekonnektori konfiguratsioonide kaalumiseks
- Teave, mida saab tugijuhtumi puhul kasutada, kui on vaja lisaabi

## <a name="checkout-module-error-reference-codes"></a>Väljaregistreerimise mooduli tõrke viitekoodid

Kasutage järgmist tabelit, et saada rohkem üksikasju tõrkekoodi viidete kohta, mida pakub klient või mis on võrgupoes kogenud.

| Tõrkekood | Dynamics-korrelatsiooniga seotud tõrkekood | Tõrke kirjeldus |
| ---------- | ------------------------------ | ----------------- |
| CcR001 (koopia)     | Microsoft\_ Dynamics\_ Commerce Runtime\_ ei\_ saaToAuthorizePaymentCardTypeMissingOrNotSupported. | Makset ei saanud autoriseerida. Kaarditüübi ID tabelis **TokenizedPaymentCard** puudub või antud kaarditüübi ID-d ei toetata. |
| CcR002     | Microsoft\_ Dynamics\_ Commerce’i\_ käitusaeg\_ ei saatoAuthorizePayment | Vähenenud. Makset ei saanud autoriseerida. |
| CcR003     | Microsoft\_ Dynamics\_ Commerce Runtime\_\_ EiToAuthorizePaymentCardAdditionalContextRequired | Makset ei saanud autoriseerida. Kliendilt nõutav lisateave. |
| CcR004     | Microsoft\_ Dynamics\_ Commerce’i\_ käitusaeg\_ ei saaToRetrieveCardPaymentAcceptResult | Kahjuks ilmnes tõrge. Kaardimakse aktsepteerimise tulemust ei õnnestunud saada. Proovige uuesti või pöörduge oma süsteemiadministraatori poole. |
| CCR005 (koopia)     | Microsoft\_ Dynamics\_ Commerce’i\_ käitusaja\_ makseRequiresMerchantProperties | Makset ei saa puuduva kaupmehe makse atribuutide tõttu teha. Pöörduge oma süsteemiadministraatori poole. |
| CcR006     | Microsoft\_ Dynamics\_ Commerce’i\_ käitusaja\_ invalidPaymentRequest | Toimingu jaoks ei saa maksevahendi teenust tuua. Saate kontrollida valitud maksevahendi tüübi makseviisi seadistust. |
| CcR007     | Microsoft\_ Dynamics\_ Commerce’i\_ käitusaja\_ MultipleCustomerAccountPaymentsNotAllowed | Kliendikonto makse on juba rakendatud ja kande kohta on lubatud ainult üks makse. |
| CcR008     | Microsoft\_ Dynamics\_ Commerce’i\_ käitusaja\_ CustomerAccountLimitSignDifferentFromAmountDue | Kliendi konto limiit erineb summast, mis tuleb tasuda. Proovige muud makseviisi või võtke abi saamiseks ühendust klienditoega. |
| CCR009     | Microsoft\_ Dynamics\_ Commerce’i\_ käitusaja\_ CustomerAccountPaymentExceedsTotalAmountForCarryOutAndReturnItems | Kliendi konto makse ületab loetletud kaupade kogumakse. Proovige hiljem uuesti või võtke abi saamiseks ühendust klienditoega. |
| CcR010     | Microsoft\_ Dynamics\_ Commerce’i\_ käitusaja\_ makseusingUnauthorizedAccount | Kliendikonto makse nõuab maksevahendi real oma kontot või ühtivate arvekontot. |
| CcR011     | Microsoft\_ Dynamics\_ Commerce Runtime\_\_ CustomerAccountPaymentExceedsCustomerAccountFloorLimit | Kliendikonto makset ei saa praegu töödelda – piirväärtus on ületatud. |
| CcR012     | Microsoft\_ Dynamics\_ Commerce’i\_ käitusaja\_ customerAccountPaymentForCustomerWithoutAllowOnAccount | Sellel kliendil ei ole lubatud ettemaksta. |
| CcR013     | Microsoft\_ Dynamics\_ Commerce’i\_ käitusaeg\_ ei saatoCancelPayment | Kahjuks ilmnes tõrge. Makset ei saanud tühistada. Proovi uuesti. |
| CcR014     | Microsoft\_ Dynamics\_ Commerce’i\_ käitusaeg\_ ei SaaToReadCardTokenInfo | Makse töötlemisel ilmnes tõrge. Proovige hiljem uuesti. |
| CcR015     | Microsoft\_ Dynamics\_ Commerce Runtime\_\_ NotEnoughRewardPoints | Kliendikaardi maksesumma ületab kandes kasutatava kliendikaardi jaoks lubatud piirmäära. |
| CcR016     | Microsoft\_ Dynamics\_ Commerce’i\_ käitusaja\_ tagasimakseAmountMoreThanAllowed | Kliendikaardi tagasimakse summa ületab kandes kasutatava kliendikaardi jaoks lubatud piirmäära. |
| CcR017     | Microsoft\_ Dynamics\_ Commerce’i\_ käitusaja\_ invalidLoyaltyCardNumber | Kliendikaardi numbrit ei leitud. Aktiveerige kliendikaardi number või sisestage muu kaardinumber ja proovige uuesti. |
| CcR018     | Microsoft\_ Dynamics\_ Commerce Runtime\_\_ BlockedLoyaltyCard | Kliendikaardi number ei ole saadaval. Sisestage muu kaardinumber ja proovige uuesti. |
| CcR019     | Microsoft\_ Dynamics\_ Commerce’i\_ käitusaja\_ noTenderLoyaltyCard | Sellel kliendikaardil ei ole õigus selle kande boonuspunktide lunastamiseks. |
| CCR020     | Microsoft\_ Dynamics\_ Commerce Runtime’i\_\_ kinkekaartCurrencyMismatch | Kinkekaardi numbris ilmnes tõrge. Proovige teist kinkekaarti või võtke abi saamiseks ühendust klienditoega. |
| CcR021     | Microsoft\_ Dynamics\_ Commerce’i\_ käitusaja\_ makseAmountExceedsGiftBalance | Summa ületab kinkekaardi saldot. Sisestage muu summa ja proovige uuesti. |
| CcR022     | Microsoft\_ Dynamics\_ Commerce Runtime\_\_ NoMoreThanOneLoyaltyTender | Kanne ei saa sisaldada rohkem kui üht kliendikaardi makserida. |
| CcR023     | Microsoft\_ Dynamics\_ Commerce’i\_ käitusaja\_ makseAlreadyVoided | Makseteave on kas puuduv teave või vale. Kontrollige makseteavet ja proovige uuesti. |
| CcR024     | Microsoft\_ Dynamics\_ Commerce’i\_ käitusaja\_ pettuserisk | Tellimust ei saa praegu töödelda. Proovige hiljem uuesti. |
| CcR025     | Eest lõpu ajalõpp väljaregistreerimise API jaoks | Eesmise lõppoperatsiooni aeg on lõppemas. Kinnitage, kas tellimus on peakontoris töödeldud Dynamics 365 Commerce. |
| CcR026     | Algne autoriseeritud summa muudetud | Tellimuse summa on muutunud makselüüsiga töödeldud algsest autoriseerimissummast. Selle põhjuseks võib olla kupongi, kampaaniahinna või müügi aegumine ajas. |
| CcR027     | Microsoft\_ Dynamics\_ Commerce Runtime\_\_ InvalidCartVersion | Makse töötlemisel ilmnes tõrge. Ostukorvi API-le esitatud viitel on oodatust erinev viide (ärgitav vastuolu väljaregistreerimise protsessi ajal). |
| CcR028     | Microsoft\_ Dynamics\_ Commerce’i\_ käitusaja\_ puuduvRequiredCartTenderLines | Katsel kasutatud makseviisis ilmnes tõrge. Kontosätete läbivaatamiseks pöörduge tugiteenuste poole või proovige muu makseviisiga uuesti. |

## <a name="additional-resources"></a>Lisaressursid

[Maksete KKK](dev-itpro/payments-retail.md)

[Maksmismoodul](add-checkout-module.md)

[Makse moodul](payment-module.md)
