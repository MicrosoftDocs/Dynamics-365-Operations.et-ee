---
title: Rakenduse Supply Chain Management müügiarvete päiste ja ridade sünkroonimine otse rakendusega Sales
description: Artikkel käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügipakkumise päiste ja ridade sünkroonimiseks otse Dynamics 365 müügist vormile Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 440b0a6fd2d297027cf3cab548c611544450269a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854119"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a>Rakenduse Supply Chain Management müügiarvete päiste ja ridade sünkroonimine otse rakendusega Sales

[!include [banner](../includes/banner.md)]



Artikkel käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügipakkumise päiste ja ridade sünkroonimiseks otse Dynamics 365 müügist vormile Dynamics 365 Supply Chain Management.

> [!NOTE]
> Enne kui saate kasutada lahendust Potentsiaalne klient sularahaks, tutvuge [andmete integreerimisega teenusesse Microsoft Dataverse for Apps](/powerapps/administrator/data-integrator).

## <a name="data-flow-in-prospect-to-cash"></a>Andmevoog lahenduses Potentsiaalne klient sularahaks

Lahendus Potentsiaalne klient sularahaks kasutab andmete integreerimise funktsiooni andmete sünkroonimiseks rakenduste Supply Chain Management ja Sales vahel. Andmeintegratsiooni funktsiooniga saadaolevad Prospect to cash mallid võimaldavad andmevahetust kontode, kontaktide, toodete, müügihindade, müügitellimuste ja müügiarvete kohta Supply Chain Managementi ja Salesi vahel. Järgmine illustratsioon näitab, kuidas sünkroonitakse andmeid rakenduste Supply Chain Management ja Sales vahel.

