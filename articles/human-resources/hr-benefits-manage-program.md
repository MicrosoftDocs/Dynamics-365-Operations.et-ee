---
title: Soodustusprogrammi määratlemine ja haldamine
description: Inimressursid pakuvad tööriistu, mida saab kasutada soodustuste, mahaarvamiste ja töötajate hüvitusplaanide seadistamiseks ja haldamiseks, mida organisatsioon oma töötajatele pakub või nende puhul töötleb. See artikkel sisaldab teavet soodustuste seadistamise ja haldamise kohta.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 08b80f4f90ce6b4a286120cd6329a45a4ebd3f71
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877797"
---
# <a name="define-and-manage-a-benefits-program"></a>Soodustusprogrammi määratlemine ja haldamine


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Inimressursid pakuvad tööriistu, mida saab kasutada soodustuste, mahaarvamiste ja töötajate hüvitusplaanide seadistamiseks ja haldamiseks, mida organisatsioon oma töötajatele pakub või nende puhul töötleb. See artikkel sisaldab teavet soodustuste seadistamise ja haldamise kohta.

## <a name="benefit-setup"></a>Soodustuse seadistamine

Enne kui töötajad saavad soodustuste saamiseks registreeruda, tuleb luua iga soodustuse elemendid. Need elemendid ühendavad sarnased soodustusplaanid ja määratlevad vaikesätted, nagu mahaarvamise määrad ja raamatupidamise üksikasjad. Paljusid neid sätteid saab kohandada, kui töötajad soodustuse saamiseks hiljem registreeruvad. Iga soodustusplaani puhul saab organisatsioon pakkuda mitut registreerimise võimalust või töötaja saab plaanis registreerumisest loobuda. 

[![Soodustuse protsessivoog.](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Soodustuse elemendid

Enne soodustuste loomist ja töötajate registreerimist nende saamiseks peate määratlema elemendid, mis moodustavad soodustuse: tüüp, plaan ja valikud.

-   **Tüüp** – teatud soodustuse plaanide kogum, näiteks arstiabi või parkimine.
-   **Plaan** – lepinguliselt pakkujalt saadav konkreetne soodustus.
-   **Valik** – katvuse tase, näiteks ainult töötaja või töötaja ja abikaasa/partner.

Iga soodustuse tüübi, nt visiooni või hambaravi puhul saab organisatsioon pakkuda oma töötajatele ühte või enamat plaani. Iga plaani puhul saab organisatsioon pakkuda erinevaid valikuid. Näiteks saavad töötajad täiendava tähtajaga elukindlustuse katvuse osta oma ühe, kahe või kolme aastapalga ulatuses. Iga plaani ja valiku kombinatsioonist saab soodustus, mille saamiseks töötajad saavad registreeruda. 

[![soodustuse pilt.](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Sobivus
Töötaja soodustuse saamise õiguse tööandja pakutavatele eri tüüpi soodustustele määravad paljud tegurid. Soodustuse loomisel Dynamics 365 Human Resourcesis saate seadistada selle soodustuse puhul rakenduva soodustuse saamise õiguse tüübi. 

Saate muuta soodustuse saadavaks kõigile töötajatele. Mõned ettevõtted pakuvad näiteks parkimislube kõigile töötajatele erisoodustusena. Selle soodustuse loomisel seate soodustuse saamise õiguse suvandile **Kõigil töötajatel on soodustuse saamiseks õigus**. 

Muude soodustuste, nagu sissenõudmiste ja maksude kehtestamise puhul soodustuse saamise õigus ei kehti. Seda tüüpi soodustuste loomisel seate soodustuse saamise õiguse valikule **Jäta soodustuse saamise õiguse protsess vahele**. 

Lisaks võib soodustuse saamise õigus olla reeglipõhine. Näiteks ettevõte pakub töötajatele kahte tüüpi elukindlustust. Juhtivtöötajatel on õigus kasutada ühte meie elukindlustusplaani, samas kui kõigil teistel täistööajaga töötajatel on õigus kasutada muud elukindlustusplaani. Rakenduses Human Resources saate luua kõigi juhtivtöötajate leidmiseks soodustuse saamise õiguse reegli ja teise reegli kõigi täistööajaga töötajate leidmiseks ning seejärel saate need reeglid asjakohasele soodustusele rakendada.

## <a name="enrollment"></a>Registreerimine
Pärast teie organisatsiooni pakutavate soodustuste loomist ja soodustuse saamise õiguse määratlemist saate töötajaid soodustuse saamiseks registreerida. Saate soodustuse saamiseks registreerida ühe töötaja või registreerida mitu töötajat ühe protsessi ühe või mitme soodustuse saamiseks. 

Mõnikord lõpetab organisatsioon konkreetsete soodustuste pakkumise. Sellisel juhul peate soodustust ja selle saamiseks registreerunud töötajaid värskendama. Hulgisoodustuse aegumine võimaldab teil korraga muuta nii soodustuse kui ka selleks soodustuseks töötajate registreerumise aegumiskuupäeva. Samuti saate valida mitut soodustuse saamiseks registreerunud töötajat ja muuta nende soodusperioodi lõppkuupäeva. 

Samuti võimaldab hulgisoodustuse pikendamine teil pikendada nii soodustuse kui ka selle saamiseks töötajate registreerumise aegumiskuupäeva, kui otsustate soodustust pakkuda kauem kui algselt plaanitud.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
