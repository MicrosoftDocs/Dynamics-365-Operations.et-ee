---
title: Elektroonilise aruandluse domeenispetsiifilise andmemudeli kujundamine
description: See artikkel kirjeldab, kuidas luua uus elektroonilise aruandluse (ER) konfiguratsioon, mis sisaldab elektrooniliste maksedokumentide andmemudelit.
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
ms.openlocfilehash: 6116ee7bc65aa72f655aa3e5d1467560792bd024
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291110"
---
# <a name="er-design-domain-specific-data-model"></a>Elektroonilise aruandluse domeenispetsiifilise andmemudeli kujundamine

[!include [banner](../../includes/banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua uue elektroonilise aruandluse (ER) konfiguratsiooni, mis sisaldab andmemudelit elektrooniliste maksedokumentide jaoks. Seda andmemudelit kasutatakse hiljem maksedokumentide vormingu loomisel andmeallikana.

Selles näites loote konfiguratsiooni näidisettevõttele Litware, Inc. Neid etappe saab teha mis tahes ettevõttes, kuna ER-konfiguratsioonid on ettevõtetel ühised. Etappide lõpuleviimiseks, peate esmalt läbima teemas „Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine” kirjeldatudetapid.

1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.

    Valige konfiguratsiooni pakkuja näidisettevõttele „Litware, Inc.” Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris „Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks” esitatud juhised.  
    
2. Klõpsake valikut Aruandluse konfiguratsioonid.

    Loote konfiguratsiooni, mis sisaldab elektroonilise makse dokumentide andmemudelit. Seda andmemudelit kasutatakse hiljem andmeallikana maksedokumentide vormingu loomisel.  

## <a name="create-a-new-data-model-configuration"></a>Uue andmemudeli konfiguratsiooni loomine
1. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
2. Sisestage väljale Nimi suvand Maksed (lihtsustatud mudel).
3. Sisestage väljale Kirjeldus suvand Makse mudeli konfiguratsioon.

    Aktiivne konfiguratsiooni pakkuja sisestatakse siia automaatselt. See pakkuja saab seda konfiguratsiooni hallata. Muud pakkujad saavad seda konfiguratsiooni kasutada, kuid ei saa seda hallata.  

4. Klõpsake konfiguratsiooni loomise ülesande lõpetamiseks nuppu „Loo konfiguratsioon”

## <a name="create-a-data-model"></a>Andmemudeli loomine
Loote valitud konfiguratsioonile uut andmemudelit. Selle konfiguratsiooni versiooni olekuks on Mustand.  
1. Klõpsake valikut Kujundaja.

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a>Makseprotsessis osaleva osapoole struktuuri määratlemine
1. Rippdialoogi avamiseks klõpsake valikut Uus.
2. Väljale Nimi sisestage Osapool.
3. Klõpsake vahekaarti Lisa.
4. Rippdialoogi avamiseks klõpsake valikut Uus.
5. Sisestage väljale Nimi suvand Nimi.
6. Valige väljalt Kaubakood suvand String.
7. Klõpsake vahekaarti Lisa.
8. Väljale Otsi sisestage Osapool.
9. Klõpsake nuppu Leia eelmine.

## <a name="define-the-bank-structure-for-this-model"></a>Selle mudeli pangastruktuuri määratlemine
1. Rippdialoogi avamiseks klõpsake valikut Uus.
2. Sisestage väljale Nimi suvand Esindaja.
3. Valige väljalt Kaubakood suvand Kirje.
4. Klõpsake vahekaarti Lisa.
5. Sisestage väljale Kirjeldus suvand Osapoole (deebitor/kreeditor) kontot hooldav finantsasutus (nt pank).

    Osapoole (deebitor/kreeditor) kontot hooldav finantsasutus.  

6. Rippdialoogi avamiseks klõpsake valikut Uus.
7. Sisestage väljale Nimi suvand Nimi. 
8. Valige väljalt Kaubakood suvand String.
9. Klõpsake vahekaarti Lisa.
10. Rippdialoogi avamiseks klõpsake valikut Uus.
11. Sisestage väljale Nimi suvand SWIFT.
12. Klõpsake vahekaarti Lisa.
13. Väljale Kirjeldus sisestage „Panga ID-kood”. 
14. Rippdialoogi avamiseks klõpsake valikut Uus.
15. Sisestage väljale Nimi suvand RoutingNumber.
16. Klõpsake vahekaarti Lisa.
17. Väljale Kirjeldus sisestage „Registreerimisnumber”.
18. Klõpsake nuppu Leia eelmine.

## <a name="define-the-bank-account-structure-for-this-model"></a>Selle mudeli konto struktuuri määratlemine
1. Rippdialoogi avamiseks klõpsake valikut Uus.
2. Sisestage väljale Nimi suvand Konto. 
3. Valige väljalt Kaubakood suvand Kirje.
4. Klõpsake vahekaarti Lisa.
5. Väljale Kirjeldus sisestage „Osapoole konto tuvastamine finantsasutuses (näiteks pangas)”.

    Osapoole konto tuvastamine finantsasutuses (näiteks pangas).  

6. Rippdialoogi avamiseks klõpsake valikut Uus.
7. Sisestage väljale Nimi suvand Valuuta. 
8. Valige väljalt Kaubakood suvand String.
9. Klõpsake vahekaarti Lisa.
10. Väljale Kirjeldus sisestage „Valuutakood”.
11. Rippdialoogi avamiseks klõpsake valikut Uus.
12. Sisestage väljale Nimi suvand Number. 
13. Klõpsake vahekaarti Lisa.
14. Rippdialoogi avamiseks klõpsake valikut Uus.
15. Sisestage väljale Nimi suvand IBAN. 
16. Klõpsake vahekaarti Lisa.
17. Väljale Kirjeldus sisestage „Rahvusvaheline pangakonto number”.

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a>Kreeditiülekande maksetüübi jaoks makseteate struktuuri määratlemine
1. Rippdialoogi avamiseks klõpsake valikut Uus.
2. Väljale Uus sõlm kui sisestage „Mudeli juur”.
3. Sisestage väljale Nimi suvand CustomerCreditTransferInitiation.
4. Klõpsake vahekaarti Lisa.
5. Väljale Otsi tippige „CustomerCreditTransferInitiation”. 
6. Klõpsake nuppu Leia eelmine.
7. Rippdialoogi avamiseks klõpsake valikut Uus.
8. Sisestage väljale Nimi suvand MessageIdentification. 
9. Klõpsake vahekaarti Lisa.
10. Väljale Kirjeldus sisestage „Juhendava osapoole määratud punkt-punktiline viide (mis saadetakse järgmisele osapoolele) teate identifitseerimiseks”.

    Juhendava osapoole määratud punkt-punktiline viide (mis saadetakse järgmisele osapoolele) teate identifitseerimiseks.  

11. Rippdialoogi avamiseks klõpsake valikut Uus.
12. Sisestage väljale Nimi suvand ProcessingDateTime.
13. Valige väljalt Kaubakood suvand DateTime.
14. Klõpsake vahekaarti Lisa.
15. Väljale Kirjeldus sisestage „Makseteate loomise kuupäev ja kellaaeg”. 
16. Rippdialoogi avamiseks klõpsake valikut Uus.

    Määratlege selle mudeli puhul makse kande struktuur.  

17. Sisestage väljale Nimi suvand Maksed.
18. Valige väljalt Kaubakood suvand Kirjete loend.
19. Klõpsake vahekaarti Lisa.
20. Sisestage väljale Kirjeldus suvand Praeguse teate makseread.
21. Rippdialoogi avamiseks klõpsake valikut Uus.
22. Sisestage väljale Nimi suvand Saaja. 
23. Valige väljalt Kaubakood suvand Kirje.
24. Klõpsake vahekaarti Lisa.
25. Väljale Kirjeldus sisestage „Osapool, kellele tuleb rahasumma maksta”. 
26. Klõpsake nuppu Vaheta kauba viidet.
27. Väljale Otsi sisestage Osapool.
28. Klõpsake nuppu Otsi järgmine.
29. Klõpsake nuppu OK.
30. Väljale Otsi sisestage „Maksed”.
31. Klõpsake nuppu Otsi järgmine.
32. Rippdialoogi avamiseks klõpsake valikut Uus.
33. Sisestage väljale Nimi suvand Maksja. 
34. Klõpsake vahekaarti Lisa.
35. Väljale Kirjeldus sisestage „Osapool, kes võlgneb rahasumma (lõplikule) kreeditorile”.
36. Klõpsake nuppu Vaheta kauba viidet.
37. Väljale Otsi sisestage Osapool.
38. Klõpsake nuppu Otsi järgmine.
39. Klõpsake nuppu OK.
40. Klõpsake nuppu Otsi järgmine.
41. Rippdialoogi avamiseks klõpsake valikut Uus.
42. Sisestage väljale Nimi suvand Kirjeldus.
43. Valige väljalt Kaubakood suvand String.
44. Klõpsake vahekaarti Lisa.
45. Rippdialoogi avamiseks klõpsake valikut Uus.
46. Sisestage väljale Nimi suvand Valuuta.
47. Klõpsake vahekaarti Lisa.
48. Väljale Kirjeldus sisestage „Valuutakood”.
49. Rippdialoogi avamiseks klõpsake valikut Uus.
50. Sisestage väljale Nimi suvand TransactionDate. 
51. Valige väljalt Kaubakood suvand Kuupäev.
52. Klõpsake vahekaarti Lisa.
53. Väljale Kirjeldus sisestage „Kande kuupäev”. 
54. Rippdialoogi avamiseks klõpsake valikut Uus.
55. Sisestage väljale Nimi suvand InstructedAmount.  
56. Valige väljalt Kaubakood suvand Tegelik.
57. Klõpsake vahekaarti Lisa.
58. Väljale Kirjeldus sisestage „Maksja ja saaja vahel enne maksude mahaarvamist liigutatav rahasumma”. Summa peaks olema väljendatud algatanud osapoole tellitud valuutas.

    Maksja ja saaja vahel enne maksude mahaarvamist liigutatav rahasumma. Summa peaks olema väljendatud algatanud osapoole tellitud valuutas.  

59. Rippdialoogi avamiseks klõpsake valikut Uus.
60. Sisestage väljale Nimi suvand End2EndID. 
61. Valige väljalt Kaubakood suvand String.
62. Klõpsake vahekaarti Lisa.
63. Väljale Kirjeldus sisestage „Algatava osapoole määratud kordumatu kood. Seda ID-d edastatakse muutmata kujul kogu ahela ulatuses. 
64. Sisestage väljale Nimi suvand PaymentModel.

    Suvandi PaymentModel nimi joondatakse maksevormide eelmääratletud liidestega.  

65. Klõpsake nuppu Salvesta.
66. Sulgege leht.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
