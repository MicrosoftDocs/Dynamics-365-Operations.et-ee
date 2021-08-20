---
title: Väärtusmudelite seadistamine
description: See protseduur näitab, kuidas luua uut põhivara raamatut ja seostada seda põhivaragrupiga.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 923c3d0c7a2d54f616452a8b927681603f4955c2d7e5ff306971561b73355743
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741532"
---
# <a name="set-up-value-models"></a>Väärtusmudelite seadistamine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas luua uut põhivara raamatut ja seostada seda põhivaragrupiga. See kasutab USMF-i juriidilise isiku puhul raamatupidaja rolli ja demoandmeid.


## <a name="create-a-book"></a>Raamatu loomine
1. Avage Põhivarad > Seadistus > Raamatud.
2. Klõpsake valikut Uus.
3. Tippige väärtus väljale Raamat.
4. Sisestage väljale Kirjeldus soovitud väärtus.
    * Kui Kulumiarvestus on valitud, kaasatakse seostatud vara raamat kulumisoovitustesse. Kui see pole valitud, ei amortiseerita vara raamatut automaatselt.  
5. Tehke väljal Kulumiarvestus valik Jah.
6. Valige või sisestage väärtus väljal Kulumireeglid.
    * Alternatiivne kulumireegel on tuntud ka kui kulumi ümberlülitusmeetod. Kulumisoovitus lülitub sellele reeglile, kui alternatiivne reegel arvutab kulumi summa, mis on vaikimisi kulumireegliga võrdne või sellest suurem.  
    * Plaaniväliseid kulumireegleid kasutatakse vara täiendava kulumi arvestamiseks ebatavalistes olukordades. Näiteks võite seda kasutada loodusõnnetusest tuleneva kulumi registreerimiseks.  
    * Kui valitud on suvand Loo kulumi korrigeerimised koos aluse korrigeerimistega, luuakse kulumi korrigeerimised automaatselt, kui vara väärtust värskendatakse. Kui see valitud pole, mõjutab värskendatud vara väärtus ainult kulumi arvutusi alates tänasest.  
7. Tehke väljal Loo kulumi korrigeerimised koos aluse korrigeerimistega valik Jah.
    * Vaikimisi sisestatakse põhivara raamatu kanded pearaamatusse. Raamatu sisestamise pearaamatusse saab keelata, määrates valiku Sisesta pearaamatusse väärtuseks Ei. Raamatuid, mida pearaamatusse ei sisestata, kasutatakse tavaliselt maksuaruandluse jaoks. See lisab paindlikkust vararegistri varasemate kannete kustutamisel, kuna neid pole pearaamatuga kooskõlastatud.  
    * Sisestamiskihiks on vaikimisi Praegune kiht, kui raamat sisestatakse pearaamatusse, ja Pole, kui seda pearaamatusse ei sisestata. Värskendage sisestamiskihti, kui vajate selle raamatu kannete sisestamist teise kihti.  
8. Sisestage või valige väärtus väljal Kalender.
    * Tuletatud raamatud sisestavad kandeid korraga erinevatesse raamatutesse. Loote kanded peamises raamatus ja sisestamise ajal sisestatakse kande täpne koopia tuletatud raamatusse. Tuletatud raamatu kandeid ei arvutata ümber, seega ei tohiks seda kulumikannete jaoks kasutada.  

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Raamatu seostamine põhivaragrupiga
1. Klõpsake suvandit Põhivaragrupid.
2. Sisestage väärtus väljale Põhivara grupp või valige sellelt väljalt.
3. Sisestage number väljale Kasutusiga.
    * Pange tähele, et väärtus Kulumiperioodid arvutatakse pärast kasutusea seadistamist.  
    * Kulumiarvestusreeglit saab maksuarvestuse jaoks vajalikul viisil seadistada.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]