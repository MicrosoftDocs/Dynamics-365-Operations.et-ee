---
title: Müügipakkumiste loomine ja redigeerimine
description: See protseduur näitab, kuidas koostada ja muuta müügipakkumist.
author: omulvad
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f313aafb79faaf1344b7e70759405b3bab2d7e45
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148707"
---
# <a name="create-and-edit-sales-quotations"></a>Müügipakkumiste loomine ja redigeerimine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas koostada ja muuta müügipakkumist. Saate seda protseduuri käitada oma andmete või demoettevõtte USMF andmetega.


## <a name="create-a-sales-quotation"></a>Müügipakkumise loomine
1. Avage **Navigeerimispaan > Moodulid > Müük ja turundus > Müügipakkumised > Kõik pakkumised**.
2. Klõpsake valikut **Uus**.
3. Tehke väljal **Konto tüüp** valik „Potentsiaalne klient”.
4. Valige või sisestage väärtus väljal **Potentsiaalne klient**.
5. Laiendage jaotist **Üldine**. Kuna otsustasite koostada pakkumise müügi ja turunduse alalt, määratakse tüübiks automaatselt „Müügipakkumine”. Projektipakkumise koostamiseks tuleb see avada **Projektijuhtimise ja raamatupidamise** moodulis.
6. Klõpsake valikut **OK**. Hinnapakkumise ridade väljad ja tegevused on müügitellimuse ridade omadega väga sarnased.   Sarnaselt müügitellimustele saab hinnapakkumisi koostada konkreetsele kaubale või kui kaubakood pole teada või seda pole hinnapakkumise koostamise ajal olemas, saab hinnapakkumisi koostada müügikategooriale.     
7. Valige või sisestagle väärtus väljal **Kaup**.
8. Sisestage väärtus väljale **Sait**.
9. Sisestage arv väljale **Kogus**. Kui real valitud kaubal on kehtivaid kaubandusleppeid, kopeeritakse kehtiv hind ja allahindlused automaatselt pakkumise reale. Veenduge, et ühiku hinna väljal on väärtus, ja saate soovi korral sisestada ka allahindluse väärtusi. 
10. Klõpsake valikut **Salvesta**.
11. Klõpsake **Tegevuspaanil** valikut **Müügipakkumine**.
12. Klõpsake valikut **Kogusummad**.
13. Klõpsake valikut **OK**.
14. Valige müügipakkumise rida.
15. Klõpsake **Tegevuspaanil** valikut **Hinnapakkumine**.
16. Klõpsake valikut **Hinnasimulatsioon**.
    - Lehel **Hinnasimulatsiooni käivitamine** saate proovida korrigeerida oma hinnapakkumise eeldatavat tulu või kasumlikkust, tuginedes soovitud ühiku hinnale, allahindluse summale, allahindluse protsendile, kogusummale, marginaalile või kasumiprotsendile. Kui olete sihtarvudega rahul, rakendage soovitus hinnapakkumise reale ja selle hinnaga seotud välju värskendatakse vastavalt.  
    - Saate luua soovitud arvu hinnasimulatsioone. Kui klõpsate nuppu **Uus**, kopeeritakse selle pakkumise rea hinnatingimused lehele. Seejärel saate muuta hinnaga seotud väljade väärtused sihtväärtusteks. Ühe välja muutmine käivitab kõigi teiste väljade ümberarvutamise. Et süsteem saaks arvutada müügimarginaali ja kasumiprotsendi, peab toote ühiku omahind teada olema. Vaadake vahekaardilt Simuleeritud hinnad algseid hindu, soovitatavaid muudatusi ja nende mõju hinnapakkumise kogusummadele. Reeglina, kui hinnapakkumise reale rakendatakse simulatsioon, mis määrab uue summa, arvutab süsteem uue väärtuse ja sisestab selle väljale Ühiku hind. Kui simulatsioon põhineb uuel marginaalil või kasumiprotsendil, muudetakse ainult välja Netosumma ja Ühiku hind on tühi. Mõlemal juhul kustutatakse kõik allahindlused, mis olid enne simulatsiooni pakkumise real.
17. Klõpsake **Tegevuspaanil** valikut **Hinnapakkumine**.
18. Klõpsake käsku **Saada pakkumine**.
19. Tehke väljal **Hinnapakkumise printimine** valik „Jah”.
20. Klõpsake valikut **OK**. Aruande koostamine võib minuti aega võtta. Ärge sulgege lehte enne, kui see on valmis.

## <a name="update-a-sales-quotation"></a>Müügipakkumise värskendamine
1. Avage **Navigeerimispaan > Moodulid > Müük ja turundus > Müügipakkumised > Kõik pakkumised**.
2. Klõpsake **Tegevuspaanil** valikut **Järeltegevus**.
3. Klõpsake valikut **Teisenda kliendiks**.
4. Sisestage väärtus väljale **Kliendi konto**.
5. Klõpsake nuppu **Kontrolli**. Veenduge, et näete sõnumit, et sisestatud konto number on kasutamiseks vaba.  
6. Klõpsake valikut **OK**. Süsteem on nüüd loonud hinnapakkumise potentsiaalsele kliendile uue kliendikonto.  
7. Sulgege leht.
8. Klõpsake **Tegevuspaanil** valikut **Järeltegevus**.
9. Klõpsake käsku **Kinnita**.
10. Väljale **Põhjus** sisestage või valige väärtus.
11. Klõpsake valikut **OK**.
12. Paanil **Toimingupaan** klõpsake **Üldine**.
13. Klõpsake valikut **Müügitellimused**.
14. Sulgege leht.

