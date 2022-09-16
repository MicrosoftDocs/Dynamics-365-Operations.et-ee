---
title: WHat uut ja muutunud Dynamics 365 Commerce 10.0.29 (oktoober 2022)
description: See artikkel kirjeldab funktsioone, mis on uued või muutunud Microsoft Dynamics 365 Commerce 10.0.29-s.
author: josaw1
ms.date: 08/17/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 6e457864f51159f46f45e9b8969863c9d34c5786
ms.sourcegitcommit: 56677afde87a9176f879482a7af223e251801d5d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/14/2022
ms.locfileid: "9475899"
---
# <a name="whats-new-or-changed-in-dynamics-365-commerce-10029-october-2022"></a>Mis on Dynamics 365 Commercei versioonis 10.0.29 uut või mida on muudetud (oktoober 2022)

[!include [banner](../includes/banner.md)]


Selles artiklis loetletakse funktsioonid, mis on kas uued või versioonis Microsoft Dynamics 365 Commerce 10.0.29 muudetud. Sellel versioonil on järgu number 10.0.1326 see on saadaval järgmises graafikus.

- **Eelvaateversiooni välja andmine:** august 2022
- **Väljalaske üldine kättesaadavus (enesevärskendus):** september 2022
- **Väljalaske üldine kättesaadavus (automaatne värskendamine):** oktoober 2022

## <a name="features-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selles versioonis sisalduvad funktsioonid. Võime seda artiklit värskendada, et kaasata funktsioonid, mis lisati koostesse pärast selle artikli algset avaldamist.

| Funktsiooniala | Funktsioon | Lisateave | Lubaja:   |
|---------|------------------|----------------|--------------| 
| B2B | [Müügilepingu toe lubamine kanalites](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-b2b-sales-agreement-contract-based-pricing) | See funktsioon võimaldab ettevõtete vahel (B2B) müüjaorganisatsioonidel kasutada müügilepinguid Commerce Headquartersis, et määrata nende ostjatele lepingupõhine hinnakujundus. Kui B2B ostja kauplused e-äri veebisaidil, rakendatakse B2B ostja organisatsiooni jaoks konfigureeritud lepingupõhist hinnakujundust automaatselt kogu toote avastamisele, ostmisele ja väljaregistreerimise kogemusele. | Funktsioonihaldus<p>*Müügilepingu tugi kõigis kaubanduskanalites* |
| Klienditeenindus | [Klienditeeninduse lubamine koos Dynamics 365Channeliga klienditeeninduse jaoks](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/chat-dynamics-365-commerce-omnichannel-customer-service) | Esimese klassi klienditoe kogemus on võti isikupärastatud ja ärikogemuse pakkumiseks klientidele. Praegu on olemas mitu äri touchipunkti, nt füüsilised kauplused, võrgukanalid ja sotsiaalkanalid. Tarbijad ootavad isikupärastatud tugikogemust kõigis nendes puutepunktides. See funktsioon aitab teil suurendada ostukorvi teisendusi müüki, suurendada isikupärastatud suhtlust klientidega ja parandada klienditeenindust, integreerides Dynamics 365 Müügitellimuste klienditeenindusega. | Administraatorite/tegijate poolt lubatud |
| E-kaubandus | Tootevõrdluse tugi e-kaubanduses | Lubage ostjatel võrrelda tooteid erinevates kategooriates, nii et nad saavad endale õige ostu otsuse teha. See funktsioon on saadaval nii ettevõtete ja tarbijat (B2C) kui B2B-saitide jaoks. | Saidikonstruktorid | 
| Kinkekaardid | Jaemüügi kinkekaardi tabelite tugi ettevõtetevaheliseks andmete ühiskasutuseks | Dynamics headquarters toetab võimalust lubada ettevõteteülene andmete ühiskasutus kindlate tabelite jaoks Dynamicsi arhitektuuris. Selles funktsioonis lisab Dynamics 365 Commerce toe ettevõtetevahelisele andmete ühiskasutusele jaemüügi kinkekaardi tabelite jaoks. Seetõttu saab ühes ettevõttes kinkekaardi andmed nüüd dubleerida teisele ettevõttele keskkonnas. Ettevõtte kinkekaardi tabelisse tehtud muudatused jagatakse dubleeritud ettevõtte kinkekaardi tabelile. | Arendajad |
| Globaliseerimine | [Commerce’i lokaliseerimisfunktsiooni lubamine uue commerce SDK jaoks](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-commerce-localization-features-new-commerce-sdk) | Uus funktsioon annab võimaluse lubada Commerce Headquartersi Commerce’i lokaliseerimise funktsioonid, kasutades funktsioonihalduse raamistikku või parameetreid. Fiskaalintegratsiooni näidised on nüüd uude Commerce SDK-sse kaasatud ja toetavad iseseisvat pakkimist. See funktsioon lubab ka rakenduse Store Commerce sihtkoha globaalsed kliendid.<p><p>See vabastamine hõlmab Äriintegratsiooni funktsioone ja [Fiskaalintegratsiooni näidised Austria](../localizations/emea-aut-fi-sample.md), [Tšehhi Vabariigi](../localizations/emea-cze-fi-sample.md),[Prantsusmaa](../localizations/emea-fra-cash-registers.md), [Saksamaa](../localizations/emea-deu-fi-sample.md), [Itaalia](../localizations/emea-ita-fpi-sample.md), [Norra](../localizations/emea-nor-cash-registers.md) ja Poola [puhul](../localizations/emea-pol-fpi-sample.md). | Administraatorite/tegijate poolt lubatud |
| Jõudlus | Eemalda RTS-sõltuvus stsenaariumite "Kliendi redigeerimine" puhul | Kõrge saadavus ja kõrge jõudlus on vaikimisi ootused müügikohas (POS) ja e-äri kanalites. Nende ootuste täitmiseks ei pea Dynamics 365 Commerce kanalid klienditeabe redigeerimisel enam toetuda Äriinfo reaalajas kommunikatsioonile. Asünkroonste ja mitteasünkroonste klientide klienditeabe asünkroonselt redigeerimise võimalus aitab vähendada reaalajas kutseid Commerce Headquartersi. | Administraatorite/tegijate poolt lubatud |

