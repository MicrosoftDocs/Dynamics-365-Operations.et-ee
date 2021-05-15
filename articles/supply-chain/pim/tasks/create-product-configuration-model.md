---
title: Toote konfiguratsioonimudeli loomine
description: See protseduur kirjeldab, kuidas luua toote konfiguratsioonimudelit ja sisestada põhiandmeid (nt atribuute ja alamkomponente).
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cb9e33d7bab6ca9cd378ec40baa796d1a933ece
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921361"
---
# <a name="create-a-product-configuration-model"></a>Toote konfiguratsioonimudeli loomine

[!include [banner](../../includes/banner.md)]

See protseduur kirjeldab, kuidas luua toote konfiguratsioonimudelit ja sisestada põhiandmeid (nt atribuute ja alamkomponente). Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="create-a-product-model"></a>Tootemudeli loomine

1. Avage **Tooteteabe haldus \> Tooted \> Tootekonfiguratsiooni mudelid**.
1. Valige suvand **Uus**.
1. Sisestage väärtus väljale **Nimi**.
1. Sisestage väärtus väljale **Kirjeldus**.
1. Valige väljal **Lahendaja strateegia** suvand.
    * Lahendaja strateegia määrab, kuidas piiranguid piirangupõhises toote konfiguratsioonimudelis töödeldakse. See valik võib mõjutada toote konfiguratsioonimudeli toimimist.  
1. Sisestage väärtus väljale **Nimi**.
    * Juurkomponent tähistab toote konfiguratsioonimudelit, kuid seda saab kasutada ka muudes tootemudelites.  
1. Valige nupp **OK**.
1. Valige väljal **Konfiguratsioonide taaskasutamine** suvand.
    * Kui konfiguratsioonide taaskasutuse parameetri sätteks on määratud Jah, kontrollib süsteem identseid konfiguratsioone pärast iga konfiguratsiooniseanssi ja kasutab uuesti, kui leitakse täpne vaste.  

## <a name="add-attributes"></a>Atribuutide lisamine

1. Laiendage jaotist **Atribuudid**.
2. Valige **Lisa**.
3. Märkige loendis valitud rida.
4. Sisestage väärtus väljale **Nimi**.
5. Sisestage väljale **Lahendaja nimi** väärtus.
    * Lahendaja nime kasutab toote konfiguraatori piirangu lahendaja. See ei tohi sisaldada tühikuid ega erimärke, v.a _ (allkriips).  
6. Sisestage väärtus väljale **Kirjeldus**.
    * Kirjeldav tekst kuvatakse konfiguratsiooni kasutajale ja seetõttu võib sellest õige atribuudi väärtuse valimisel abi olla.  
7. Sisestage või valige väärtus väljal **Atribuudi tüüp**.
    * Atribuudi tüüp määrab, millised väärtused on atribuudi jaoks saadaval.  
8. Valige märkeruut **Kaasa korduvkasutusse**.
    * See valik on saadaval ainult siis, kui valitakse suvand Taaskasuta konfiguratsioone. Atribuudi lisamine taaskasutuse märkeruutu tähendab, et seda atribuuti arvestatakse, kui süsteem täpset vastet otsib.  

## <a name="add-subcomponents"></a>Alamkomponentide lisamine

1. Laiendage jaotist **Alamkomponendid**.
2. Valige **Lisa**.
3. Märkige loendis valitud rida.
4. Sisestage väärtus väljale **Nimi**.
5. Sisestage väljale **Lahendaja nimi** väärtus.
6. Sisestage väärtus väljale **Kirjeldus**.
7. Valige või sisestage väärtus väljal **Komponent**.
    * Iga alamkomponent peab viitama komponendi definitsioonile. See mudel toetab taaskasutatavaid komponente ja tagab, et kui komponent on määratletud, saab seda kasutada paljudes tootemudelites.  
8. Valige käsk **Salvesta**.
9. Valige **koosluse rea üksikasjad**.
    * Koosluse rea üksikasjade vorm võimaldab kasutajal valida alamkomponendile vajalikud atribuudid. Igale atribuudile saab anda püsiväärtuse või selle saab vastendada atribuudiga. Atribuudiga vastendamisel saab koosluse rea atribuut erinevad väärtused, olenevalt konfiguratsiooni valikust.  
10. Sisestage või valige väärtus väljale **Kauba kood**.
    * Iga alamkomponent tähistab piirangupõhise konfiguratsioonitehnoloogiaga konfigureeritavat tooteetaloni. Viidatakse kaubakoodi kaudu.  
11. Märkige ruut **Määra**.
12. Valige suvand **Jah** väljal **Kalkulatsioon**.
    * Arvutamise suvandi seadistamine tagab, et toode kaasatakse toote kuluarvutusse.  
13. Valige vahekaart **Häälestus**.
14. Märkige ruut **Määra**.
15. Sisestage arv väljale **Kogus**.
    * Koguse väli määratleb, kui palju seda toodet konfigureeritud tootes tarbitakse.  
16. Märkige ruut **Määra**.
17. Sisestage number väljale **Seeria kohta**.
18. Valige nupp **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]