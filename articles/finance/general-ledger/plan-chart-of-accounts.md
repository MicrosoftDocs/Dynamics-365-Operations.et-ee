---
title: Kontoplaanide plaanimine
description: Selles artiklis antakse teavet, mis aitab teil planeerida organisatsiooni kontoplaane.
author: aprilolson
ms.date: 04/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10906d7b30628dfe69907cfa69ae1022fde33243
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070630"
---
# <a name="plan-your-chart-of-accounts"></a>Kontoplaanide plaanimine

[!include [banner](../includes/banner.md)]

Selles artiklis antakse teavet, mis aitab teil planeerida organisatsiooni kontoplaane.

Organisatsiooni finantsteabe jälgimiseks ja säilitamiseks saate seadistada kontoplaani. Kontoplaan on finantsraamistikku määratlevate kontode kogum. Nende kontode kannete edasiseks jälgimiseks saate lisada segmente. Neid segmente nimetatakse finantsdimensioonideks. Näiteks võib kulukonto sisaldada finantsdimensioone nimedega Osakond, Kulukeskus ja Eesmärk. Kasutaja määratud reeglid määravad, kuidas finantsdimensioonid on seotud põhikontode ja muude finantsdimensioonidega ning kuidas kandeid sisestatakse. Neid kasutaja määratud reegleid nimetatakse konto struktuurideks ja täpsemateks reegliteks.

Kontoplaan on juriidilise isiku pearaamatukontode struktureeritud loend. Seda loendit kasutatakse ametivõimudele ja omanikele finantsaruannete ettevalmistamiseks. Kontod grupeeritakse kõigepealt kontotüüpide järgi ja seejärel koondatakse suurematesse kategooriatesse. Kõige üldisemal tasandil on kontod grupeeritud tulude ja kuludena (kasutusel olevad kontod) ning varade ja kohustustena (bilansikontod).

Kontoplaani saavad jagada ja kasutada kõik organisatsiooni juriidilised isikud. Kontoplaan, mida juriidiline isik kasutab, on määratletud lehel **Pearaamat**.

Järgmiselt on toodud mõni tegur, millega peate oma organisatsiooni kontoplaani struktuuri plaanimisel arvestama.

- Organisatsiooni riigi või regiooni aruandluse nõuded
- Teie juriidilise isiku aruandluse nõuded
- Nõutav üksikasjalik täpsustustase nii muude organisatsioonide kui ka teie organisatsiooni jaoks

Saate luua kontoplaani lehel **Kontoplaan**. Saate luua põhikontosid lehel **Kontoplaan** või lehel **Põhikontod**. Põhikontodel ei tohiks kasutada erimärke, mida kasutatakse kontoplaani eraldajatena. Vastasel juhul võib konto ja dimensiooni kombinatsioonide sisestamisel ilmneda ebastabiilsus või vajalik olla alati otsingute või dialoogiboksi kasutamine. Lisateabe jaoks vt [Põhikonto loomine](tasks/create-main-account.md).

> [!NOTE]
> Dynamics 365 Finance versioonis 8.0 (2018 **. aprill) saate muuta kontoplaani eraldaja pearaamatu parameetrite lehelt**.

Soovitatav on siduda põhikontod põhikonto kategooriatega, nii et saate kasutada vaikimisi finantsaruandeid ega pea muudatusi tegema. Seetõttu saate aruandeid kiiremini ja hõlpsamini kujundada ja säilitada.

Saate luua konto struktuure lehel **Konto struktuuride konfigureerimine**. Konto struktuurid määratlevad kehtivaid kombinatsioone. Need kombinatsioonid koos põhikontodega moodustavad kontoplaani. Lisateabe jaoks vt [Konto struktuuride loomine](tasks/create-account-structures.md).

**Juriidilise isiku alistamised**

Kõik põhikontod ei kehti kõikide juriidiliste isikute puhul ja mõni põhikonto võib olla asjakohased ainult konkreetse perioodi puhul. Sel juhul saab kasutada jaotist **Juriidilise isiku tühistamised** tuvastamiseks, milliste ettevõtete põhikonto tuleks peatada, kes on omanik ja mis ajaperioodil on dimensioon aktiivne. Ühiskasutuse tasandil alistamised ei saa olla piiravamad kui alistamised juriidilise isiku tasandil.

Lisateavet vt järgmistest teemadest:

- [Finantsdimensioonid](financial-dimensions.md)
- [Täpsemate reeglistruktuuride loomine ja määramine](tasks/create-assign-advanced-rule-structures.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