## <a name="feature-state-changes-in-this-release"></a>Funktsiooni oleku muudatused selles väljalaskes

Järgmises tabelis loetletakse funktsioonid, mis muutsid kohustuslikuks või mis muutsid seda vaikimisi versioonis 10.0.29. Kõik need funktsioonid lülitatakse teie süsteemi jaoks automaatselt sisse kohe, kui te uuendate versiooniks 10.0.29. Kohustuslikke funktsioone ei saa välja lülitada, kuid vaikimisi sisse lülitatud funktsioone saab funktsioonihalduse abil endiselt [välja lülitada](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tabelis loetletakse ka funktsioonid, mis olid eelnevalt avalikus eelvaates, kuid on muutunud kättesaadavaks versioonis 10.0.29. See muudatus näitab, et funktsioonid on nüüd tootmiskeskkondades kasutamiseks soovitatavad. Need funktsioonid lülitatakse vaikimisi välja, kui pole märgitud teisiti. Seetõttu peate nende kasutamiseks [funktsioonihaldust](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kasutama.

| Funktsioon | Nimetus | Uue funktsiooni olek |
| --- | --- | --- |
| BrazilRetailLocalizationFeature_BR |(Brasiilia) Brasiiliale omased rakenduse Commerce funktsioonid | Vaikimisi sees |
| RetailAdvancedGTETaxAdjustmentFeature | (India) Rakendage jaemüügiväljavõtete jaoks Retail POS-is jaemüügitehingute jaoks arvutatud GST-d | Vaikimisi sees |
| RetailChronologicalInvoicePostingFeature_IT | (Itaalia) Luba kronoloogilise järjekorrata sisestatud jaemüügiarved | Vaikimisi sees |
| RetailDiscountWithoutTaxAdjustingFeature_MX | (Mehhiko) Jaemüügi CFDI globaalsete allahindluste korrigeerimine | Vaikimisi sees |
| JaemüügifiscalIntegrationConfigurationEnhancementFeature | Fiskaalüksuse integreerimise tehnilise profiili alistamised | Vaikimisi sees |
| Vaade RetailFiscalIntegrationConnectorLocationFeature | Fiskaalüksuse integreerimise juhtimine kassaregistritest | Vaikimisi sees |
| Välja RetailFiscalIntegrationLocalStorageBackupEnableFeature jaoks | Fiskaalüksuse integreerimise kohaliku salvestusruumi varukoopia | Vaikimisi sees |
| JaemüügifiscalIntegrationPostponeFiscalRegistrationFeature | Dokumentide registreerimise edasilükkamine | Vaikimisi sees |
| Funktsioon RetailFiscalIntegrationRegistrationProcessTerminalExceptionFeature | Kassaregistrite fiskaalüksuse registreerimise olek | Vaikimisi sees |
| RetailGSTInvoiceAddressTaxCalculationFeature_IN | (India) Arvutage GST e-kaubanduse tellimuste arve aadressi põhjal | Vaikimisi sees |
| RetailInvoicesDefaultSalesDocumentStatusFeature_PL | (Poola) Jaemüügiarvete müügidokumendi vaikeolek | Vaikimisi sees |
| RetailRecalculateRoundingOfTaxBaseAmountsFeature_MX | (Mehhiko) Retail CFDI globaalse maksu baassumma ümardamise ümberarvutamine. | Vaikimisi sees |
| JaemüügisupplementaryInvoiceFeature | Täiendavate arvete lubamine jaekauplustes lõpule viidud hulgilaokannetele | Vaikimisi sees |
| RetailInventoryBufferAndInventoryLevelEnableFeature   |  Luba varude puhvrid ja varude tasemed    |  Vaikimisi sees|
|Välja RetailInboundOutboundInventoryValidationFeature|   Lubage kinnitamine müügikoha sissetulevate ja väljaminevate varude toimingus   |   Vaikimisi sees   |
|  RetailInventoryChannelCalculationConsolidationFeature    |  Tõhustatud e-kaubanduse kanalipoolne varude arvutamise loogika |   Vaikimisi sees   |
|RetailInventoryAdjustmentsInPointOfSaleFeature|    Varade korrigeerimised kassas   |  Vaikimisi sees  |
| Rakendus RetailMultiplePickupDeliveryModeFeature |  Mitme pealevõtte tarnerežiimi tugi     |   Kohustuslik    |
|  RetailProductAvailabilityOptimizationFeature |   Optimeeritud toote saadavuse arvutus  |  Kohustuslik |
|   JaemüügipricingDataManagerV2Feature   |   Commerceִ’i hindamise mootori jõudluse parandamine |   Kohustuslik |
|  Jaemüügi hinnakujundusPreventUnintendedRecalculationFeature   | Enneta soovimatut hinnakalkulatsiooni commerce ordersi jaoks    |  Kohustuslik  |
| RetailTeamsIntegration    |   Luba Microsoft Teamsi integratsioon| Kohustuslik   |  
| ConsumerEFDSyncProcessFeature_BR | (Brasiilia) NFC-e sünkroonne töötlemine | Vaikimisi sees |
| JaemüügifiscalIntegrationInternalAndExternalServicesEnableFeature | Sise- ja väliskonnektorite tugi fiskaalüksuse integreerimise raamistikus | Kohustuslik |
| RetailTaxRegistrationIdEnableFeature_BR | (Brasiilia) Otsi kliente Retail POS-is maksuregistreerimisnumbrite järgi | Kohustuslik |
| RetailTaxRegistrationIdEnableFeature_IN | (India) Otsi kliente Retail POS-is maksuregistreerimisnumbrite järgi | Kohustuslik |
| RetailTaxRegistrationIdEnableFeature_IT | (Itaalia) Klienditeabe haldus Retail POS-is | Kohustuslik |
| RetailTaxRegistrationIdEnableFeature_PL | (Poola) Klienditeabe haldus Retail POS-is | Kohustuslik |
| RetailUpdateReturnOriginalTransactionIdGlobalEnableFeature_IN | (Jaemüügi GST India jaoks) Värskenda kreeditarveid viidetega originaalarvetele | Kohustuslik |
| RetailUserDefinedCertificateProfileFeature | Kasutaja määratletud serdiprofiilid jaekaupluste jaoks | Kohustuslik |
  

## <a name="additional-resources"></a>Lisaressursid

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finantside ja toimingute rakenduste platvormi värskendused

Microsoft Dynamics 365 Commerce 10.0.29 sisaldab platvormivärskendusi. Lisateavet vt Platvormi värskendustest [versioonile 10.0.29 Finance and Operations rakendustest (oktoober 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md). 

### <a name="bug-fixes"></a>Veaparandused

Teavet versiooni 10.0.29 igas versiooniga 10.0.29 lisatud uuenduses sisaldub vigaparanduste kohta, logige sisse elutsükli teenustesse (LCS) [ja vaadake KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559&dbType=3&qc=ec3e3846199f5d3a27a0c4949e3902ffdbc87560f0cf928c4838b3bdd421633c). 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 ja majandusharu pilved: 2022 väljalaskevoo 2 plaan

Kas teile pakuvad huvi meie ärirakenduste või platvormi uued ja hiljuti väljaantud võimalused?

Vaadake [Dynamics 365 ja majandusharu pilved: 2022 väljalaskevoo 2 plaan](/dynamics365-release-plan/2022wave2/). Käsitleme ühes dokumendis kõiki üksikasju otsast lõpuni ja ülevalt alla, millest võite plaanide tegemisel lähtuda.

### <a name="removed-and-deprecated-features"></a>Eemaldatud ja taunitud funktsioonid

Artikli [eemaldatud või taunitud funktsioonid Dynamics 365 Commerce](removed-deprecated-features-commerce.md) kirjeldavad funktsioone, mis on Commerce’i eemaldatud või taunitud.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

Enne mis tahes funktsiooni eemaldamist tootest teatatakse amortiseerumisest [Dynamics 365 Commerce](removed-deprecated-features-commerce.md) artikli 12 kuu jooksul enne eemaldamist eemaldatud või taunitud funktsioonides.

Murranguliste muudatuste puhul, mis mõjutavad ainult kompileerimise aega, kuid on binaarselt ühilduvad liivakasti- ja tootmiskeskkondadega, on aegumise aeg vähem kui 12 kuud. Need on tavaliselt funktsionaalsed uuendused, mida tuleb teha kompilaatori jaoks.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