[![Andmevoog lahenduses Potentsiaalne klient sularahaks.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="template-and-tasks"></a>Mall ja ülesanded

Müügipakkumise päiste ja ridade vahetuks sünkroonimiseks rakendusest Sales rakendusse Supply Chain Management kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

- **Andmete integratsioon malli nimi:** Müügipakkumised (rakendusest Sales rakendusse Supply Chain Management) – otse
- **Ülesannete nimed andmete integratsiooni projektis.**

    - QuoteHeader
    - QuoteLine

Enne müügipakkumise päiste ja ridade sünkroonimist on nõutavad järgmised sünkroonimisülesanded.

- Tooted (rakendusest Supply Chain Management rakendusse Sales) - otse
- Kontod (rakendusest Sales rakendusse Supply Chain Management) - otse (kui kasutatakse)
- Kontaktid klientidesse (Salesist Supply Chain Managementi) - otse (kui kasutatakse)

## <a name="entity-set"></a>Üksuste komplekt

| Müük        | Supply Chain Management     |
|--------------|----------------------------|
| Tsitaadid       | Dataverse’i müügipakkumise päis |
| QuoteDetails | Dataverse’i müügipakkumise read  |

## <a name="entity-flow"></a>Üksuse voog

Müügiarved luuakse rakenduses Sales ja sünkroonitakse rakendusega Supply Chain Management.

Müügipakkumised rakendusest Sales sünkroonitakse ainult juhul, kui täidetud on järgmised tingimused.

- Kõiki müügipakkumises olevaid tooteid hallatakse väliselt.
- Kui klõpsate käsku **Aktiveeri pakkumine**, muutub müügipakkumine aktiivseks.

## <a name="prospect-to-cash-solution-for-sales"></a>Lahendus Potentsiaalne klient sularahaks rakendusele Sales

Pakkumise üksusele on lisatud väli **Sisaldab ainult väliselt hallatavaid tooteid**, et jälgida järjepidevalt, kas üksus **Müügipakkumine** sisaldab täielikult või väliselt hallatavaid tooteid. Kui müügipakkumine sisaldab ainult väliselt hallatavaid tooteid, hallatakse neid rakenduses Supply Chain Management. See käitumine aitab tagada, et te ei püüa sünkroonida müügipakkumise ridu, mis hõlmavad rakenduse Supply Chain Management jaoks tundmatuid tooteid.

Kõiki müügipakkumise tooteid ja ridu värskendatakse müügipakkumise päisest pärit teabega **Sisaldab ainult väliselt hallatavaid tooteid**. See teave on saadaval üksuse **QuoteDetails** väljal **Pakkumine sisaldab ainult väliselt hallatavaid tooteid**.

Pakkumise tootele saab lisada allahindluse, mis sünkroonitakse rakendusega Supply Chain Management. Päise välju **Allahindlus**, **Tasud** ja **Maks** juhitakse seadistusega rakenduses Supply Chain Management. See seadistus ei toeta praegu integratsiooni vastendamist. Praeguses kujunduses haldab ja reguleerib välju **Hind**, **Allahindlus**, **Tasu** ning **Maks** rakendus Supply Chain Management.

Rakenduses Sales muudab lahendus järgmised väljad kirjutuskaitstuks, kuna väärtusi ei sünkroonita rakendusega Supply Chain Management.

- Müügipakkumise päise kirjutuskaitstud väljad: **Allahindluse %**, **Allahindlus** ja **Veose kogus**
- Pakkumise toodete kirjutuskaitstud väljad: **Maks**

## <a name="preconditions-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

Enne müügipakkumiste sünkroonimist on oluline värskendada järgmisi sätteid.

### <a name="setup-in-sales"></a>Seadistus rakenduses Sales

- Veenduge, et load oleks seadistatud töörühma jaoks, kuhu rakenduses Sales häälestatud ühendusest pärit kasutaja on määratud. Demoandmete kasutamisel on kasutajal tavaliselt administraatori juurdepääs, kuid töörühmal mitte. Kui töörühmal ei ole administraatorijuurdepääsu, ilmub andmete integratsioonis projekti käivitamisel veateade, mis annab teada, et peamine töörühm puudub.

    Töörühma lubade seadistamiseks avage jaotis **Sätted** &gt; **Turve** &gt; **Töörühmad** ja valige vastav töörühm. Valige **Rollide haldamine** ja seejärel valige roll, millel on soovitud load, nt **Süsteemiadministraator**.

- Avage jaotis **Sätted** &gt; **Administreerimine** &gt; **Süsteemisätted** &gt; **Sales** ja veenduge, et kasutusel oleks järgmised sätted.

    - Suvand **Kasuta süsteemi hinna arvutamise süsteemi** on seatud väärtusele **Jah**.
    - Väli **Allahindluse arvutamise meetod** on seatud väärtusele **Rea kaup**.

### <a name="setup-in-the-data-integration-project"></a>Seadistus andmeintegratsiooni projektis

#### <a name="quoteheader"></a>QuoteHeader

- Veenduge, et atribuutide **Shipto\_country** – **DeliveryAddressCountryRegionISOCode** vahel oleks olemas nõutav vastendamine. Väärtuste kaardil saate määratleda vaikeväärtuse, mida kasutatakse juhul, kui väärtus on tühi. Jätke vasak pool tühjaks ja määrake paremal pool soovitud riik või regioon. Nii ei pea riigisiseste tellimuste puhul riiki või regiooni sisestama.

    Malli väärtus on väärtuskaart, kus on vastendatud mitu riiki või regiooni ja mille puhul tühja välja väärtus on **Ameerika Ühendriigid**.

#### <a name="quoteline"></a>QuoteLine

- Veenduge, et üksuse **SalesUnitSymbol** nõutav väärtuskaart oleks rakenduses Supply Chain Management olemas.
- Veenduge, et rakenduses Sales oleks nõutud ühikud määratletud.

    Üksuste **oumid.name** ja **SalesUnitSymbol** jaoks on määratletud väärtuskaardiga malli väärtus.

- Valikuline: saate lisada järgmised vastendused, et tagada pakkumise ridade importimine rakendusse Supply Chain Management, kui kliendilt või tootelt vaiketeave puudub.

    - **SiteId** – sait on vajalik pakkumiste ja müügitellimuse ridade loomiseks rakenduses Supply Chain Management. Atribuudi **SiteId** jaoks malli vaikeväärtus puudub.
    - **WarehouseId** – ladu on vajalik pakkumiste ja müügitellimuse ridade töötlemiseks rakenduses Supply Chain Management. Atribuudi **WarehouseId** jaoks malli vaikeväärtus puudub.

## <a name="template-mapping-in-data-integrator"></a>Malli vastendamine andmeintegraatoris

> [!NOTE]
> - Päise välju **Allahindlus**, **Tasud** ja **Maks** juhitakse keeruka seadistusega rakenduses Supply Chain Management. See seadistus ei toeta praegu integratsiooni vastendamist. Praeguses kujunduses reguleerib välju **Hind**, **Allahindlus**, **Tasu** ning **Maks** rakendus Supply Chain Management.
> - Väljad **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa. Nende väljade vastendamiseks peate seadistama väärtuskaardi, mis on kohane neis organisatsioonides olevatele andmetele, mille vahel üksust sünkroonitakse.

Järgmisel joonisel on toodud näide malli vastendusest andmeintegraatoris.

### <a name="quoteheader"></a>QuoteHeader

![Malli vastendamine andmeintegraatoris, QuoteHeader.](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![Malli vastendamine andmeintegraatoris, QuoteLine.](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-articles"></a>Seotud artiklid

[Potentsiaalne klient sularahaks](prospect-to-cash.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]