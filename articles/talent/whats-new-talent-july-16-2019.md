---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 Talent (16. juuli 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 07/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-07-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: cd7f288e5c1015f4266db527adfcd62a5dbbc95f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528095"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-16-2019"></a>Mis on uut ja mida on muudetud rakenduses Dynamics 365 Talent (16. juuli 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis
See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Attract.

### <a name="coming-soon-in-attract"></a>Peagi tulekul rakenduses Attract
#### <a name="job-approvals-appear-on-the-home-page"></a>Töökinnitused kuvatakse avalehel

Kinnitused kuvatakse armatuurlaua jaotises **Kinnitused**. Kinnitajad saavad kinnitusi üle vaadata jaotises **Teile määratud**, kus kuvatakse töö ID, töö pealkiri, teised kinnitajad ja töö määramise kuupäev. Kasutajad, kes töö kinnitamiseks esitavad, saavad oma töid üle vaadata jaotises **Teie taotletud**, mis kuvab kinnitajaid, kes peavad edastatud tööd veel kinnitama.

## <a name="changes-in-onboard"></a>Muutused Onboardis
See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused
Jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2390.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>Common Data Service kohandatud välju nüüd toetavad üksused

- BusinessProcessCalendar                     
- BusinessProcessGroupAssignment         
- BusinessProcessStage                          
- BusinessProcessTemplateHeader          
- BusinessProcessTemplateTask            
- HcmBenefitOption                              
- HcmBenefitType                                  
- HcmCompensationGrid                            
- HcmCompensationLevel                          
- HcmCompensationPayFrequency                 
- HcmCompensationReferencePointSetup        
- HcmCompensationReferencePointSetupLine 
- HcmCompensationRegion                     
- HcmCompFixedPlanTable                     
- HcmEmployment                                
- HcmEthnicOrigin                                
- HcmFixedCompensationEvent                 
- HcmJob                                           
- HcmJobFunction
- HcmJobType
- HcmLanguageCode
- HcmPayrollCalculationFrequency
- HcmPosition
- HcmPositionType
- HcmSkillType
- HcmVeteranStatus
- HcmWorkCalendarHoliday
- HcmWorkCalendarHolidayLine
- HcmWorker
- HcmWorkerPersonalDetail
- LeaveType
- OMDepartment
- OMLegalEntity
- PayCycle
- PayPeriod
- PayrollBenefitCalculationRate
- PayrollBenefitCalculationRateDetail
- PayrollEarningCode

### <a name="unable-to-see-goals-and-reviews-in-manager-self-service"></a>Juhi iseteeninduses ei saa eesmärke ja arvustusi näha

Selle nädala muudatused võimaldavad nüüd kõrgema tasandi juhtide eesmärkide ja ülevaadete kuvamist ja redigeerimist juhi iseteeninduses.

### <a name="goal-form-cannot-be-closed-after-a-user-edits-any-goal-field"></a>Eesmärgi vormi ei saa sulgeda, kui kasutaja ei redigeeri ühtegi eesmärgi välja

See versioon parandab probleemi, kus eesmärgi vorm ei sulgu valides **Sule**.

### <a name="creating-new-goals-and-saving-displays-error"></a>Uute eesmärkide loomine ja salvestamine kuvab tõrke

See versioon lahendab probleemi, kui salvestatakse eesmärgid töötaja ja juhi iseteeninduskeskuses.

### <a name="unable-to-add-a-field-to-position-details"></a>Välja ei saa ametikoha üksikasjadesse lisada 

Selle versiooniga on kohandatud väljad nüüd ametikoha üksikasjades toetatud.
 
### <a name="unable-to-set-up-expiring-date-on-the-earning-code-through-data-management"></a>Töötasu koodi aegumiskuupäeva ei saa andmehalduse kaudu seadistada

Muudatuste abil saate nüüd määrata andmehalduses töötasu koodide aegumiskuupäevi.

### <a name="new-custom-fields-dont-sync-quickly-enough"></a>Uued kohandatud väljad ei sünkrooni piisavalt kiiresti

Selle nädala versiooniga on parandatud kohandatud välja sünkroonimise jõudlust ühise andmeserveriga Common Data Service.

### <a name="entity-export-to-database-jobs-fail-with-error-message-format-of-the-initialization-string-does-not-conform-to-specification-starting-at-index-0"></a>Üksuse eksportimine andmebaasitöödesse nurjus tõrketeatega: „Lähtestusstringi vorming ei vasta määratlusele, mis algab indeksist 0.”

See versioon parandab probleemi, kus andmebaasi pakett-tööd ei õnnestu. Käsitsi uuendamiseks:

1. Go to **Andmehaldus**.
2. Valige **Konfigureeri üksuse eksportimist andmebaasi**.
3. Sisestage ühenduse string uuesti sihtkoha andmebaasi ja valige **Salvesta**.

### <a name="smtp-email-configuration-suddenly-fails-with-error-message-the-smtp-server-requires-a-secure-connection-or-the-client-was-not-authenticated"></a>SMTP-meili konfiguratsioon nurjub veateatega: „SMTP-server nõuab turvalist ühendust või klienti ei autenditud.”

See versioon parandab SMTP-meili konfiguratsiooni, mis ootamatult nurjub. Käsitsi uuendamiseks:

1. Avage **Süsteemihaldus**.
2. Select **Meiliparameetrite kuvamine**.
3. Valige **SMTP sätted**. 
4. Sisestage SMTP-serveri jaoks kasutatav kasutajanimi ja parool uuesti ning valige **Salvesta**.

## <a name="in-preview"></a>Eelvaates

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Eelvaate funktsioonid on lubatud ainult liivakasti eksemplarides

Kui valmistate ette uue Talenti eksemplari, saate eksemplari tüübiks määrata **Tootmine** või **Liivakast**. **Liivakasti** tüübi eksemplarid võimaldavad uute funktsioonide varajast katsetamist. Kõik olemasolevad Talenti eksemplarid uuendatakse eksemplari tüübiks **Tootmine**. Kui soovite mõne olemasoleva eksemplari **Liivakasti** tüübile värskendada, võtke muudatuse taotlemiseks ühendust [Toega](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support).

Lisateavet muudatuste avaldamise kohta vt teemast [Talenti ettevalmistamine](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Puhkuse tüüpide piiramine puhkusetaotluste korral

Organisatsioonid võivad töötajatele pakkuda mitut erinevat tüüpi puhkust. Siiski ei pruugi töötajatel olla asjakohane teatud puhkuse tüüpide puhkusetaotluste esitamine. Neid puhkuse tüüpe võib hallata hoopis HR. Selle väljalaskega saate konfigureerida, milliste puhkusetüüpide puhkusetaotluseid töötajad saavad esitada. 

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Halduri iseteeninduses otseste ja kaudsete alluvate jõudluse teabe kuvamine

Uus suvand võimaldab juhtidel vaadata nii oma otseste kui ka kaudsete alluvate jõudlust. Praegu saavad rea haldurid määrata ja uuendada jõudluse eesmärke ja väljastada uusi arvustusi. Lisaks saavad otsesed juhid ja nende töötajad hallata ja värskendada jõudluse töölehti, mis aitavad tagada sujuva jõudluse ülevaate protsessi. Selle muudatuse rakendamisel saavad juhid vaadata ja hallata lisaks otseste alluvate jõudlusega seotud teabele ka oma kaudsete alluvate jõudlusega seotud teavet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]