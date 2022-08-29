---
title: Äri hinnakujunduse API-d
description: See artikkel kirjeldab erinevaid hinnakujunduse API-sid, mida pakub Microsoft Dynamics 365 Commerce hinnakujundusmootor.
author: boycez
ms.date: 08/10/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-15
ms.openlocfilehash: d694c44f6987fbf2a360869d2fb2a2fbaf0d2e4d
ms.sourcegitcommit: 924dbcdc6b03f6a7ae3a07378ec405fd15c7e359
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2022
ms.locfileid: "9293648"
---
# <a name="commerce-pricing-apis"></a>Äri hinnakujunduse API-d

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab erinevaid hinnakujunduse API-sid, mida pakub Microsoft Dynamics 365 Commerce hinnakujundusmootor.

Hinnakujunduse Dynamics 365 Commerce mootor pakub järgmisi jaemüügiserveri API-sid, mida saavad tarbida välised rakendused, et toetada erinevaid hinnastsenaariume:

- **GetActivePrices** – see API saab toote arvutatud hinna, sh lihtsad allahindlused.
- **CalculateSalesDocument** – see API arvutab toodete hinnad ja allahindlused antud kogustes, kui need ostetakse koos.
- **GetAvailablePromotions** – see API saab ostukorvi toodetele kehtivaid allahindlusi. 
- **AddCoupons** – see API lisab ostukorvi kuponge.
- **RemoveCoupons** – see API eemaldab ostukorvist kupongid.

Lisateavet jaemüügiserveri API-de tarbimise kohta välistes rakendustes vt [jaemüügiserveri API-de tarbimine välisrakendustes](dev-itpro/consume-retail-server-api.md).

## <a name="getactiveprices"></a>GetActivePrices

GetActivePrices *API* tutvustati Commerce’i versiooni 10.0.4 väljalaskes. See API saab toote arvutatud hinna, sh lihtsad allahindlused. See ei arvuta multiallahindlusi ja eeldab, et igale API taotluse tootele on kogus 1. See API võib sisestusina võtta ka toodete loendi ja teha hulgipäringuid üksikute toodete hinna kohta.

GetActivePrices *API* toetab töötaja **, kliendi**, **anonüümse ja** **rakenduse** äri **rolle**.

*GetActivePrices* API peamine kasutusjuhtum on toote üksikasjade leht (PDP), kus jaemüüjad soovivad esitada tootele parimat hinda, sh efektiivseid allahindlusi.

Järgmine tabel näitab sisendparameetreid *GetActivePrices* API jaoks.

| Nimi                                    | Alamnimi | Tüüp | Kohustuslik/valikuline | Kirjeldus |
|-----------------------------------------|----------|------|-------------------|-------------|
| projectDomain                           | | ProjektsioonDomain | Nõutav | |
|                                         | Kanali ID | Pikk | Nõutav | |
|                                         | CatalogId | Pikk | Nõutav | |
| ProductIds (toote ID-d)                              | | IEnumerable\<long\> | Nõutav | Toodete loend, mille jaoks hinnad arvutada |
| activeDate (aktiivne)                              | | Välja DateTimeOffset | Nõutav | Hindade arvutamise kuupäev. |
| Kliendi ID                              | | string | Valikuline | Kliendikood. |
| All kuuluvusLoyaltyTiers                 | | IEnumerable\<AffiliationLoyaltyTier\> | Valikuline | All kuuluvus ja püsikliendijärgud. |
|                                         | Allutuse ID | Pikk | Nõutav | Allutuse ID. |
|                                         | LoyaltyTierId | Pikk | Valikuline | Püsikliendi järgu ID. |
| includeSimpleDiscountsInContextualPrice | | Bool | Valikuline | Seadistage see parameeter **tõeseks**, et kaasata lihtsad allahindlused hinnakujunduse arvutusse. Vaikeväärtus on **väär**. |
| kaasavariantPriceRange                | | Bool | Valikuline | Seadistage see parameeter **tõeseks**, et saada põhitoote kõigi variantide seast miinimum- ja maksimumhinnad. Vaikeväärtus on **väär**. |
| Kaasaa tuleb kasutada järgmisi summasid:PricesAndDiscounts     | | Bool | Valikuline | Seadistage see parameeter soovitud **õigeks**, et saada saavutatud hinnad ja allahindlused. Vaikeväärtus on **väär**. |

