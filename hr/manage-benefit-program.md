---
title: "Soodustusprogrammi määratlemine ja haldamine"
description: "Inimressursid pakuvad tööriistu, mida saab kasutada soodustuste, mahaarvamiste ja töötajate hüvitusplaanide seadistamiseks ja haldamiseks, mida organisatsioon oma töötajatele pakub või nende puhul töötleb. See artikkel sisaldab teavet soodustuste seadistamise ja haldamise kohta."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1d972f2d6bacf6f60ab3ce3bab2fcfaeb8d2e524
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="define-and-manage-a-benefits-program"></a>Soodustusprogrammi määratlemine ja haldamine

[!include[banner](includes/banner.md)]


Inimressursid pakuvad tööriistu, mida saab kasutada soodustuste, mahaarvamiste ja töötajate hüvitusplaanide seadistamiseks ja haldamiseks, mida organisatsioon oma töötajatele pakub või nende puhul töötleb. See teema sisaldab teavet soodustuste seadistamise ja haldamise kohta.

<a name="benefit-setup"></a>Soodustuse seadistamine
-------------

Enne kui töötajad saavad soodustuste saamiseks registreeruda, tuleb luua iga soodustuse elemendid. Need elemendid ühendavad sarnased soodustusplaanid ja määratlevad vaikesätted, nagu mahaarvamise määrad ja raamatupidamise üksikasjad. Paljusid neid sätteid saab kohandada, kui töötajad soodustuse saamiseks hiljem registreeruvad. Iga soodustusplaani puhul saab organisatsioon pakkuda mitut registreerimise võimalust või töötaja saab plaanis registreerumisest loobuda. 

[![Soodustuse protsessivoog](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Soodustuse elemendid
Enne soodustuste loomist ja töötajate registreerimist nende saamiseks peate määratlema elemendid, mis moodustavad soodustuse: tüüp, plaan ja valikud.

-   **Tüüp** – teatud soodustuse plaanide kogum, näiteks arstiabi või parkimine.
-   **Plaan** – lepinguliselt pakkujalt saadav konkreetne soodustus.
-   **Valik** – katvuse tase, näiteks ainult töötaja või töötaja ja abikaasa/partner.

Iga soodustuse tüübi, nt visiooni või hambaravi puhul saab organisatsioon pakkuda oma töötajatele ühte või enamat plaani. Iga plaani puhul saab organisatsioon pakkuda erinevaid valikuid. Näiteks saavad töötajad täiendava tähtajaga elukindlustuse katvuse osta oma ühe, kahe või kolme aastapalga ulatuses. Iga plaani ja valiku kombinatsioonist saab soodustus, mille saamiseks töötajad saavad registreeruda. 

[![soodustuse pilt](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Sobivus
Töötaja soodustuse saamise õiguse tööandja pakutavatele eri tüüpi soodustustele määravad paljud tegurid. Soodustuse loomisel Microsoft Dynamics 365 for Operationsis saate seadistada selle soodustuse puhul rakenduva soodustuse saamise õiguse tüübi. 

Saate muuta soodustuse saadavaks kõigile töötajatele. Mõned ettevõtted pakuvad näiteks parkimislube kõigile töötajatele erisoodustusena. Selle soodustuse loomisel seate soodustuse saamise õiguse suvandile **Kõigil töötajatel on soodustuse saamiseks õigus**. 

Muude soodustuste, nagu sissenõudmiste ja maksude kehtestamise puhul soodustuse saamise õigus ei kehti. Seda tüüpi soodustuste loomisel seate soodustuse saamise õiguse valikule **Jäta soodustuse saamise õiguse protsess vahele**. 

Lisaks võib soodustuse saamise õigus olla reeglipõhine. Näiteks ettevõte pakub töötajatele kahte tüüpi elukindlustust. Juhtivtöötajatel on õigus kasutada ühte meie elukindlustusplaani, samas kui kõigil teistel täistööajaga töötajatel on õigus kasutada muud elukindlustusplaani. Dynamics 365 for Operations saate luua kõigi juhtivtöötajate leidmiseks soodustuse saamise õiguse reegli ja teise reegli kõigi täistööajaga töötajate leidmiseks ja seejärel saate need reeglid asjakohasele soodustusele rakendada.

## <a name="enrollment"></a>Registreerimine
Pärast teie organisatsiooni pakutavate soodustuste loomist ja soodustuse saamise õiguse määratlemist saate töötajaid soodustuse saamiseks registreerida. Saate soodustuse saamiseks registreerida ühe töötaja või registreerida mitu töötajat ühe protsessi ühe või mitme soodustuse saamiseks. 

Mõnikord lõpetab organisatsioon konkreetsete soodustuste pakkumise. Sellisel juhul peate soodustust ja selle saamiseks registreerunud töötajaid värskendama. Hulgisoodustuse aegumine võimaldab teil korraga muuta nii soodustuse kui ka selleks soodustuseks töötajate registreerumise aegumiskuupäeva. Samuti saate valida mitut soodustuse saamiseks registreerunud töötajat ja muuta nende soodusperioodi lõppkuupäeva. 

Samuti võimaldab hulgisoodustuse pikendamine teil pikendada nii soodustuse kui ka selle saamiseks töötajate registreerumise aegumiskuupäeva, kui otsustate soodustust pakkuda kauem kui algselt plaanitud.

<a name="see-also"></a>Vt ka
--------

[Soodustuse saamise õiguse poliitikad](benefit-eligibility-policies.md)




