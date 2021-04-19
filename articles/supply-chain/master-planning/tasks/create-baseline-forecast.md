---
title: Alusprognoosi loomine
description: Tootmise planeerija saab luua alusprognoosi, kasutades kas ajaseeria prognoosimudeleid või kopeerides ajaloolise nõudluse.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d89219d90ddff7cec70195025ffc361fb8101552
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841715"
---
# <a name="create-a-baseline-forecast"></a>Alusprognoosi loomine

[!include [banner](../../includes/banner.md)]

Tootmise planeerija saab luua alusprognoosi, kasutades kas ajaseeria prognoosimudeleid või kopeerides ajaloolise nõudluse. See protseduur näitab, kuidas kopeerida ajaloolist nõudlust, et luua alusprognoos kõigi toodete puhul, mis kasutavad ühte kauba eraldamisvõtit. 


## <a name="set-up-an-item-allocation-key"></a>Kauba eraldamisvõtme seadistamine
1. Avage Koondplaneerimine > Seadistus > Kontsernisisesed plaanimisgrupid.
2. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks saate filtrida välja Nimi väärtuse 10 järgi.
    * Nõudluse prognoos töötab juriidiliste isikute vahel. Seetõttu peate seadistama kõik ettevõtted, mille puhul soovite ühes kontsernisiseses plaanimisgrupis prognoose luua.  
3. Otsige loendist ja valige soovitud kirje.
4. Klõpsake suvandit Kauba eraldamisvõtmed.
    * Valige kõik kauba eraldamisvõtmed, mille puhul soovite prognoose luua.  
5. Märkige loendis valitud rida.
    * Valige kauba eraldamisvõti D_Aloc.  
6. Klõpsake >.
7. Sulgege leht.
8. Sulgege leht.

## <a name="set-up-the-demand-forecasting-parameters"></a>Nõudluse prognoosiparameetrite seadistamine
1. Avage Koondplaneerimine > Seadistus > Nõudluse prognoos > Nõudluse prognoosiparameetrid.
2. Laiendage jaotist Prognoosi algoritmi parameetrid.
3. Valige väljal Prognoosi koostamise strateegia suvand Kopeeri ajalooline nõudlus ümber.
4. Klõpsake nuppu Salvesta.

## <a name="create-a-baseline-forecast"></a>Alusprognoosi loomine
1. Avage Koondplaneerimine > Prognoosimine > Nõudluse prognoos > Statistilise alusprognoosi loomine.
2. Sisestage kuupäev väljale Alguskuupäev.
    * Kui teil on müügitellimusi alates 1. jaanuarist 2015, sisestage see kuupäev. Kui pole, sisestage müügitellimuste varaseim kuupäev.  
3. Sisestage kuupäev väljale Lõpukuupäev.
    * Sisestage müügitellimuste viimane kuupäev, näiteks 31.03.2015.  
4. Sisestage kuupäev väljale Alguskuupäev.
    * Sisestage 01.04.2015. See kuupäev arvutatakse automaatselt järgmise prognoosi vahemiku alguskuupäevana.  
5. Jaotise kaasamiseks laiendage kirjeid.
6. Klõpsake käsku Filtreeri.
7. Märkige loendis valitud rida.
    * Märkige rida, kus väli = Kontsernisisene plaanimisgrupp.  
8. Sisestage väärtus väljale Kriteeriumid.
    * Sisestage kontsernisisene plaanimisgrupp, nt 10, mida kasutasite esimeses ülesandes.  
9. Otsige loendist ja valige soovitud kirje.
    * Valige rida, kus väli = Kauba eraldamisvõti.  
10. Sisestage väärtus väljale Kriteeriumid.
11. Klõpsake nuppu OK.
12. Laiendage jaotist Täpsemad parameetrid.
13. Valige väljal Prognoosi vahemik suvand Kuu.
14. Sisestage väljale Prognoosi periood väärtus 3.
15. Sisestage väljale Ajapiiri külmutamine väärtus 1.
16. Klõpsake nuppu OK.

## <a name="visualize-the-demand-forecast"></a>Nõudluse prognoosi visualiseerimine
1. Avage Koondplaneerimine > Prognoosimine > Nõudluse prognoos > Korrigeeritud nõudluse prognoos.
2. Valige koondtabelis lahter reas 1 ja veerus 2. See on teine kuu, mille jaoks olete prognoosi loonud.
3. Määrake lahtri QtyCell väärtuseks 400.
    * Sisestage lahtrisse prognoositust teistsugune number, nt 400.  
4. Olete prognoosi käsitsi korrigeerinud. Pöörake tähelepanu järgmises etapis olevale graafilisele näidikule.
5. Klõpsake suvandit Prognoosi rea andmed.
    * Sellel lehel näete täpsuse väärtusi, ajaloolist nõudlust ja prognoosi. Saate ka prognoosi muuta.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]