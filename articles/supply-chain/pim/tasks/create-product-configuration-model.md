---
title: Toote konfiguratsioonimudeli loomine
description: See protseduur kirjeldab, kuidas luua toote konfiguratsioonimudelit ja sisestada põhiandmeid (nt atribuute ja alamkomponente).
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9577005fb4fc016670713c36e40263ff30030caf
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203752"
---
# <a name="create-a-product-configuration-model"></a>Toote konfiguratsioonimudeli loomine

[!include [banner](../../includes/banner.md)]

See protseduur kirjeldab, kuidas luua toote konfiguratsioonimudelit ja sisestada põhiandmeid (nt atribuute ja alamkomponente). Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="create-a-product-model"></a>Tootemudeli loomine
1. Klõpsake valikut Tootevariandi mudeli määratlus.
2. Klõpsake valikut Toote konfiguratsioonimudelid.
3. Klõpsake Uus.
4. Sisestage väärtus väljale Nimi.
5. Sisestage väljale Kirjeldus soovitud väärtus.
6. Valige suvand väljal Lahendaja strateegia.
    * Lahendaja strateegia määrab, kuidas piiranguid piirangupõhises toote konfiguratsioonimudelis töödeldakse. See valik võib mõjutada toote konfiguratsioonimudeli toimimist.  
7. Sisestage väärtus väljale Nimi.
    * Juurkomponent tähistab toote konfiguratsioonimudelit, kuid seda saab kasutada ka muudes tootemudelites.  
8. Klõpsake nuppu OK.
9. Valige suvand väljal Taaskasuta konfiguratsioone.
    * Kui konfiguratsioonide taaskasutuse parameetri sätteks on määratud Jah, kontrollib süsteem identseid konfiguratsioone pärast iga konfiguratsiooniseanssi ja kasutab uuesti, kui leitakse täpne vaste.  

## <a name="add-attributes"></a>Atribuutide lisamine
1. Laiendage jaotist Atribuudid.
2. Klõpsake vahekaarti Lisa.
3. Märkige loendis valitud rida.
4. Sisestage väärtus väljale Nimi.
5. Sisestage väärtus väljale Lahendaja nimi.
    * Lahendaja nime kasutab toote konfiguraatori piirangu lahendaja. See ei tohi sisaldada tühikuid ega erimärke, v.a _ (allkriips).  
6. Sisestage väljale Kirjeldus soovitud väärtus.
    * Kirjeldav tekst kuvatakse konfiguratsiooni kasutajale ja seetõttu võib sellest õige atribuudi väärtuse valimisel abi olla.  
7. Sisestage või valige väärtus väljal Atribuudi tüüp.
    * Atribuudi tüüp määrab, millised väärtused on atribuudi jaoks saadaval.  
8. Märkige ruut Lisa taaskasutusse.
    * See valik on saadaval ainult siis, kui valitakse suvand Taaskasuta konfiguratsioone. Atribuudi lisamine taaskasutuse märkeruutu tähendab, et seda atribuuti arvestatakse, kui süsteem täpset vastet otsib.  

## <a name="add-subcomponents"></a>Alamkomponentide lisamine
1. Laiendage jaotist Alamkomponendid.
2. Klõpsake vahekaarti Lisa.
3. Märkige loendis valitud rida.
4. Sisestage väärtus väljale Nimi.
5. Sisestage väärtus väljale Lahendaja nimi.
6. Sisestage väljale Kirjeldus soovitud väärtus.
7. Valige või sisestage väärtus väljal Komponent.
    * Iga alamkomponent peab viitama komponendi definitsioonile. See mudel toetab taaskasutatavaid komponente ja tagab, et kui komponent on määratletud, saab seda kasutada paljudes tootemudelites.  
8. Klõpsake nuppu Salvesta.
9. Klõpsake valikut Koosluse rea üksikasjad.
    * Koosluse rea üksikasjade vorm võimaldab kasutajal valida alamkomponendile vajalikud atribuudid. Igale atribuudile saab anda püsiväärtuse või selle saab vastendada atribuudiga. Atribuudiga vastendamisel saab koosluse rea atribuut erinevad väärtused, olenevalt konfiguratsiooni valikust.  
10. Sisestage või valige väärtus väljal Kaubakood.
    * Iga alamkomponent tähistab piirangupõhise konfiguratsioonitehnoloogiaga konfigureeritavat tooteetaloni. Viidatakse kaubakoodi kaudu.  
11. Märkige ruut Määra.
12. Tehke väljal Arvutus valik Jah.
    * Arvutamise suvandi seadistamine tagab, et toode kaasatakse toote kuluarvutusse.  
13. Klõpsake vahekaarti Seadistus.
14. Märkige ruut Määra.
15. Sisestage arv väljale Kogus.
    * Koguse väli määratleb, kui palju seda toodet konfigureeritud tootes tarbitakse.  
16. Märkige ruut Määra.
17. Sisestage number väljale Seeria kohta.
18. Klõpsake nuppu OK.

