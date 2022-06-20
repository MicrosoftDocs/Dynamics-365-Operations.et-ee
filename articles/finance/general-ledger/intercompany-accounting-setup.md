---
title: Kontsernisisese raamatupidamise häälestus
description: See artikkel selgitab, kuidas seadistada kontserni raamatupidamist nii, et saate kasutada kontsernisiseseid töölehti pearaamatueraldiste ja finantstöölehtede, nt igapäevaste töölehtede, hankijaarvete töölehtede ja maksetöölehtede jaoks.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 309c121c1ef4b3814d676cad6f3c2b6826b59843
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871213"
---
# <a name="intercompany-accounting-setup"></a>Kontsernisisese raamatupidamise häälestus

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas seadistada kontserni raamatupidamist nii, et saate kasutada kontsernisiseseid töölehti pearaamatueraldiste ja finantstöölehtede, nt igapäevaste töölehtede, hankijaarvete töölehtede ja maksetöölehtede jaoks.

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
