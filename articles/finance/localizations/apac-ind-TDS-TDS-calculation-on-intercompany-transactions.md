---
title: TDS-i arvutamine kontsernisisestelt kannetelt
description: See artikkel kirjeldab protsessi, mida kasutatakse allikas (TDS) maha arvatud maksu arvutamiseks kontsernisisestel kannetel faasides.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: c27bea997804f2c5eff6be2b20064b272ccd062f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888969"
---
# <a name="tds-calculation-on-intercompany-transactions"></a>TDS-i arvutamine kontsernisisestelt kannetelt

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab protsessi, mida kasutatakse allikas (TDS) maha arvatud maksu arvutamiseks kontsernisisestel kannetel faasides.

Kontsernisisese ostutellimuse või müügitellimuse loomisel kasutatakse TDS-i summa arvutamiseks kliendile või hankijale määratud TDS-i vaikegruppi. TDS-i summa sisestatakse tagasisaadav või ostureskontrole pärast arve sisestamist.

Algsele ostutellimusele või müügitellimusele luuakse automaatselt kontsernisisene müügi- või ostutellimus. TDS-i vaikegrupp kuvatakse kontsernisisesel tellimusel nii, et TDS-i saab arvutada. Saate sisseostjate gruppi muuta. Arve saab sisestada ainult siis, kui automaatselt loodud kontsernisisese tellimuse arve netosumma vastab algsel tellimusel olevale arve netosummale. (Netosumma on arve summa pärast TDS-i mahaarvamist.)

Näiteks müügiarve luuakse summale 50 000 ja sellega on seotud **10%** TDS-grupist. Sisestatud arve summa on 45 000 ja müügiarve sisestatud TDS-i summa on 5000. Kontsernisisese müügitellimuse jaoks luuakse ostutellimus automaatselt ning sellega on seotud **10%** TDS-grupist. Kui muudate TDS-grupi **15%** ei saa arvet sisestada, kuna automaatselt loodud kontsernisisese müügitellimuse arve netosumma ei vasta algse müügitellimuse arve netosummale.

Automaatselt sisestatakse kontsernisisese arve jaoks loodud maksetööleht. Maksetöölehte saab sisestada ainult siis, kui selle netomakse summa ühtib algse maksetöölehe netomakse summaga.
