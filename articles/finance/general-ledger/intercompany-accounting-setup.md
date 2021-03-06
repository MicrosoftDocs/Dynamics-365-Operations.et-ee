---
title: Kontsernisisese raamatupidamise seadistus
description: Selles teemas selgitatakse, kuidas seadistada kontsernisisest raamatupidamist nii, et saaksite kasutada kontsernisiseseid töölehti pearaamatueraldiste ja finantstöölehtede (nt igapäevaste töölehtede, hankija arve töölehtede ja maksetöölehtede) jaoks.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: roschlom
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f74a70c5db4f70b9850fb5093f1afea2a4f7240
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826590"
---
# <a name="intercompany-accounting-setup"></a>Kontsernisisese raamatupidamise seadistus

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas seadistada kontsernisisest raamatupidamist nii, et saaksite kasutada kontsernisiseseid töölehti pearaamatueraldiste ja finantstöölehtede (nt igapäevaste töölehtede, hankija arve töölehtede ja maksetöölehtede) jaoks.

Kontserni töölehed saab luua mitmesugustes stsenaariumides, näiteks igapäevaste töölehtede, hankija arve töölehtede, pearaamatu eraldiste ja tsentraliseeritud maksete jaoks. Nende stsenaariumide lubamiseks peate seadistama kontsernisisese raamatupidamise.

## <a name="define-main-accounts"></a>Põhikontode määratlemine
Esmalt tuleb luua kontsernisisesed põhikontod, et kasutada makse saaja ja maksja raamatupidamiskirjeid. Iga ettevõtte jaoks tasub kasutada kordumatuid põhikontosid, et hõlbustada kontsernisiseste raamatupidamiskirjete tasakaalustamist ja likvideerimist. Kui kasutate kontsernisisese osapoole tuvastamiseks äripartneri või ekvivalendi dimensiooni, saate määratleda selle dimensiooni kontsernisiseses raamatupidamises määratletud põhikonto fikseeritud dimensioonina. Põhikontode seadistamisel tuleb lehel **Põhikontod** määrata välja **Põhikonto tüüp** väärtuseks **Bilanss**.

## <a name="define-journal-names"></a>Töölehenimede määratlemine
Järgmisena tuleb määratleda töölehe nimi. Määrake lehel **Töölehenimed** välja **Töölehe tüüp** väärtuseks **Igapäevane**. Kontsernisiseseks raamatupidamiseks tasub kasutada kindlat töölehe nime.

## <a name="define-intercompany-accounting-setup"></a>Kontsernisisese raamatupidamise seadistuse määratlemine
Lehte **Kontsernisisene raamatupidamine** kasutatakse juriidiliste isikute paaride loomiseks, kes saavad üksteisega tehinguid teha. Kontsernisisese raamatupidamise seadistus on ühiskasutuses, mis tähendab, et seadistus on näha kõigist juriidilistest isikutest. Uue juriidiliste isikute paari loomisel veenduge, et oleksite teadlik, milline juriidiline isik on määratud sihtettevõtte suhtes lähte-ettevõtteks. Kontsernisisestesse kannetesse sisenemisel määrab kanne, milline juriidiline isik kande algatab või on kande lähtepunktiks. Näiteks seadistatakse kontsernisisene raamatupidamine USMF-i (lähtepunkt) ja USSI (sihtpunkt) jaoks. Kui kasutaja on USSI-s aktiivne ja teeb USMF-iga kontsernisisese kande, siis kannet ei sisestata, kuna kontsernisiseses raamatupidamises on USMF määratletud ainult lähtepunktina. Kui kumbki ettevõte võib kande algatada, on vaja mõlemapoolse seadistuse jaoks luua teine juriidiliste isikute paar. 

Valige **Deebetkonto (maksja)** ja **Kreeditkonto (vastuvõtja)** nii algatava kui ka vastuvõtva juriidilise isiku jaoks. Määratlege, millist **töölehe nime** kasutatakse, kui sihtettevõttes kanne luuakse. Lähteettevõtte tööleht on juba teada, kuna kasutaja valis selle kontsernisisese kande loomisel. 

Lõpuks valige, millise juriidilise alla paigutatakse tugisummade arvestus (nt skonto või realiseeritud kasum/kahjum) tsentraliseeritud maksete puhul. 

Vastastikuse seose saab lehel **Kontsernisisene raamatupidamine** hõlpsasti seadistada, kasutades nuppu **Loo vastastikune seos** pärast esimese juriidiliste isikute paari loomist. Kui vastastikune paar on loodud, kopeeritakse sihtettevõtte andmed lähteettevõttele ja vastupidi. Sihtettevõttele määratletud tööleht jääb alles. Enamik organisatsioone kasutab oma töölehenimede jaoks sama nime andmise süsteemi, et töölehe nimi oleks sama. Kui töölehe nimi on erinev, kuvatakse väljal hoiatus, mis ütleb, et töölehte pole olemas, ja saab valida teise töölehe.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]