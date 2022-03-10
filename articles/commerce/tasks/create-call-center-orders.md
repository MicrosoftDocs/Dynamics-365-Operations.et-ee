---
title: " Kõnekeskuse tellimuste loomine"
description: See protseduur juhendab kliendi otsimisel, uue tellimuse loomisel, toote otsimisel ja kliendilt makse vastuvõtmisel.
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 78cccabb206d938b850e70b7e8057e20cc6158e1d154fc4876de7918dbe44d87
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730655"
---
# <a name="create-call-center-orders"></a> Kõnekeskuse tellimuste loomine

[!include [banner](../includes/banner.md)]

See protseduur juhendab kliendi otsimisel, uue tellimuse loomisel, toote otsimisel ja kliendilt makse vastuvõtmisel. See protseduur kasutab ettevõtte USRT demoandmeid ja on mõeldud müügitellimuste ametnikule. Eeltingimused: kasutaja, kes viib protseduuri lõpule, häälestatakse kõnekeskuse kasutajana ja Fabrikami poolaastakataloogis avaldatakse vähemalt üks lähtekood.

1. Avage **Jaemüük ja kaubandus \> Kliendid \> Klienditeenindus**.
2. Sisestage väljale **SearchText** otsingukriteeriumid kliendi leidmiseks.
    * Selleks näidisprotseduuriks sisestage „Karen” ja valige **Vahekaart**.  
3. Valige Otsi.
    * Kuna demoandmetes on ainult ühe kliendi nimi Karen, valitakse tulemus automaatselt.  
4. Valige **Uus müügitellimus**.
5. Laiendage või ahendage jaotise **Müügitellimus** päiseosa.
6. Valige kataloogi jaoks lähtekood.
    * Kui ühtegi aktiivset lähtekoodi ei ole, saab selle etapi vahele jätta.  
7. Valige **Lisa rida**.
8. Sisestage väljale **Kaubakood** kauba otsingusõna.
    * Selleks näidisprotseduuriks sisestage osaline kaubakood 8111 ja vajutage vahekaarti. See tegevus avab kauba otsinguakna.  
9. Valige toode müügitellimusele lisamiseks.
10. Sisestage müügikogus.
11. Valige **Loo**.
12. Klõpsake kliendi makse vastuvõtmiseks nuppu Complete **Valmis**.
13. Valige **Lisa**.
    * Lisamise link on vahekaardil Payments (Maksed). Laiendage maksete vahekaarti, kui see on kokku pandud.  
14. Valige makseviis.
    * Valige selle protseduuri jaoks sularaha maksemeetod.  
15. Sulgege leht.
16. Sisestage summa.
    * Sisestage selle protseduuri jaoks summa, mis on võrdne tellimuse saldoga, mis on nähtav müügitellimuse kokkuvõtte lehel summa väljast vasakul pool. See tegevus võimaldab teil tellimuse täielikult tasutuna lõpule viia.  
17. Valige nupp **OK**.
18. Valige käsk **Esita**.

## <a name="additional-resources"></a>Lisaressursid

[Tehingumeilide kohandamine tarneviisi alusel](../customize-email-delivery-mode.md)

[Kassas tarneviisi muutmine](../pos-change-delivery-mode.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]