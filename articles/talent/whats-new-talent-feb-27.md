---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (27. veebruar 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 02/27/2019
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
ms.search.validFrom: 2019-02-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: afa1044c8adc9566149e20ade57e771b50d9c53f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529134"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-27-2019"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (27. veebruar 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Muutused Onboardis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused

Jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2163

### <a name="add-a-custom-fields-menu-item-to-system-administration"></a>Menüükäsu Kohandatud väljad lisamine süsteemihaldusesse

**Süsteemihalduse** tööruumi lisati navigeerimine menüüsse **Kohandatud väljad**.

### <a name="hide-the-import-and-create-options-for-new-mobile-applications"></a>Impordi peitmine ja uute suvandite loomine uutele mobiilirakendustele

Praegu ei saa Talentis uusi mobiilirakendusi luua. Uute mobiilsete kogemuste loomise suvand on menüüst **Mobiilirakendus** eemaldatud.

### <a name="variable-compensation-award-dmf-entity"></a>Ergutussüsteemi preemia (DMF-üksus)

Selles väljalaskes on nüüd eksportimiseks saadaval andmehaldusraamistiku (DMF) üksus **Ergutussüsteemi preemia**.

### <a name="uk-addresses-appear-in-the-personnel-management-analytics-page-as-swiss-addresses"></a>Ühendkuningriigi aadresse kuvatakse personalihalduse analüüsi lehel Šveitsi aadressidena

Selles versioonis kuvatakse aadressid linnade alusel. Selles versioonis parandatakse probleemid, kus visualiseeringud kuvasid töövõtja asukoha valesti.

### <a name="the-workforce-power-bi-report-shows-an-error-when-a-workers-seniority-date-is-on-leap-day"></a>Tööjõu Power BI aruandes kuvatakse tõrge, kui töötaja staaži kuupäev on liigaasta lisapäeval

Microsoft Power BI-s tehti parandus, mis arvestab staaži kuupäevi, mis langevad 29. veebruarile.

### <a name="employee-fixed-compensation-employee-variable-awards-employee-variable-plans-enrollments-allow-for-custom-fields"></a>Töövõtja põhipalk, töövõtja tulemustasud, töövõtja ergutussüsteemi plaanid (registreerimised) võimaldavad kohandatud välju

Nüüd saab töövõtja põhipalgale, töövõtja tulemustasudele ja töövõtja ergutussüsteemi plaanidele (registreerimised) lisada kohandatud välju. Nüüd saate lisaks vaikimisi saadaolevale teabele jälgida rohkem teavet töövõtja põhipalga ja ergutussüsteemi plaanide kohta. Kohandatud välju saab sisestada ja värskendada kas kasutajaliidese või esitatud üksuste kaudu.

### <a name="other-miscellaneous-bug-fixes"></a>Muud mitmesugused veaparandused

See versioon sisaldab ka muid väikesi veaparandusi.

## <a name="coming-soon"></a>Peagi tulekul

### <a name="advanced-compensation-security-fixed-and-variable"></a>Täpsem hüvitusturve (fikseeritud ja muutuv)

Paljudes ettevõtetes on hüvitise ja eeliste halduritel juurdepääs ainult teatud hüvituskirjetele. Need kirjed võivad olla juhtkonna või piirkonna töövõtjate omad. See muudatus võimaldab inimressurssidel (HR) hüvitusplaane hallata ja säilitada ettevõtte erinevate töövõtjate populatsioonide jaoks. Turberollid, mida saab määrata fikseeritud ja muutuvatele plaanidele, määravad nende plaanide juurdepääsu ja nendega seotud töövõtja andmed (näiteks palgateabe või lisakulumikirjed). Nende töövõtjate hüvitisi saavad töödelda ainult rollid, millele on antud juurdepääs.

### <a name="platform-update-24-for-finance-and-operations"></a>Teenuse Finance and Operations platvormivärskendus 24

Lisateavet Microsoft Dynamics 365 Finance and Operations (märts 2019) platvormiuuenduse 24 kohta vt [Finance and Operations rakenduse eelvaatefunktsioonid platvormiuuendus 24 (märts 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).

### <a name="make-employee-fixed-compensation-available-for-future-position-assignments"></a>Töövõtja põhipalga lubamine tulevaste ametikoha määrangute jaoks

Tavaliselt on ettevõttega liituvate töövõtjate alguskuupäev tulevikus. See muudatus võimaldab määrata põhipalka töövõtjatele, kellel on tulevased ametikoha määrangud.

## <a name="known-issues"></a>Teadaolevad probleemid

### <a name="changes-to-the-core-hr-integration-template-talent-common-data-service-to-finance"></a>Core HR-i integratsioonimalli muudatused (rakendusest Talent Common Data Service rakendusse Finance)
Core HR mall on värskendatud „täpsemaks päringumalliks”. Seetõttu on täpsem päring vaikimisi saadaval projektidele, mis selle malli abil luuakse. Lisaks on mis tahes vastendamise vaikefunktsioonid nähtavad ainult täpsemas päringuredaktoris. (Vastendamise vaikefunktsioonid kuvatakse vastendamistes kui „FN”.)

Lisateavet vastendamistõrgete kohta vt jaotisest [Mis on Dynamics 365 Talent: Core HR-is uut või mida on muudetud (14. detsember 2018)](https://docs.microsoft.com/dynamics365/unified-operations/talent/whats-new-talent-december-14).

Uue malli kasutamiseks looge uus projekt ja valige uus Talenti integratsioonimall.

Olemasoleva malli värskendamiseks toimige järgmiselt.

1. Järgmiste vastenduste värskendamine.

    - **Ametikohtadest Ametikohtadesse:** eemaldage see vastendus.
    - **Ametikohast Ametikoha peamisele tööülesandele:** eemaldage see vastendus.
    - **Ametikohast Peamisele ametikohale:** Lisage uus vastendus üksuse **Ametikoht** teenusest Common Data Service üksuse **Peamine ametikoht** rakendusse Finance and Operations. Teisaldage see järjestuses ametikohale 7.

        [![Vastendus Ametikohast Peamisele ametikohale](./media/CDS-Mapping1.png)](./media/CDS-Mapping1.png)

    - **Ametikohast Ametikoha üksikasjadele:** Lisage uus vastendus üksuse **Ametikoht** teenusest Common Data Service üksuse **Ametikoha üksikasjad** rakendusse Finance and Operations. Teisaldage see järjestuses ametikohale 8.

        [![Vastendus Ametikohast Ametikoha üksikasjadele](./media/CDS-Mapping2.png)](./media/CDS-Mapping2.png)

    - **Ametikohast Ametikoha kestvusele:** Lisage uus vastendus üksuse **Ametikoht** teenusest Common Data Service üksuse **Ametikoha kestvuse** rakendusse Finance and Operations.

        [![Vastendus Ametikohast Ametikoha kestustele](./media/CDS-Mapping3.png)](./media/CDS-Mapping3.png)

    - **Ametikohast Ametikoha hierarhiateni:** Lisage uus vastendus üksuse **Ametikoht** teenusest Common Data Service üksuse **Ametikoha hierarhiate** rakendusse Finance and Operations. Täpsema päringu projektile kättesaadavaks muutmiseks tehke valik **Täpsem päring**.

       [![Täpsema päringu nupp](./media/CDS-Advanced-Query.png)](./media/CDS-Advanced-Query.png)

2. Järgmiste vastenduste lisamine.
    
    [![Vastendamine](./media/CDS-Mapping4.png)](./media/CDS-Mapping4.png)

    1. cdm_jobpositionnumber cdm_jobspositionnumb... = POSITIONID cdm_parentjobpositionid.cdm-jobpositionnumb... = PARENTPOSITIONID cdm_validfrom cdm_validfrom = VALIDFROM cdm_validto cdm_validto = VALIDTO
       
    2. Valige välja **Otsing** kõrval link **Täpsem päring ja filtreerimine**.  

    3. Leidke veerg **cdm_parentjobpositionid.cdm_jobpositionnumber** ja valige selle paremal pool allanoolega nupp.

    4. Kuvatavas dialoogiboksis tehke valik **Eemalda tühjad**.

    5. Vaikeväärtuse teisenduse lisamiseks üksusele HIERARCHYTYPENAME tehke valikud **Lisa veerg \> Lisa tingimusveerg**.

        [![Käsk Lisa tingimusveerg](./media/Add-column.png)](./media/Add-column.png)

    6. Sisestage dialoogiboksis **Lisa tingimusveerg** uue veeru nimena **HIERARCHYTYPENAME**.
    7. Tingimuse osas **Kui** valige mis tahes väli, kasutage seosena väärtust **võrdne** ja sisestage mis tahes väärtus. Tingimuse osades **_Siis_** ja **Muidu** määrake, mis peab olema vaikeväärtus. Siinses näites sisestage mõlemas osas **Rida**.

        [![Tingimusveeru dialoogiboksi lisamine](./media/Add-conditional-column.png)](./media/Add-conditional-column.png)

    8. Dialoogiboksi **Täpsem päring ja filtreerimine** sulgemiseks valige **OK**.
    9. Lehel **Vastendamise ülesanne** valige uus veerg allikaks, mis loob üksusele HIERARCHYTYPENAME veel ühe vastenduse.

        [![Vastendamine](./media/CDS-Mapping5.png)](./media/CDS-Mapping5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]