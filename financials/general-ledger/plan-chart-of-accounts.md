---
title: Kontoplaani kavandamine
description: Selles artiklis antakse teavet, mis aitab teil planeerida organisatsiooni kontoplaane.
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: c4f5dae90c5fcaaa52a7087d7c20b2de343b7da0
ms.openlocfilehash: 424ea5ce12d51d384c86878b7d2199bcd52c40f8
ms.contentlocale: et-ee
ms.lasthandoff: 08/01/2017

---

# <a name="plan-your-chart-of-accounts"></a>Kontoplaani kavandamine

[!include[banner](../includes/banner.md)]


Selles artiklis antakse teavet, mis aitab teil planeerida organisatsiooni kontoplaane.

Organisatsiooni finantsteabe jälgimiseks ja säilitamiseks saate seadistada kontoplaani. Kontoplaan on finantsraamistikku määratlevate kontode kogum. Nende kontode kannete edasiseks jälgimiseks saate lisada segmente, mida nimetatakse finantsdimensioonideks. Näiteks võib kulukonto sisaldada finantsdimensioone nimedega Osakond, Kulukeskus ja Eesmärk. Kasutaja määratud reeglid, mida nimetatakse konto struktuurideks ja täpsemateks reegliteks, määravad, kuidas finantsdimensioonid on seotud põhikontode ja muude finantsdimensioonidega ning kuidas kandeid sisestatakse. 

Kontoplaan on juriidilise isiku pearaamatukontode struktureeritud loend. Seda loendit kasutatakse ametivõimudele ja omanikele finantsaruannete ettevalmistamiseks. Kontod on grupeeritud kontotüüpide järgi ja seejärel koondatud suurematesse kategooriatesse. Kõige üldisemal tasandil on kontod grupeeritud tulude ja kuludena (kasutusel olevad kontod) ning varade ja kohustustena (bilansikontod). 

Kontoplaani saavad jagada ja kasutada kõik organisatsiooni juriidilised isikud. Kontoplaan, mida juriidiline isik kasutab, on määratletud lehel **Pearaamat**. 

Järgmiselt on toodud mõni tegur, millega peate oma organisatsiooni kontoplaani struktuuri plaanimisel arvestama.

-   Organisatsiooni riigi/regiooni aruandluse nõuded
-   Teie juriidilise isiku aruandluse nõuded
-   Nõutav üksikasjalik täpsustustase nii muude organisatsioonide kui ka teie organisatsiooni jaoks

Looge kontoplaan lehel **Kontoplaan**. Põhikontosid saab luua lehel **Kontoplaan** või lehel **Põhikontod**. Põhikontodel ei tohiks kasutada erimärke, mida kasutatakse kontoplaani eraldajatena. Erimärgi olemasolul, mis vastab teie kontoplaani eraldajale, võib konto ja dimensiooni kombinatsioonide sisestamisel ilmneda ebastabiilsus või olla alati vaja otsinguid või hüpikut kasutada. Lisateabe jaoks vt [Põhikonto loomine](tasks/create-account-structures.md).


Soovitatav on siduda põhikontod põhikonto kategooriatega, nii et saate kasutada vaikimisi finantsaruandeid ega pea muudatusi tegema. Seetõttu saate aruandeid kiiremini ja hõlpsamini kujundada ja säilitada. 

Kasutage konto struktuuride loomiseks lehte **Konto struktuuride konfigureerimine**. Konto struktuurid määratlevad kehtivaid kombinatsioone. Need kombinatsioonid koos põhikontodega moodustavad kontoplaani.  Lisateabe jaoks vt [Konto struktuuride loomine](tasks/create-main-account.md).

**Juriidilise isiku alistamised** 

Kõik põhikontod ei kehti kõikide juriidiliste isikute puhul ja mõned võivad olla asjakohased ainult konkreetse ajaperioodi puhul. Sellisel juhul saab jaotist Juriidilise isiku alistamised kasutada tuvastamaks, milliste ettevõtete põhikonto tuleks peatada, kes on omanik ja mis ajaperioodil on dimensioon aktiivne. Ühiskasutuse tasandil alistamised ei saa olla piiravamad kui alistamised juriidilise isiku tasandil.

Lisateavet saate lugeda järgmistest teemadest. [Finantsdimensioonid](financial-dimensions.md)
[Täpsemate reegli struktuuride loomine ja määramine](tasks/create-assign-advanced-rule-structures.md)