**Taotluse näidiskogum**

```json
{
    "projectDomain": 
    {
        "ChannelId": 5637144592,
        "CatalogId": 0
    },
    "productIds": 
    [
        68719489871
    ],
    "activeDate": "2022-06-20T14:40:05.873+08:00",
    "includeSimpleDiscountsInContextualPrice": true,
    "includeVariantPriceRange": false
}
```

**Vastuse näidiskogum**

```json
{
    "value": 
    [
        {
            "ProductId": 68719489871,
            "ListingId": 68719489871,
            "BasePrice": 0,
            "TradeAgreementPrice": 0,
            "AdjustedPrice": 0,
            "MaxVariantPrice": 0,
            "MinVariantPrice": 0,
            "CustomerContextualPrice": 0,
            "DiscountAmount": 0,
            "CurrencyCode": "USD",
            "ItemId": "82000",
            "InventoryDimensionId": null,
            "UnitOfMeasure": "ea",
            "ValidFrom": "2022-06-20T01:40:05.873-05:00",
            "ProductLookupId": 0,
            "ChannelId": 5637144592,
            "CatalogId": 0,
            "SalesAgreementPrice": 0,
            "PriceSourceTypeValue": 1,
            "DiscountLines": [],
            "AttainablePriceLines": [],
        }
    ]
}
```

## <a name="calculatesalesdocument"></a>ArvutabSalesDocumenti

CalculateSalesDocument *API* tutvustati Commerce’i versiooni 10.0.25 väljalaskes. See API arvutab hinnad ja allahindlused toodetele antud koguses, kui need ostetakse tellimusel koos. Api CalculateSalesDocument *API* hinnakujunduse kalkulatsioon võtab arvesse nii ühe rea allahindlusi kui ka multiallahindlusi.

*CalculateSalesDocument* API peamine kasutusjuhtum on hinnakujunduse arvutus stsenaariumites, kus ostukorvi kogukontekst ei püsi (nt müügipakkumised). Seda kasutusjuhtumit saab kasutada ka müügikohas (POS) ja äri e-kaubanduses. Madalam koguhind, kui ostukorvi kaubad arvutatakse komplektina (nt eraldi kogumite, lingitud või soovitatud toodete puhul või tooted, mis on juba ostukorvi lisatud) võivad kliente ostukorvi tooteid lisada.

CalculateSalesDocument API nii taotluse kui ka vastuse *andmemudel* on **Ostukorv**. Kuid selle API kontekstis on andmemudeli nimi **SalesDocument**. Kuna enamik atribuute on valikulised ja ainult mõned neist mõjutavad hinnakujunduse arvutust, kuvatakse järgmises tabelis ainult hinnakujundusega seotud väljad. Me ei soovita API-nõudesse kaasata muid välju.

*CalculateSalesDocument API ulatus* on ainult hindade ja allahindluste arvutamine. Makse ja tasusid ei kaasata.

Järgmine tabel näitab sisendparameetreid objektis nimega **salesDocument**.

