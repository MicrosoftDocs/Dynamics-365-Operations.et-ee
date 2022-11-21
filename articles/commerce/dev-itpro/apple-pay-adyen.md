---
title: Saate häälestada Oma pay’d koos Mileeniga. Dynamics 365 Commerce
description: See artikkel kirjeldab, kuidas seadistada VäärtusesMeeter Pay koos Omaen-Ga Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: 0949b9d7a4b181605d43956932b4fc095940bd64
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780202"
---
# <a name="set-up-apple-pay-with-adyen-in-dynamics-365-commerce"></a>Saate häälestada Oma pay’d koos Mileeniga. Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

See artikkel kirjeldab, kuidas seadistada VäärtusesMeeter Pay koos Omaen-Ga Microsoft Dynamics 365 Commerce.

## <a name="key-terms"></a>Põhimõisted

| Mõiste | Kirjeldus |
|---|---|
| Raha maks | Tuntud ka nime all Pay "button", Siis On Hinnaaland Pay Puhvri kaudu toetatav makseteenuse pakkumine. See võimaldab kliendikogemust ja integreerimist, mida Microsoft Dynamics toetab 365Andmete Pay Connector. |
| Rahakott | Maksetüüp, mis ei sisalda traditsioonilisi makse omadusi nt panga ID-koodi (BIN) vahemikku ja aegumiskuupäeva, mida kasutatakse krediit- ja deebetkaardi tüüpide eristamiseks. |

Dynamics 365 Commerce Rakendus <a0/& pakub boksist välja integreerimist Gateway Pay’i jaoks, kui kasutatakse Portaal-makselüüsi teenust. The Pay on digitaalse maksmise maksmise meetod, mis kasutab Hinnaalandi makse kaupmehekontot Asendatakseen makseteenusega. Kui see on konfigureeritud, on Button Pay valitav makseviis, mis on osa võrgupoe tellimuse väljaregistreerimise lehest. Button Hinnaaland Pay on esitatud makse suvandina ainult Toetatud Toetatud Seadmete Pay Puhul. Kui kasutajad valivad **Toetatud brauseris või seadmes Pay** Pay, suunatakse nad Pay Service’i, et oma maksed otse lõpule viia. Seejärel tagastatakse need tellimuse lõpetamiseks võrgupoes.

Dynamics 365 Payment ConnectoritSumma maksmise konnektori jaoks kasutatakse lisaks Dynamics 365 Payment Connectorile Puhvrile Puhvrile, et lubadaSummamaksete ja krediitkaardimakseid saidil. Summat saab konfigureerida ka Kauplustes kasutamiseks, kus on Puhvri makseterminalid, mis kasutavad Sisestaja jaoks Dynamics 365 Payment Connectorit koos kassaga Commerce Pos. Sel juhul käsitleb Dynamics 365 Payment Connector for Puhvrit Puhvri makseseadme jagamist terminalis.

## <a name="prerequisites"></a>Eeltingimused

