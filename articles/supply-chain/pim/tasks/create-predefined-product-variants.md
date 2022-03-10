---
title: Eelmääratletud tootevariantide loomine
description: Selles protseduuris juhendatakse teid looma tooteetalonidele tootevariante, kasutades tootedimensioonide kombinatsioone.
author: t-benebo
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6d3a4ae8efd438e01c263af1c0a1746d9484e491
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103094"
---
# <a name="predefined-product-variants"></a>Eelmääratletud tootevariandid

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a>Näidistsenaarium: Eelmääratletud tootevariantide loomine

Selles näidisstenaariumis juhendatakse teid looma tooteetalonidele tootevariante, kasutades tootedimensioonide kombinatsioone.

### <a name="make-demo-data-available"></a>Demoandmete kättesaadavaks tegemine

Selle stsenaariumi ja siinsoovitatud väärtustega töötamiseks peavad teil olema installitud demoandmed ja peate valima juriidilise isiku *USMF*.

### <a name="step-1-create-a-product-master"></a>Samm 1. Tooteetaloni loomine

Tooteetaloni loomiseks:

1. Avage **Tooteteabe haldus > Tooted > Tooteetalonid**.
1. Valige suvand **Uus**.
1. Kui väljal **Tootenumber** ei ole veel numbrit, sisestage väärtus. See on nõutav ainult siis, kui sellele väljale pole numbrijada häälestatud.
1. Sisestage toote nimi väljale **Toote nimi**.
1. Valige väljal **Tootedimensioonigrupp** tootedimensiooni grupp *SizeCol* (Suurus ja värv).
1. Valige uue tooteemudeli loomiseks ja avamiseks **OK**.

### <a name="step-2-add-product-dimensions"></a>Samm 2. Tootedimensioonide lisamine

Selles näites kirjeldatakse, kuidas sisestada käsitsi tootedimensioone. Samuti saate valida suuruse, värvi või laadi grupi, mis sisaldab tootedimensiooni väärtusi, mida soovite kasutada.

Tootedimensioonide lisamiseks:

1. Kui uus tooteetelm on endiselt avatud, valige tegevuspaanil **tootedimensioonid**.
1. Avage vahekaart **Suurus** ja valige tööriistaribal **Uus**, et lisada rida ruudustikule. Uue rea jaoks seadistage järgnev.
    - **Suurus:** valige suuruse väärtus.
    - **Nimi:** sisestage suuruse nimi.
1. Valige tööriistaribal **Uus** ja lisage ruudustikule teine suurus, millel on uus **suurus** ja **nimi**.
1. Avage vahekaart **Värvid** ja valige tööriistaribal **Uus**, et lisada rida ruudustikule. Uue rea jaoks seadistage järgnev.
    - **Värv:** valige värvi väärtus.
    - **Nimi:** sisestage värvi nimi.
1. Valige tööriistaribal **Uus** ja lisage ruudustikule teine värv, millel on uus **värv** ja **nimi**.
1. Valige käsk **Salvesta**.
1. Uue tootekoondi juurde tagasipöördumiseks sulgege leht.

### <a name="step-3-generate-product-variants"></a>3. samm. Tootevariantide loomine

> [!NOTE]
> See jaotis kirjeldab, kuidas luua tootevariantide, kui *variandisoovituste lehekülje parendusfunktsioon* ei ole lubatud. Tootevariantide loomise üksikasju, kui see funktsioon on saadaval, leiate järgmisest jaotisest.

Tootevariantide loomiseks:

1. Kui uus tooteetelm on endiselt avatud, valige tegevuspaanil **tootevariandid**.
1. Valige toimingupaanil suvand **Variandisoovitused**.
1. Süsteem loob loendi kõigi võimalike tootele määratud suuruste ja värvide kombinatsioonidega. Valige **Vali kõik** tööriistaribal.
    - Selles näites valige kõik võimalikud variandid. Kui soovite kasutada ainult võimalike tootedimensioonide kombinatsioonide alamkogumeid, märkige vastavalt vajadusele ainult vajalikud märkeruudud.  
1. Valige **Loo**.
1. Valige käsk **Salvesta**.

## <a name="improved-variant-suggestions"></a>Täiustatud variandisoovitused

*Variandisoovituste lehekülje parendusfunktsioon* parandab **variandisoovituste** lehte, et lahendada jõudluse ja kasutatavuse probleemid ettevõtete puhul, kus on suur hulk tootedimensiooni kombinatsioone. Täiustatud protsess tootedimensiooni väärtuste valimiseks, mille jaoks variandisoovitusi luua, muudab asjakohase tootevariantide kogumi tuvastamise ja vabastamise kiiremaks ja lihtsamaks.

Selle funktsiooniga lisatakse järgmised parendused:

- **Variandisoovituste edasi lükatud loomine:** **variandisoovituste** leht ei näita enam soovitusi, kui selle esimest korda avate. Selle asemel peate valima selgesõnaliselt soovitud väärtused ja valima kombinatsioonide loomiseks nupu **Soovita**. See muudab protsessi nähtavamaks ja interaktiivsemaks.
- **Dimensiooniväärtuste valik:** kui teil on palju dimensiooniväärtusi, olete tavaliselt huvitatud variantide soovituste loomisest, mis sisaldavad ainult mõnda neist (nt uute värvide või stiilide kogumi tutvustamisel). Täiustatud kujundusega saate valida dimensiooniväärtused, mille jaoks soovite tootevariandi soovitusi luua. See suurendab oluliselt soovitatud variantide olulisust ning parandab nii süsteemi jõudlust kui ka kasutajate tööviljakust.

### <a name="turn-the-variant-suggestions-page-improvements-feature-on-or-off"></a>Variandisoovituste lehe parendusfunktsiooni sisse- või väljalülitamine

Tarneahela halduse versiooni 10.0.25 puhul lülitatakse see funktsioon vaikimisi sisse. Administraatorid saavad selle funktsiooni sisse või välja lülitada, otsides *funktsioonihalduse*[tööruumist variandisoovituste lehekülje parendusfunktsiooni.](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

### <a name="work-with-the-improved-variant-suggestions"></a>Täiustatud variandisoovitustega töötamine

See jaotis kirjeldab, kuidas luua tootevariantide, kui *variandisoovituste lehekülje parendusfunktsioon* on lubatud.

1. Avage või looge tooteetelm ja lisage sellel nõutavad tootedimensioonid, nagu kirjeldatud eelmises jaotises.
1. Kui tooteetelm on endiselt avatud, valige tegevuspaanil **tootevariandid**.
1. Valige toimingupaanil suvand **Variandisoovitused**.
1. Valige väärtused, mida tahate iga mõõtmega kasutada.
1. Valige ülemisel tööriistaribal käsk **Soovita**.
1. Süsteem loob loendi kõigi võimalike valitud suuruste ja värvide kombinatsioonidega. Märkige kiirkaardil **Soovitatud variandid** ruut iga tootedimensiooni kombinatsiooni jaoks, mida soovite kasutada, või valige tööriistaribal **Vali kõik**, et neid valida.  
1. Valige **Loo**, et lisada variandid praegusele tooteetelmi põhiandmetele.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
