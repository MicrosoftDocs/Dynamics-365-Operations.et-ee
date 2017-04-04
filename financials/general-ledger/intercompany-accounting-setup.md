---
title: Kontserni arvestuse seadistamine
description: "Selles artiklis käsitletakse loodud kontserni raamatupidamise nii, et saate kasutada IC-žurnaalides pearaamatu eraldised ja rahalise töölehtedele, päevased töölehed, hankija arve töölehtedel ja Maksežurnaalid."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 5fd279327013f26230146be38e23e9955c6f12c7
ms.lasthandoff: 03/31/2017


---

# <a name="intercompany-accounting-setup"></a>Kontserni arvestuse seadistamine

Selles artiklis käsitletakse loodud kontserni raamatupidamise nii, et saate kasutada IC-žurnaalides pearaamatu eraldised ja rahalise töölehtedele, päevased töölehed, hankija arve töölehtedel ja Maksežurnaalid.

IC-žurnaalides loomist mitmesugustel juhtudel, näiteks päevased töölehed, hankija arve töölehtedega, pearaamatu eraldised ja tsentraliseeritud maksed. Nende stsenaariumide lubamiseks peate seadistama kontsernisisese raamatupidamise.

## <a name="define-main-accounts"></a>Määratleda keskne raamatupidamine
Esmalt tuleb luua kontsernisisesed põhikontod, et kasutada makse saaja ja maksja raamatupidamiskirjeid. Iga ettevõtte jaoks tasub kasutada kordumatuid põhikontosid, et hõlbustada kontsernisiseste raamatupidamiskirjete tasakaalustamist ja likvideerimist. Kui kasutate IC poole äripartneri või vastutasu dimensiooni, saate määratleda peamine konto raamatupidamises ettevõtetevaheliste määratletud fikseeritud dimensioon selle dimensiooni. Keskne raamatupidamine seadistamisel peate seadma selle **Main liik** välja **bilansi** kohta on **Main kontode** lehekülg.

## <a name="define-journal-names"></a>Määratleda nimesid
Järgmisena tuleb määratleda töölehe nimi. Määra ning **tüüp** välja **päevas** kohta on **nimesid** lehekülg. Kontsernisiseseks raamatupidamiseks tasub kasutada kindlat töölehe nime.

## <a name="define-intercompany-accounting-setup"></a>Määratleda kontsernisisese arvestuse seadistamine
Selle **kontserni raamatupidamise** lehel saab luua teostada tehing juriidiliste isikute paarid omavahel. Arvestuse seadistamine kontsernisisese jagatakse nii, et seadistus on nähtavad jooksul juriidilised isikud. Uus juriidiline isik kahe loomisel tagama, et sa oled teadlik, milline juriidiline isik mõistetakse koostanud firma versus sihtkoha firma. Kui sisestate IC-tehinguid, määrab tehingu algatamise või pärit tehingu mis juriidiline isik. Näiteks seadistatakse kontserni raamatupidamise USMF (pärit) ja USSI (sihtkoht). Kui kasutaja on USSI ja siseneb IC-tehing koos USMF, tehing ei postita sest kontserni raamatupidamise määratletakse vaid USMF on algataja. Kui kas firma saab pärinevad tehingu, peate Loo teine juriidiline isik paar vastastikuse seadistamiseks. 

Valige selle **konto debiteerimiseks (nõuded)** ja **krediidi konto (tõttu)** nii lähte- ja juriidilisel isikul. Määratleda, mis **töölehe nimi** kasutatakse kande loomisel sihtkoha ettevõttes. Töölehe koostanud äriühingu on juba teada, sest see on kasutaja valitud IC-tehingu loomiseks. 

Lõpuks, Vali, milline juriidiline isik saab toetamiseks summasid nagu skonto või tsentraliseeritud maksete realiseeritud tulude/kulude arvestus. 

Vastastikune suhe saab seadistada hõlpsasti linna ning **kontserni raamatupidamise** lehe abil selle **luua vastastikusest** nuppu esimene paar juriidiline isik on loodud. Vastastikune paari loomisel kopeeritakse sihtkoha ettevõtte teave pärit firma ja vastupidi. Sihtkoha ettevõtte määratletud töölehe jääb. Enamikus organisatsioonides kasutada sama nimetamistava nende töölehtede nimed, et töölehe nimi on sama. Kui töölehe nimi on erinev, ilmub hoiatus välja, et teavitada teid, et tööleht pole olemas ja saab valida eri žurnaali.