Merchanti kaupmehe konto on äris nõutav Selleks Pay koos Mileeniga. Lisateabe saamiseks Selle kohta, kuidas Seadistada Oma testkliendi alas, vaadake [Näiteks pay Pay’i integreerimist](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#set-up-apple-pay). Lisateavet selle kohta, mida teha, kui olete valmis oma tootmiskeskkonnas otseülekannet tegema, vt Reaalajas [töö](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live).

MaksemeetodLülitus Pay tuleb integreerida ka teie Lülituse kontoga. Sihtotstarbeliseen aitab teil seadistada makseviisi ja võib ka kindlustada, et domeenid, mille jaoks te tunnistuse kasutate, on määratud tunnistusega kasutamiseks.

Rakenduse Commerce headquarters täiustatud täiustatud funktsioonide lipu lubamiseks minge **\>** tööruumide funktsioonihaldusesse ja otsige täiustatud **täiustatud makseteenuse ja makse parendusfunktsiooni.** Valige funktsioon ja seejärel **luba**. Kui funktsioon on lubatud, käivitage **1110 jaotusgraafik**, et teha muudatus kättesaadavaks kõikides kanalites.

## <a name="map-the-apple-pay-payment-method"></a>Saate vastendada Pay Pay makseviisi

Summa maksmine on digitaalse maksmise meetod. Lisateavet maksete vastendamise häälestamise kohtaKriteeriumi Pay jaoks vt Makseteenuse toe [teemast](../wallets.md).

Pay Pay makseviisi vastendamiseks Commerce Headquartersis järgige neid samme.

1. Minge jaemüügi ja **ärikanali häälestuse \> makseviiside \> kaarditüüpidele \>**.
1. Valige **"New** " (uus), et lisada rida Pay Pay’ile ja seadke järgmised väärtused:

    - **ID:** sepay
    - **Elektroonilise makse nimi:** Pay
    - **Tüüp: Väljaminek**
    - **Väljastaja:** Lett

1. Valige **Protsessori vastendamine** protsessori makse vastendamismeetodite **dialoogiboksi** avamiseks. Vastendamata **protsessori maksemeetodite veerus** loetletakse iga saadaoleva konnektori toetatud makseviisid (Puhvrien, PayPal jaPuhvri).
1. Vastendage toetatud **makseviisid, mida soovite nii Dynamics 365 Payment Connectori kui Sumeni** konnektori jaoks (kassas kasutamiseks) **ja Dynamics 365 Payment Connectori JaoksSumma** makseühenduse jaoks (võrgukanali jaoks).
1. Valige iga vastendamisrea **jaoks veerus Vastendamata protsessori makseviisid toetav rida ja seejärel valige lisa,** **et** teisaldada valikud veergu Vastendatud protsessori makseviisid.**·**
1. Valige **OK** ja seejärel valige lehel **Kaarditüübid** suvand **Salvesta**.

## <a name="set-up-the-apple-pay-certificate-for-your-site"></a>Oma saidi jaoks Pay Pay serdi seadistamine

Iga saidi jaoks peate üles laadima domeeniseose faili (mida nimetatakse ka Contoso Pay tunnistuseks), [nagu on kirjeldatud Makse Dokumentatsioonis](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live). Saate kasutada Commerce’i saidi koostajat, et laadida oma saidi domeeniseost üles Meediateeki.

Saidikonstruktoris Pay’i serdi häälestamiseks järgige neid samme.

1. Laadige sert (domeeniseost fail) Omalt [poolt alla](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live).
1. Domeeniseose failile laiendi .txt lisamine.
1. Saidikonstruktoris [laadige](../upload-serve-static-files.md) domeeniseost üles oma saidi meediateeki.
1. Minge URL-idesse **·**.
1. Valige **uus \> Uus URL**.
1. Dialoogiaknas **Uus URL** valige meediateegi **vara**.
1. Sisestage **URL-i** tee väljale URL-i tee (kui seda pole veel sisestatud). Pärast domeeni baas-URL-i sisestage järgmine nõutav String:`<domain>/.well-known/apple-developer-merchantid-domain-association.txt`.
1. Valige **Edasi**. Meediateek näitab kõiki dokumenditüübi (.txt) üleslaaditud **meediumivarasid**.
1. Valige domeeni seosefail, mida tuleb esitada varem määratletud URL-i taotluste korral.
1. Valige **Loo**.

Sel hetkel on teie poolt loodud URL mustandi olekus. Avaldage URL protsessi lõpetamiseks. Faili, millele URL osutab, ei tagastata enne, kui olete URL-i avaldanud.

## <a name="configure-a-commerce-online-store-for-apple-pay"></a>Commerce’i e-poe konfigureerimine Pay Payi jaoks

Commerce’i e-poe konfigureerimiseks Pay Pay’i jaoks järgige neid samme.

1. Minge commerce headquartersi kaupluse ja ärikanalite **võrgupoodidesse \>\>**.
1. Valige oma **saidi võrgupoe kanali jaemüügikanali ID** väärtus.
1. **Lisage** maksekontode kiirkaardile **Dynamics 365 Payment Connector Isnen** Connectori jaoks, kui seda pole veel häälestatud, [järgides Puhvri jaoks Dynamics 365 Payment Connectori häälestamise juhiseid](adyen-connector-setup.md).
1. Kui Puhvri konnektor on konfigureeritud, **·** **valige Lisa, et lisada Dynamics 365 Payment ConnectorSumma konnektor Pay Connectorile.**
1. Sisestage väärtused konnektori kaupmehe atribuutide jaoks.

    | Atribuut               | Kirjeldus | Nõutav | Automaatselt seadistatud | Näidisväärtus |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | Assembleri nimi          | Dynamics 365 Payment Connectori Assembleri nimiSumma maksmise jaoks. | Jah | Jah | Binaarnimi |
    | Teenusekonto ID     | Kaupmehe atribuutide seadistuse kordumatu ID. See identifikaator on tembeldatud maksekannetele ja tuvastab kaupmehe atribuudid, mida allavoolu protsessid (nt arveldamine) peavad kasutama. | Jah | Jah | Guid |
    | Kaupmehe konto ID    | Sisestage kordumatu Diagramm kaupmehe identifikaator. See väärtus esitatakse siis, kui registreerite end Omaen-lepingu alusel sisse, nagu on kirjeldatud [jaotises Nendesse registreerumine](adyen-connector-setup.md#sign-up-with-adyen). | Jah | Nr | Kaupmehe ID-kood |
    | Pilve API võti          | Sisestage Sisselöödetud pilve API võti. Selle võtme hankimiseks järgige API võtme [hankimisjuhiseid](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key). | Jah | Nr | abcdefg |
    | Portaali keskkond    | Sisestage Gateway Environment, et vastendada. Võimalikud väärtused on Katse **ja** Reaalajas **·**. Määrake selle välja väärtuseks Live **ainult** tootmisseadmete ja kannete puhul. | Jah | Jah | Reaalajas |
    | Toetatud valuutad   | Sisestage valuutad, mida konnektor peaks töötlema. Kaardi praegusi stsenaariumedes saab Prognoos toetada lisavaluutasid dünaamilise valuutateisenduse [kaudu](https://www.adyen.com/pos-payments/dynamic-currency-conversion) pärast kande taotluse saatmist makseterminali. Toetatud valuutade loendi kuvamiseks pöörduge Omayen-i toe saamiseks. | Jah | Jah | USD; Eur |
    | Toetatud maksevahendi tüübid | Sisestage maksevahendi tüübid, mida ühendus peaks töötlema. | Jah | Jah | Menüü <a0/& menüü |

1. Kui kaupmehe teave on sisestatud, käivitage **1070 kanali konfiguratsiooni** jaotuse graafiku töö.

## <a name="configure-commerce-pos-for-apple-pay"></a>Commerce POS-i konfigureerimine Pay’i jaoks

Müügikoha konfiguratsioon kasutab riistvaraprofiili EFT-teenuse **välja** konfigureerimist Dynamics 365 Payment Connectori jaoks Puhvrile. Konfigureerige Commerce headquartersis Dynamics 365 Payment Connectori ELEKTROONILISE ülekande (EFT) teenus Sumeni [jaoks, nagu on kirjeldatud Dynamics 365 kassa riistvaraprofiili jaotises](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile).

Veenduge, et lisate **AddPay** maksevahendi tüüpide loendisse väljal Toetatud **maksevahendi tüübid**. Semikoolonite kasutamine (;) maksevahendi tüüpide jaoks loendis.

Puhvri Puhvri vastendamine hõivab Koostelekaartide tüübid, mida kasutab Pos-i terminalisKriteeriumi tasu.

### <a name="configure-content-security-policies-in-site-builder"></a>Sisu turbepoliitikate konfigureerimine saidikonstruktoris

Enne killude või lehtede konfigureerimist, et kasutada Pay Pay’i, peate veenduge, et teie sisu turbepoliitikad (CSPs) on commerce’i saidi koostajas teie saidi jaoks konfigureeritud.

Sisu turbepoliitikate konfigureerimiseks saidikonstruktoris järgige neid samme.

1. Avage **Saidi sätted \> Laiendused**.
1. **Valige** vahekaardil Sisu turbepoliitika suvand Lisa, **·**`https://applepay.cdn-apple.com/jsapi/v1/apple-pay-sdk.js`**et lisada alam-src- ja ühendus-src** **·**-, **raami-src**-, **koodi-src**-, **skripti-src** **- ja stiili-src-jaotistele** rida.
1. Kui olete lõpetanud, valige muudatuste **avaldamine ja** salvestamine.

### <a name="set-up-apple-pay-as-a-checkout-payment-option"></a>Saate häälestada Hinnaaland Payi väljaregistreerimise makse suvandina.

Et seadistada Hinnaaland Pay maksmise suvandina teie saidi (mitte kiir väljaregistreerimise) väljaregistreerimise lehel, järgige neid samme.

1. Minge saidi koostajas fragmentidesse **ja** valige saidi väljaregistreerimise killus.
1. Valige suvand **Redigeeri**.
1. Väljaregistreerimise **sektsiooni ümbrises** valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige **moodul Palka** ja seejärel valige **OK**.
1. Valige käsk **Salvesta**.
1. Valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

**Modulei Pay’i** sätted on moodulisse loodud ja ühendatud Konfigureeritud Dynamics 365 Payment Connectoriga Pay Connectori jaoks, mis on häälestatud Commerce headquartersi võrgukanalile.

### <a name="apple-pay-payment-behavior"></a>Tasu maksmise käitumine

**Hinnaalanduse maksenupp** kuvatakse ainult Toetatud Makseteenuse tasuseadmetel (iPhones, iPhones, iPhones ja Browsers, mis toetavad Seda tasu). Kui kasutaja ei kasuta ühte neist seadmetest, **on Vaates** peidetud Button The Pay payment.

Kui kasutaja valib nupuSumma **maksmine**, kuvatakse **Dialoogiboks Hinnaalandi** tasu. Seal saab kasutaja autentida oma Windowsi makseseadme või brauseri suhtes. Dialoogiaknas **Hinnaaland Pay** kuvatakse tellimuse summa kokkuvõte ja makseviis, mille kasutaja on konfigureerinud oma Tagasimaksmise vastu. Kasutaja saab need üksikasjad üle vaadata ja seejärel makse **lõpule viimiseks** valida. Pärast makse lõpule viimist suunatakse kasutaja **lõpuleviidud** kande üksikasjaliku tellimuse kokkuvõttega saidile.

## <a name="additional-resources"></a>Lisaressursid

[Maksete KKK](payments-retail.md)

[Maksmismoodul](../add-checkout-module.md)

[Maksemoodul](../payment-module.md)
