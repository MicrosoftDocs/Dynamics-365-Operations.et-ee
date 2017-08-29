--- 
title: Toote konfiguratsioonimudeli loomine
description: "See protseduur kirjeldab, kuidas luua toote konfiguratsioonimudelit ja sisestada põhiandmeid (nt atribuute ja alamkomponente)."
author: BibiSp
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: da8dd3bbc350c29ce1f7dc22ab3914dfee4b967c
ms.contentlocale: et-ee
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-product-configuration-model"></a>Toote konfiguratsioonimudeli loomine

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


