---
title: Müügipakkumiste loomine ja redigeerimine
description: See protseduur näitab, kuidas koostada ja muuta müügipakkumist.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b5618a815aaff12dd366523920ed275801b3b16
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "343623"
---
# <a name="create-and-edit-sales-quotations"></a>Müügipakkumiste loomine ja redigeerimine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas koostada ja muuta müügipakkumist. Saate seda protseduuri käitada oma andmete või demoettevõtte USMF andmetega.


## <a name="create-a-sales-quotation"></a>Müügipakkumise loomine
1. Avage Müük ja turundus > Müügipakkumised > Kõik hinnapakkumised.
2. Klõpsake valikut Uus.
3. Tehke väljal Konto tüüp valik Potentsiaalne klient.
4. Valige või sisestage väärtus väljal Potentsiaalne klient.
5. Laiendage jaotis Üldine.
    * Kuna otsustasite koostada pakkumise müügi ja turunduse alalt, määratakse tüübiks automaatselt Müügipakkumine. Projektipakkumise koostamiseks tuleb see avada projektijuhtimise ja raamatupidamise moodulis.   
6. Klõpsake nuppu OK.
    * Hinnapakkumise ridade väljad ja tegevused on müügitellimuse ridade omadega väga sarnased.   Sarnaselt müügitellimustele saab hinnapakkumisi koostada konkreetsele kaubale või kui kaubakood pole teada või seda pole hinnapakkumise koostamise ajal olemas, saab hinnapakkumisi koostada müügikategooriale.  
7. Valige või sisestage väärtus väljal Kaup.
8. Tippige väärtus väljale Kaup.
9. Sulgege leht.
10. Sisestage arv väljale Kogus.
    * Kui real valitud kaubal on kehtivaid kaubandusleppeid, kopeeritakse kehtiv hind ja allahindlused automaatselt pakkumise reale. Veenduge, et ühiku hinna väljal on väärtus, ja saate soovi korral sisestada ka allahindluse väärtusi.  
11. Klõpsake nuppu Salvesta.
12. Klõpsake toimingupaanil valikut Müügipakkumine.
13. Klõpsake valikut Kogusummad.
14. Klõpsake nuppu OK.
15. Klõpsake valikut Müügipakkumise rida.
16. Klõpsake valikut Hinnad.
    * Lehel Hinnasimulatsiooni käivitamine saate proovida korrigeerida oma hinnapakkumise eeldatavat tulu või kasumlikkust, tuginedes soovitud ühiku hinnale, allahindluse summale, allahindluse protsendile, kogusummale, marginaalile või kasumiprotsendile.   Kui olete sihtarvudega rahul, rakendage soovitus hinnapakkumise reale ja selle hinnaga seotud välju värskendatakse vastavalt.  
    * Saate luua soovitud arvu hinnasimulatsioone. Kui klõpsate nuppu Uus, kopeeritakse selle pakkumise rea hinnatingimused lehele. Seejärel saate muuta hinnaga seotud väljade väärtused sihtväärtusteks. Ühe välja muutmine käivitab kõigi teiste väljade ümberarvutamise. Et süsteem saaks arvutada müügimarginaali ja kasumiprotsendi, peab toote ühiku omahind teada olema. Vaadake vahekaardilt Simuleeritud hinnad algseid hindu, soovitatavaid muudatusi ja nende mõju hinnapakkumise kogusummadele.   Reeglina, kui hinnapakkumise reale rakendatakse simulatsioon, mis määrab uue summa, arvutab süsteem uue väärtuse ja sisestab selle väljale Ühiku hind. Kui simulatsioon põhineb uuel marginaalil või kasumiprotsendil, muudetakse ainult välja Netosumma ja Ühiku hind on tühi. Mõlemal juhul kustutatakse kõik allahindlused, mis olid enne simulatsiooni pakkumise real.  
17. Sulgege leht.
18. Klõpsake toimingupaanil valikut Pakkumine.
19. Klõpsake käsku Saada pakkumine.
20. Tehke väljal Hinnapakkumise printimine valik Jah.
21. Klõpsake nuppu OK.
    * Aruande koostamine võib minuti aega võtta. Ärge sulgege lehte enne, kui see on valmis.  
22. Sulgege leht.

## <a name="update-a-sales-quotation"></a>Müügipakkumise värskendamine
1. Klõpsake tegumiribal valikut Järeltegevus.
2. Klõpsake valikut Teisenda kliendiks.
3. Sisestage väärtus väljale Kliendi konto.
4. Klõpsake nuppu Kontrolli.
    * Veenduge, et näete sõnumit, et sisestatud konto number on kasutamiseks vaba.  
5. Klõpsake nuppu OK.
    * Süsteem on nüüd loonud hinnapakkumise potentsiaalsele kliendile uue kliendikonto.  
6. Sulgege leht.
7. Klõpsake tegumiribal valikut Järeltegevus.
8. Klõpsake käsku Kinnita.
9. Valige või sisestage väärtus väljal Põhjus.
10. Klõpsake nuppu OK.
11. Klõpsake toimingupaanil valikut Üldine.
12. Klõpsake valikut Müügitellimused.
13. Sulgege leht.

