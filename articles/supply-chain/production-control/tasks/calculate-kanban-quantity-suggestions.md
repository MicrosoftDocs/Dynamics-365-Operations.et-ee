---
title: Kanban-koguse soovituste arvutamine
description: See protseduur keskendub kanban-suuruse ja koguste optimeerimisele konkreetse kanban-reegli puhul, kasutades kanban-koguse arvutamist.
author: ChristianRytt
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 409903740413994fead3f65b12afb414ca5c43ed
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255393"
---
# <a name="calculate-kanban-quantity-suggestions"></a>Kanban-koguse soovituste arvutamine

[!include [banner](../../includes/banner.md)]

See protseduur keskendub kanban-suuruse ja koguste optimeerimisele konkreetse kanban-reegli puhul, kasutades kanban-koguse arvutamist. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. See protseduur on mõeldud väärtuse voo haldurile. See on eeltingimus, et olete lõpetanud protseduuri Kanban-koguse arvutuspoliitika lisamine kanban-reeglile.


## <a name="create-a-kanban-quantity-calculation"></a>Kanban-koguse arvutamise loomine
1. Avage Tootmise juhtimine > Perioodilised ülesanded > Kanban-koguse arvutamine > Kanban-koguse arvutamine.
2. Klõpsake valikut Uus.
3. Sisestage väljale Nimi suvand Speaker2016.
4. Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.
    * Valige poliitika, mille olete loonud protseduuris Uue kanban-koguse arvutuspoliitika lisamine kanban-reeglile. Näiteks sisestage Speaker2016.  
5. Klõpsake loendis valitud real olevat linki.
6. Seadistage kuupäev ja kellaaeg väljal Reegli kehtivuse alguskuupäev väärtusele 2012-12-17T08:00:00.
    * See kuupäev on nende fikseeritud kanban-reeglite määratlemise aluseks, mis lisatakse kanban-koguse arvutamisse.  
7. Seadistage kuupäev ja kellaaeg väljal Täidetud nõudlusperioodi alguskuupäev väärtusele 2012-11-17T09:00:00.
    * Alguskuupäev, kui möödunud nõudluse kanded lisatakse kanban-koguse arvutamiseks.  
8. Seadistage kuupäev ja kellaaeg väljal Täidetud nõudlusperioodi lõppkuupäev väärtusele 2012-12-17T07:59:59.
    * Lõppkuupäev, milleni möödunud nõudluse kanded lisatakse kanban-koguse arvutamiseks.  
9. Seadistage kuupäev ja kellaaeg väljal Nõudlusperioodi alguskuupäev väärtusele 2012-12-17T08:00:00.
    * Alguskuupäev, millest alates praeguse nõudluse kanded lisatakse kanban-koguse arvutamiseks.  
10. Seadistage kuupäev ja kellaaeg väljal Nõudlusperioodi lõppkuupäev väärtusele 2013-01-16T07:59:59.
    * Lõppkuupäev, milleni praeguse nõudluse kanded lisatakse kanban-koguse arvutamiseks.  

## <a name="generate-kanban-quantity-proposal"></a>Kanban-koguse soovituse loomine
1. Klõpsake nuppu Salvesta.
2. Klõpsake suvandit Loo.
    * See loob kanban-koguse soovituse rea kanban-reegli 000020 puhul.  

## <a name="run-kanban-quantity-calculation"></a>Kanban-koguse arvutamise käivitamine
1. Klõpsake valikut Arvuta.
    * See arvutab kanban-koguse soovituse.  
2. Klõpsake nuppu OK.
3. Märkige loendis valitud rida.
    * Pange tähele, et soovitatud kanban-kogus on 2.  

## <a name="change-product-quantity-and-calculate-again"></a>Toote koguse muutmine ja uuesti arvutamine
1. Määrake toote koguseks 5.
2. Klõpsake valikut Arvuta.
3. Klõpsake nuppu OK.
    * Pange tähele, et kanban-kogusega 5 muudetakse soovitus kanban-kogusele 4.  
    * Põhjuseks on see, et väiksema toote kogusega on nõudluse täitmiseks vaja rohkem kanbane.  

## <a name="update-kanban-rule"></a>Kanban-reegli värskendamine
1. Sisestage kuupäev ja kellaaeg väljale Reegli jõustumiskuupäev.
    * Määrake suvandi Reegli kehtivuse alguskuupäev puhul kuupäev tulevikku. Näiteks täna + üks aasta.  
2. Klõpsake käsku Uuenda.
3. Klõpsake nuppu OK.
4. Sulgege leht.

## <a name="validate-change-on-kanban-rule"></a>Kanban-reegli muudatuse kinnitamine
1. Avage Tooteteabe haldus > Lean manufacturing > Kanban-reeglid.
2. Klõpsake loendis valitud real olevat linki.
    * Valige eelmises alamülesandes loodud kanban-reegel. See peaks olema loendi esimene kanban-reegel, mis on sorditud numbri järgi.  
3. Laiendage jaotist Üksikasjad.
    * Pange tähele jõustumiskuupäeva, mis tähendab, et seda reeglit ei aktiveerita kuni selle kuupäevani.  
4. Laiendage jaotist Kogused.
    * Pange tähele, et see on kanban-koguse arvutamisse sisestatud vaikekogus.  
    * Pange tähele, et see on fikseeritud kanban-kogus 4 kanban-koguse arvutamisest.  
5. Klõpsake vahekaarti ListPanel.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]