| Nimi             | Alamnimi | Tüüp | Kohustuslik/valikuline | Kirjeldus |
|------------------|----------|------|-------------------|-------------|
| ID               | | string | Nõutav | Müügidokumendi IDENTIFIKAATOR. |
| CartLines        | | IList\<CartLine\> | Valikuline | Ridade loend, mille jaoks hinnad ja allahindlused arvutatakse. |
|                  | Toote ID | Pikk | Vajalik CartLine’i ulatuses | Toote kirje ID |
|                  | ItemId | string | Valikuline | Kauba ID. Kui väärtus on antud, peab see vastama ProductId **parameetri väärtusele**. |
|                  | InventDimensionId | string | Valikuline | Varude dimensiooni ID. Kui väärtus on antud, peab **ItemId** **ja InventoryDimensionId** väärtuste kombinatsioon **vastama parameetri ProductId väärtusele**. |
|                  | Kogus | Kümnendarv | Vajalik CartLine’i ulatuses | Toote kogus |
|                  | Üksus UnitOfMeasureSymbol | string | Valikuline | Toote ühik. Kui väärtust ei ole esitatud, kasutab API vaikimisi toote müügiüksust. |
| CustomerId       | | string | Valikuline | Kliendikood. |
| Kliendikaardi ID    | | string | Valikuline | Kliendikaardi identifikaator. Iga kliendikaardiga seostatud kliendikonto peab sobima **CustomerId parameetri** väärtusega (kui see on olemas). Kliendikaarti ei loeta, kui seda ei leita või selle olek on **Blokeeritud**. |
| AffiliationLines | | IList\<AffiliationLoyaltyTier\> | Valikuline | Püsikliendijärgu read. Kui **esitatud on väärtused CustomerId** ja/ **või LoyaltyCardId**, **ühendatakse vastavad püsikliendijärgu read väärtustega AffiliationLines**. |
|                  | Allutuse ID | Pikk | AffiliationLoyaltyTieri ulatuselt nõutav | Allumiskirje ID. |
|                  | LoyaltyTierId | Pikk | AffiliationLoyaltyTieri ulatuselt nõutav | Püsikliendi järgu kirje ID. |
|                  | Väärtuse AffiliationTypeValue väärtus | Int | AffiliationLoyaltyTieri ulatuselt nõutav | Väärtus, mis näitab, kas all kuuluvusrea **tüüp** on Üldine (**0**) **või Püsikliendi** tüüp (**1**). Kui selle parameetri väärtuseks **on seatud 0**, võtab API **identifikaatoriks AffiliationId** **väärtuse ja ignoreerib LoyaltyTierId** väärtust. Kui selle väärtuseks on seatud 1 **, võtab API** identifikaatoriks LoyaltyTierId **väärtuse** ja ignoreerib väärtust AffiliationId **.** |
|                  | ReasonCodeLines | Kollektsioon\<ReasonCodeLine\> | AffiliationLoyaltyTieri ulatuselt nõutav | Põhjusekoodi read. See parameeter ei mõjuta hinnakujunduse arvutust, kuid on nõutav **osana objektist AffiliationLoyaltyTier**. |
|                  | CustomerId | string | AffiliationLoyaltyTieri ulatuselt nõutav | Kliendikood. |
| Kupongid          | | IList\<Coupon\> | Valikuline | Kuponge, mis ei ole rakendatavad (passiivne, aegunud või mitte leitav), hinnakujunduse arvutamisel ei arvestata. |
|                  | Kood | string | Kupongi ulatuselt nõutav | Kupongikood. |
|                  | Koodi ID | string | Valikuline | Kupongikoodi identifikaator. Kui väärtus on antud, peab see vastama koodiparameetri **väärtusele**. |
|                  | DiscountOfferId | string | Valikuline | Allahindluse ID Kui väärtus on antud, peab see vastama koodiparameetri **väärtusele**. |

**Taotluse näidiskogum**

```json
{
    "salesDocument": 
    {
        "Id": "CalculateSalesDocument",
        "CartLines": 
        [
            {
                "ProductId": 68719491408,
                "ItemId": "91003",
                "InventoryDimensionId": "",
                "Quantity": 1,
                "UnitOfMeasureSymbol": "ea"
            },
            {
                "ProductId": 68719493014,
                "Quantity": 2,
                "UnitOfMeasureSymbol": "ea"
            }
        ],
        "CustomerId": "3003",
        "AffiliationLines": 
        [
            {
                "AffiliationId": 68719476742,
                "LoyaltyTierId": 0,
                "AffiliationTypeValue": 0,
                "ReasonCodeLines": [],
                "CustomerId": null
            }
        ],
        "LoyaltyCardId": "55103",
        "Coupons": 
        [
            {
                "CodeId": "CODE-0005",
                "Code": "CPN0004",
                "DiscountOfferId": "ST100077"
            }
        ]
    }
}
```

Kogu ostukorvi objekt tagastatakse vastuse kehana. Hindade ja allahindluste selleks, et kontrollida hindu ja allahindlusi, peaksite keskenema järgmise tabeli väljadele.

