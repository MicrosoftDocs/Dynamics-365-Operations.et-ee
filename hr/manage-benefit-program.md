---
title: "Saate määratleda ja hallata programmi eelised"
description: "Inimressursid pakuvad tööriistu, mida saab kasutada soodustuste, mahaarvamiste ja töötajate hüvitusplaanide seadistamiseks ja haldamiseks, mida organisatsioon oma töötajatele pakub või nende puhul töötleb. See artikkel sisaldab teavet soodustuste seadistamise ja haldamise kohta."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: 81b5c9056001b26c33b2b42a95711ff5b50243e6
ms.openlocfilehash: 9d00d8f6dfa075f53473af31c257deb57c9efa86
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-manage-a-benefits-program"></a>Saate määratleda ja hallata programmi eelised

Inimressursid pakuvad tööriistu, mida saab kasutada soodustuste, mahaarvamiste ja töötajate hüvitusplaanide seadistamiseks ja haldamiseks, mida organisatsioon oma töötajatele pakub või nende puhul töötleb. See teema pakub teavet kuidas seadistada Halda kasu.

<a name="benefit-setup"></a>Kasu seadistamine
-------------

Enne kui töötajad saavad soodustuste saamiseks registreeruda, tuleb luua iga soodustuse elemendid. Need elemendid ühendavad sarnased soodustusplaanid ja määratlevad vaikesätted, nagu mahaarvamise määrad ja raamatupidamise üksikasjad. Paljusid neid sätteid saab kohandada, kui töötajad soodustuse saamiseks hiljem registreeruvad. Iga soodustusplaani puhul saab organisatsioon pakkuda mitut registreerimise võimalust või töötaja saab plaanis registreerumisest loobuda. 

[![Kasu äriprotsessi voog](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Soodustuse elemendid
Enne soodustuste loomist ja töötajate registreerimist nende saamiseks peate määratlema elemendid, mis moodustavad soodustuse: tüüp, plaan ja valikud.

-   **Tüüp** – teatud soodustuse plaanide kogum, näiteks arstiabi või parkimine.
-   **Plaan** – lepinguliselt pakkujalt saadav konkreetne soodustus.
-   **Valik** – katvuse tase, näiteks ainult töötaja või töötaja ja abikaasa/partner.

Iga soodustuse tüübi, nt visiooni või hambaravi puhul saab organisatsioon pakkuda oma töötajatele ühte või enamat plaani. Iga plaani puhul saab organisatsioon pakkuda erinevaid valikuid. Näiteks saavad töötajad täiendava tähtajaga elukindlustuse katvuse osta oma ühe, kahe või kolme aastapalga ulatuses. Iga plaani ja valiku kombinatsioonist saab soodustus, mille saamiseks töötajad saavad registreeruda. 

[![kasu pic](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Sobivus
Töötaja soodustuse saamise õiguse tööandja pakutavatele eri tüüpi soodustustele määravad paljud tegurid. Kasu loomisel Microsoft Dynamics 365 operatsioonide seadistamiseks tüüpi abikõlblikkuse, et neid saada. 

Saate kasu kättesaadavaks kõigile töötajatele. Näiteks mõned firmad pakuvad, parkimine läheb kõigi töötajate erisoodustusena. Selle soodustuse loomisel seate soodustuse saamise õiguse suvandile **Kõigil töötajatel on soodustuse saamiseks õigus**. 

Muude hüvitiste puhul nagu garnishments ja lõivud, ei kohaldada. Vadaku te luua sellist tüüpi hüvitisi, seate abikõlblikkuse **ümbersõit abikõlblikkuse protsess**. 

Lõpuks saab kasu saamise eeskirjadel põhinevat. Näiteks pakub firma töötajatele kahte tüüpi elukindlustuse hüvitise. Juhtivtöötajad on kõlblikud üks elukindlustuse plaan, kõik täistööajaga töötajad ei elukindlustuse plaani. Dynamics 365 toiminguteks, saate luua kasu abikõlblikkuse tavaliselt leida kõik juhtivtöötajad ja teise reegli kõik täisajaga töötajate leidmiseks ja seejärel kohaldama neid õigusnorme asjakohase kasuks.

## <a name="enrollment"></a>Registreerimine
Pärast teie organisatsiooni pakutavate soodustuste loomist ja soodustuse saamise õiguse määratlemist saate töötajaid soodustuse saamiseks registreerida. Saate soodustuse saamiseks registreerida ühe töötaja või registreerida mitu töötajat ühe protsessi ühe või mitme soodustuse saamiseks. 

Mõnikord lõpetab organisatsioon konkreetsete soodustuste pakkumise. Sel juhul peate värskendama kasu ja töötajaid, kes õpib. Mass kasuks aegumine saate muuta see soodustus samal ajal kasu ja töötaja registreerimiste aegumiskuupäeva. Samuti saate valida mitut soodustuse saamiseks registreerunud töötajat ja muuta nende soodusperioodi lõppkuupäeva. 

Samuti võimaldab hulgisoodustuse pikendamine teil pikendada nii soodustuse kui ka selle saamiseks töötajate registreerumise aegumiskuupäeva, kui otsustate soodustust pakkuda kauem kui algselt plaanitud.

<a name="see-also"></a>Vt ka
--------

[Benefit eligibility policies](benefit-eligibility-policies.md)


