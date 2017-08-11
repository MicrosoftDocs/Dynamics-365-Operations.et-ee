---
title: "Rakenduse Sales müügipakkumise päiste ja ridade sünkroonimine rakendusega Finance and Operations"
description: "Teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügipakkumise päiste ja ridade sünkroonimiseks rakendusest Microsoft Dynamics 365 for Sales rakendusse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 172a3da1b6d90a25ea9ebd14265e70e4a6f9bd70
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a>Rakenduse Sales müügipakkumise päiste ja ridade sünkroonimine rakendusega Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Enne kui saate lahendust Potentsiaalne klient sularahaks kasutada, tutvuge [Dynamics 365 andmeintegratsiooniga](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration). 

Teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse müügipakkumise päiste ja ridade sünkroonimiseks rakendusest Microsoft Dynamics 365 for Sales (Sales) rakendusse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations). 

## <a name="template-and-tasks"></a>Mall ja ülesanded

Müügipakkumise päiste ja ridade sünkroonimiseks rakendusest Sales rakendusse Finance and Operations kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.

- **Malli nimi:** Müügipakkumised (Salesist Fin and Opsi)
- **Ülesannete nimed projektis:**

    - QuoteHeader
    - QuoteLine

Enne müügipakkumise päiste ja ridade sünkroonimist on nõutavad järgmised sünkroonimisülesanded.

- Tooted
- Kontod (kui on kasutusel)
- Kontaktid (kui on kasutusel)

## <a name="entity-set"></a>Üksuste komplekt

| Müük        | CDS           | Finance and Operations    |
|--------------|---------------|---------------------------|
| Tsitaadid       | Pakkumine     | Müügipakkumise päised   |
| QuoteDetails | QuotationLine | CDS-i müügipakkumise read |

## <a name="entity-flow"></a>Üksuse voog

Müügipakkumised luuakse rakenduses Sales ja sünkroonitakse rakendusega Finance and Operations.

Müügipakkumised rakendusest Sales sünkroonitakse ainult juhul, kui täidetud on järgmised tingimused.

- Kõiki müügipakkumise ridadel olevaid tooteid hallatakse väliselt.
- Müügipakkumine on aktiivne või aktiveeritud.

## <a name="prospect-to-cash-solution-for-sales"></a>Lahendus Potentsiaalne klient sularahaks rakendusele Sales

Pakkumise üksusele on lisatud väli **Sisaldab ainult väliselt hallatavaid tooteid**, et jälgida järjepidevalt, kas müügipakkumine sisaldab täielikult või väliselt hallatavaid tooteid. Kui müügipakkumine sisaldab ainult väliselt hallatavaid tooteid, hallatakse neid rakenduses Finance and Operations. See käitumine aitab tagada, et te ei püüa sünkroonida müügipakkumise ridu toodetega, mis on rakendusele Finance and Operations tundmatud.

Kõiki tooteid ja ridu pakkumises värskendatakse pakkumise päisest pärit teabega **Sisaldab ainult väliselt hallatavaid tooteid**. See teave on leitav pakkumise reaüksuse väljalt **Pakkumine sisaldab ainult väliselt hallatavaid tooteid**.

Välju **Allahindlus**, **Tasud** ja **Maks** juhitakse keerulise seadistusega rakenduses Finance and Operations. See seadistus ei toeta praegu integratsiooni vastendamist. Praeguses kujunduses haldab ja reguleerib välju **Hind**, **Allahindlus**, **Tasu** ning **Maks** rakendus Finance and Operations.

Rakenduses Sales muudab lahendus järgmised väljad kirjutuskaitstuks, kuna väärtusi ei sünkroonita rakendusega Finance and Operations.

- **Müügipakkumise päise kirjutuskaitstud väljad:** Allahindluse %, Allahindlus, Veose kogus
- **Müügipakkumise ridade kirjutuskaitstud väljad:** Maks

## <a name="preconditions-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

- Enne müügipakkumiste sünkroonimist minge rakenduses Sales jaotisse **Sätted** &gt; **Haldus** &gt; **Süsteemi sätted** &gt; **Müük** ja veenduge, et välja **Allahindluse arvutamise meetod** sätteks oleks valitud **Ühiku kohta**. See säte aitab tagada, et reaüksuse allahindlus rakendusest Sales vastab sättele rakenduses Finance and Operations. Muidu ei ole allahindlus rakenduses Finance and Operations õige, kuna Finance and Operations loeb allahindlust allahindlusena ühiku kohta, isegi kui see oli rakenduses Sales allahindlus rea kohta.
- Minge rakenduses Finance and Operations jaotisse **Müügireskontro** &gt; **Seadistus** &gt; **Müügireskontro parameetrid**. Valige vahekaardil **Numbriseeria** müügipakkumiste numbriseeria ja klõpsake siis nuppu **Kuva üksikasjad**. Seejärel seadke jaotises **Üldine seadistus** välja **Käsitsi** sätteks **Jah**.
- Minge rakenduses Finance and Operations jaotisse **Müügireskontro** &gt; **Seadistus** &gt; **Müügireskontro parameetrid**. Seejärel seadke vahekaardil **Saadetised** välja **Tarnekuupäeva juhtimine** sätteks **Puudub**. See säte aitab vältida müügipakkumiste puhul sünkroonimise nurjumist.

### <a name="quoteheader"></a>QuoteHeader

