---
title: TDS-i arvutamine kontsernisisestelt kannetelt
description: Selles teemas kirjeldatakse protsessi, mida kasutatakse allikas (TDS) maha arvatud maksu arvutamiseks kontsernisisestel kannetel faasides.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 029a9bcc6fad7bc3348716aadeeda9552a086e5b1a6d08018c1aaced4b241a1d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727245"
---
# <a name="tds-calculation-on-intercompany-transactions"></a>TDS-i arvutamine kontsernisisestelt kannetelt

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse protsessi, mida kasutatakse allikas (TDS) maha arvatud maksu arvutamiseks kontsernisisestel kannetel faasides.

Kontsernisisese ostutellimuse või müügitellimuse loomisel kasutatakse TDS-i summa arvutamiseks kliendile või hankijale määratud TDS-i vaikegruppi. TDS-i summa sisestatakse tagasisaadav või ostureskontrole pärast arve sisestamist.

Algsele ostutellimusele või müügitellimusele luuakse automaatselt kontsernisisene müügi- või ostutellimus. TDS-i vaikegrupp kuvatakse kontsernisisesel tellimusel nii, et TDS-i saab arvutada. Saate sisseostjate gruppi muuta. Arve saab sisestada ainult siis, kui automaatselt loodud kontsernisisese tellimuse arve netosumma vastab algsel tellimusel olevale arve netosummale. (Netosumma on arve summa pärast TDS-i mahaarvamist.)

Näiteks müügiarve luuakse summale 50 000 ja sellega on seotud **10%** TDS-grupist. Sisestatud arve summa on 45 000 ja müügiarve sisestatud TDS-i summa on 5000. Kontsernisisese müügitellimuse jaoks luuakse ostutellimus automaatselt ning sellega on seotud **10%** TDS-grupist. Kui muudate TDS-grupi **15%** ei saa arvet sisestada, kuna automaatselt loodud kontsernisisese müügitellimuse arve netosumma ei vasta algse müügitellimuse arve netosummale.

Automaatselt sisestatakse kontsernisisese arve jaoks loodud maksetööleht. Maksetöölehte saab sisestada ainult siis, kui selle netomakse summa ühtib algse maksetöölehe netomakse summaga.
