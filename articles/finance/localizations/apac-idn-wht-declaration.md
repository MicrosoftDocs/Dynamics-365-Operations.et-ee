---
title: Kinnipeetava maksu aruanne Indoneesia jaoks
description: See artikkel selgitab, kuidas indoneesias kinnipeetava maksu aruannet konfigureerida ja luua.
author: AdamTrukawka
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-12-02
ms.dyn365.ops.version: 10.0.20
ms.search.scope: ''
ms.openlocfilehash: 732db563532ebc46c7b9fc69c2aaa128640084f5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282431"
---
# <a name="withholding-tax-report-for-indonesia-id-00005"></a>Kinnipeetava maksu aruanne Indoneesia jaoks (ID-00005)

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas seadistada ja luua PPH kinnipeetava maksu faili, mida Indoneesia juriidilised isikud kasutavad kinnipeetavate kannete kohta aruande tegemiseks e-Sisestapot rakenduses.

Indoneesia maksuamet (DGT) määrab, et maksustatavad vihjed (PKP), mis on registreeritud KPP Pratamas tulumaksu (PPh) artikliga 23 ja/või artikliga 26, peavad elektrooniliselt esitama tulumaksutagastusaruande artiklid 23 ja 26, kasutades e-Eti rakendust. 

- **Artikkel 23** – aruanne sisaldab kõiki hankijate kinnipeetavaid kandeid, kus esmase aadressi riigi/regiooni kood on Indoneesia kood.
- **Artikkel 26** – aruanne sisaldab kõiki kinnipeetavaid kandeid hankijatest, kus esmase aadressi riigi/regiooni kood pole Indoneesia kood.

## <a name="prerequisites"></a>Eeltingimused

- Juriidilise isiku esmane aadress peab olema Indoneesias.
- Funktsioonihalduse **tööruumis** peab globaalse kinnipeetava **maksu funktsioon** olema lubatud. Lisateavet funktsioonide lubamise kohta, vaata [Funktsioonihalduse ülevaade.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

### <a name="download-electronic-reporting-configurations"></a>Elektroonilise aruandluse konfiguratsioonide allalaadimine

Impordifaili loomine põhineb elektroonilise aruandluse (ER) konfiguratsioonil. Lisateavet konfigureeritava aruandluse võimaluste ja mõistete kohta vaata [Eektroonilisest aruandlusest](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Tootmise ja kasutaja aktsepteerimise testimiseks (UAT) keskkondades [järgige juhiseid elektrooniliste aruandluse konfiguratsioonide allalaadimises elutsükli teenustest](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Impordifaili loomiseks laadige hoidlast üles järgmised konfiguratsioonid:

- **Maksudeklaratsiooni mudel.version.93.xml** või uuem versioon
- **Maksudeklaratsiooni mudeli vastendus.version.93.153.xml** või uuem versioon
- **Milline PPh-skeemi import (ID).version.93.14** või uuem versioon

## <a name="set-up-general-ledger-parameters"></a>Seadistage pearaamatu parameetrid

1. Minge maksu **seadistamise** \> **pearaamatu** \> **parameetritesse.**
2. Valige vahekaardi **Kinnipeetav** maks väljal **Mis deklaratsiooni vormingu vastendus**, **suvand Mis on PPh skeemi import (ID).** 
3. Minge **kinnipeetava** \> **maksu kinnipeetava** \> **·** \> **·** **maksu tulu tüüpi, et seadistada Kode Andmikuti Potongi** kinnipeetava maksu tulu tüüp ja seejärel määrake koodid seotud kauba kinnipeetava maksu gruppidele. Koodid on vajalikud integreerimisfaili loomiseks e-Hoidla rakendust kasutades. 

## <a name="generate-the-withholding-import-file"></a>Kinnipeetava impordi faili loomine

E-Kande faili ettevalmistamine ja loomine konkreetseks perioodiks põhineb kinnipeetava maksu kannetel, mis sisestati tasakaalustamise või maksemaksu sisestamise ajal.

Faili loomiseks järgige neid samme.

1. Minge **maksudeklaratsioonide** \> **kinnipeetava maksu** \> **·** \> **PPH impordifaili e-pot 23 ja 26.**
2. Valige aruande jaoks kuupäev Alates ja Kuni ning seejärel valige tasakaalustusperiood.
3. Sisestage kande kuupäev ja seejärel valige **OK**.
4. Keele valimine. Kõik aruanded tõlgitakse USA inglise (**en-us) ja** Indoneesia (**ID**).
5. Valige ettevõtte tüüp ning seejärel sisestage tšeki- ja dokumendinumbrid. 
6. Kontrollige, kas juhataja on aruande allkirjastanud. See teave esitatakse failis. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