- Väli **Nõutud tarnekuupäev** on rakenduses Finance and Operations nõutav ning sünkroonimine nurjub, kui see väli on jäetud tühjaks. Selle probleemi vältimiseks võetakse juhul, kui väli on tühi, vaikekuupäev valikust **Allikas &gt; CDS**. Kuupäev tuleb värskendada eelistatud väärtusele. Praegu ei saa tänase kuupäeva tähistamiseks sisestada väärtust, nagu **Täna**. Peate sisestama kindla kuupäeva. Malli vaikeväärtus suvandi **Nõutav tarnekuupäev** puhul on **1/1/2020**.
- Väli **Aadress, riik, piirkonnakood** on rakenduses Finance and Operations nõutav. Selleks et vältida sünkroonimistõrkeid, saate määrata vaikeväärtuse, mida kasutatakse, kui see väli on rakenduses Sales tühjaks jäetud. See vaikeväärtus on kasulik ka seetõttu, et kohalike aadresside puhul ei peate väljale **Riik, piirkond** väärtust käsitsi sisestama. Atribuudi **DeliveryAddressCountryRegionISOCode** jaoks malli vaikeväärtus puudub.
- Värskendage välja **CDS Organization ID** vastendust jaotises **Allikas &gt; CDS**, nii et see vastaks valikule **CDS-i organisatsioon** organisatsiooniüksuses.

    - Malli vaikeväärtus atribuudi **Organization_OrganizationId** puhul on **ORG001**.
    - Malli vaikeväärtus atribuudi **Account_Organization_OrganizationId** puhul on **ORG001**.
    - Malli vaikeväärtus atribuudi **InvoiceAccount_OrganizationId** puhul on **ORG001**.

### <a name="quoteline"></a>QuoteLine

- Värskendage välja **CDS Organization ID** vastendust jaotises **Allikas &gt; CDS**, nii et see vastaks valikule **CDS-i organisatsioon** organisatsiooniüksuses.

    - Malli vaikeväärtus atribuudi **Organization_OrganizationId** puhul on **ORG001**.
    - Malli vaikeväärtus atribuudi **Product_Organization_Organization_OrganizationId** puhul on **ORG001**.
    - Malli vaikeväärtus atribuudi **Quotation_Organization_Organization_OrganizationId** puhul on **ORG001**.

- Väli **Nõutud tarnekuupäev** on rakenduses Finance and Operations nõutav ning sünkroonimine nurjub, kui see väli on jäetud tühjaks. Selle probleemi vältimiseks võetakse juhul, kui väli on tühi, vaikekuupäev valikust **Allikas &gt; CDS**. Kuupäev tuleb värskendada eelistatud väärtusele. Praegu ei saa tänase kuupäeva tähistamiseks sisestada väärtust, nagu **Täna**. Peate sisestama kindla kuupäeva. Malli vaikeväärtus suvandi **Nõutav tarnekuupäev** puhul on **1/1/2020**.
- Saate lisada jaotisest **CDS &gt; Sihtkoht** järgmised vastendused, et tagada pakkumise ridade importimine rakendusse Finance and Operations, kui kliendilt või tootelt vaiketeave puudub.

    - **SiteId** – sait on vajalik pakkumiste ja müügitellimuse ridade loomiseks rakenduses Finance and Operations. Atribuudi **SiteId** jaoks malli vaikeväärtus puudub.
    - **WarehouseId** – ladu on vajalik pakkumiste ja müügitellimuse ridade töötlemiseks rakenduses Finance and Operations. Atribuudi **WarehouseId** jaoks malli vaikeväärtus puudub.

- Veenduge, et müügi mõõtühiku (UOM) puhul nõutav väärtuskaart rakenduses Finance and Operations oleks jaotise **CDS &gt; Sihtkoht** vastenduses suvandi **Quantity_UOM** puhul atribuudile **SALESUNITSYMBOL** olemas.

## <a name="template-mapping-in-data-integrator"></a>Malli vastendamine andmeintegraatoris

> [!NOTE]
> - Välju **Allahindlus**, **Tasud** ja **Maks** juhitakse keerulise seadistusega rakenduses Finance and Operations. See seadistus ei toeta praegu integratsiooni vastendamist. Praeguses kujunduses reguleerib välju **Hind**, **Allahindlus**, **Tasu** ning **Maks** rakendus Finance and Operations.
> - Väljad **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa. Nende väljade vastendamiseks peate seadistama väärtuskaardi, mis on kohane neis organisatsioonides olevatele andmetele, mille vahel üksust sünkroonitakse.

Järgmisel joonisel on toodud näide malli vastendusest andmeintegraatoris.

### <a name="quoteheader"></a>QuoteHeader

![Malli vastendamine andmeintegraatoris](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Malli vastendamine andmeintegraatoris](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a>QuoteLine

![Malli vastendamine andmeintegraatoris](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Malli vastendamine andmeintegraatoris](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Seotud dokumendid

[Rakenduse Finance and Operations toodete sünkroonimine rakenduse Sales toodetega](products-template-mapping.md)

[Rakenduse Sales kontode sünkroonimine rakenduse Finance and Operations klientidega](accounts-template-mapping.md)

[Rakenduse Sales kontaktide sünkroonimine rakenduse Finance and Operations kontaktide või klientidega](contacts-template-mapping.md)