| Nimi           | Alamnimi | Tüüp | Kirjeldus |
|----------------|----------|------|--------------|
| Netohind       | | Kümnendarv | Kogu müügidokumendi netohind enne allahindluste rakendamist. |
| Allahindluse summa | | Kümnendarv | Kogu müügidokumendi lõppallahindluse summa. |
| Summasumma    | | Kümnendarv | Kogu müügidokumendi kogusumma. |
| CartLines      | | IList\<CartLine\> | Arvutatud read, mis sisaldavad hinna ja allahindluse üksikasju. |
|                | Hind | Kümnendarv | Toote ühiku hind. |
|                | Netohind | Kümnendarv | Rea netohind enne allahindluste rakendamist (= hinnakogus *·*&times;*·*). |
|                | Allahindluse summa | Kümnendarv | Allahindluse summa. |
|                | Summasumma | Kümnendarv | Rea lõplik koguhinna tulemus. |
|                | Hinnajooned | IList\<PriceLine\> | Hinna üksikasjad, sh hinna allikas (baashind, hinna korrigeerimine või kaubandusle leping) ja summa. |
|                | Allahindluse read | IList\<DiscountLine\> | Allahindluse üksikasjad. |

## <a name="getavailablepromotions"></a>GetAvailablePromotions 

Kuna ostukorvil on mitu ostukorvi rida, tagastab *GetAvailablePromotions* API ostukorvi ridadele kõik rakendatavad allahindlused. 

*GetAvailablePromotions* API põhijuhtum on ostukorvi lehekülg, kus jaemüüjad soovivad kuvada praeguse ostukorvi puhul rakendatud allahindlusi või saadaolevaid kuponge.

Järgmine tabel näitab sisendparameetreid *GetAvailablePromotions* API jaoks.

| Nimi        | Tüüp | Kohustuslik/valikuline | Kirjeldus |
|-------------|------|-------------------|-------------|
| võti         | string | Nõutav | Ostukorvi ID. |
| cartLineIds | IEnumerable\<string\> | Valikuline | Seadke see parameeter, et tagastada ainult valitud ostukorvi ridade allahindlused. |

**Vastuse näidiskogum**

```json
{
    "value": 
    [
        {
            "LineId": "f495ffa507bc4f63a47a409cd8713dd7",
            "Promotion": {
                "OfferId": "ST100012",
                "OfferName": "Loyalty 5% off over $100",
                "PeriodicDiscountTypeValue": 4,
                "IsDiscountCodeRequired": false,
                "ValidationPeriodId": null,
                "AdditionalRestrictions": null,
                "Description": "All loyalty members get 5% with transaction total above $10 unless some exclusive or best price discounts are already applied on the transaction",
                "ValidFromDate": "2022-06-20T06:52:56.2460219Z",
                "ValidToDate": "2022-06-20T06:52:56.2460224Z",
                "CouponCodes": [],
                "ValidationPeriod": null
            }
        }
    ]
}
```

## <a name="addcoupons"></a>AddCoupons

*AddCoupons* API toetab kupongide loendi lisamist ostukorvi. See tagastab ostukorvi objekti pärast kupongide lisamist.

Järgmises tabelis on näidatud AddCoupons *API sisendparameetrid*.

| Nimi                 | Tüüp | Kohustuslik/valikuline | Kirjeldus |
|----------------------|------|-------------------|-------------|
| võti                  | string | Nõutav | Ostukorvi ID. |
| kupongikoodid          | IEnumerable\<string\> | Nõutav | Kupongikoodid, mida ostukorvi lisada. |
| isLegacyDiscountCode | Bool | Valikuline | Seadke see parameeter **tõeseks**, näitamaks, et kupong on pärandallahindluse kood. Vaikeväärtus on **väär**. |

## <a name="removecoupons"></a>Üksuse RemoveCoupons eemaldamine

RemoveCoupons *API* toetab kupongide loendi eemaldamist ostukorvist. See tagastab ostukorvi objekti pärast kupongide eemaldamist.

Järgmises tabelis on näidatud RemoveCoupons *API sisendparameetrid*.

| Nimi        | Tüüp | Kohustuslik/valikuline | Kirjeldus |
|-------------|------|-------------------|-------------|
| võti         | string | Nõutav | Ostukorvi ID. |
| kupongikoodid | IEnumerable\<string\> | Nõutav | Kupongikoodid, mida ostukorvist eemaldada. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
