---
title: Kasutushalduse armatuurlaud
description: See artikkel selgitab, kuidas kasutada kasutushalduse armatuurlauda elektroonilise arveldamise teenuse kasutamise jälgimiseks ja ühildumiseks jäämiseks.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 74f3d88faf192474c177da971a9f7bb0e58e1279
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272205"
---
# <a name="usage-management-dashboard"></a>Kasutushalduse armatuurlaud

[!include [banner](../includes/banner.md)]

**Kasutushalduse** armatuurlaud aitab jälgida elektroonilise arveldamise teenuse kasutamist ning seega aitab teie organisatsioonil püsida ühilduvigakuiste kasutustingimustega. Vastavuse määratleb esitamise mahu arvutamine ja võrreldakse seda esitamise soetatud mahuga, et tuvastada mis tahes kõrvalekaldeid soetatud mahu ja kasutatud mahu vahel.

Armatuurlaud sisaldab järgmisi näidikuid:

- Üks kulumõõdik, mida saate kasutada tarbimise jälgimiseks litsentsimise vastavuse eesmärkidel:

    - Kasutamine kuus (eksport)

- Kolm töönäitajat, mida saate kasutada elektroonilise arveldamise teenuse kasutamise jälgimiseks halduseesmärkidel:

    - Kasutus funktsiooni järgi
    - Kasutus keskkonna järgi
    - Kasutus kuus (import)

## <a name="measurement-scope"></a>Mõõtmise ulatus

- Mõõtmise ühik: 

    **Kasutushalduse** armatuurlaud loendab äridokumentide ja imporditud elektrooniliste arvete esitamist.

- Organisatsioon: 

    Loendamine summeeritakse teie organisatsiooni rentniku ID järgi, Microsoft Dynamics olenemata 365 Dynamics 365 Supply Chain Management Finantside eksemplaride arvust või juriidiliste isikute arvust, kus elektroonilise arveldamise teenus on lubatud.


## <a name="indicator-usage-per-month-export"></a>Näitaja: kasutus kuus (eksport)

See indikaator annab üksikasju elektrooniliste arvete kohta, mida teie organisatsioon määratletud perioodi jooksul väljastab.

### <a name="scope"></a>Ulatus
- Äridokumentide arv, mis on esitatud Finance and Supply Chain Management elektroonilise arveldamise teenusele, sõltumata ridade arvust, mida need äridokumendid sisaldavad.
- Edastatud äridokumentide arv, mida elektroonilise arveldamise teenus edukalt töötleb. Kui funktsiooniseadistuses määratletud tegevuste voog on lõpule viidud, loetakse dokument edukalt töödelduks.

> [!NOTE]
> Kui elektrooniline arve esitatakse välisele veebiteenusele, ei sõltu inventuur veebiteenuse töötlemise tulemustest (aktsepteeritud, tagasi lükatud või skeemi kinnitamistõrge). Kui veebiteenus sai ja vastas elektroonilise arveldamise teenuse taotlusele, loetakse esitamine kehtivaks inventuuriks.

- **Erand:** äridokumente ei arvestata, kui need on uuesti Finance and Supply Chain Management elektroonilise arveldamise teenusesse esitatud, nt stsenaariumides, kus elektroonilise arve oleku muutmiseks on vajalik sama äridokumendi uuesti esitada. Näiteks Brasiilia elektroonilise arve väljastamist (fiskaaldokument) loetakse kehtivaks, kuid selle tühistamistaotlust ei arvestata.


### <a name="calculation"></a>Kalkulatsioon

Saldo arvutatakse järgmiselt:

Saldo = Vaba + Ostetud – Kasutatud

Kus

- Vaba:
  
    Äridokumentide vaba maht, mille klient saab kuu kohta esitada. See sisaldab 100 äridokumendi paketti, mida saab elektroonilise arvelduse teenusele esitada. Vaba maht pole kumulatiivne ja ülejäänud saldot ei pöörata üle järgmisele perioodile.
  
- Ostetud:
  
    See sisaldab 1000 äridokumendi paketti, mida saab elektroonilise arvelduse teenusele esitada. See pakett tuleb soetuda teie organisatsioonile kord kuus. Vaba maht pole kumulatiivne ja ülejäänud saldot ei pöörata üle järgmisele perioodile.
  
- Kasutatud: 

    Äridokumendiedastuste arv elektroonilise arvelduse teenusele vastavalt määratletud kriteeriumidele.
   
> [!IMPORTANT]
> Kui teie organisatsioon plaanib ületada igakuist mahtu 100 vabaedastuse korral, ostke tippmaht, et tagada teie vastavus Microsofti elektroonilise arveldamise teenuse litsentsipoliitikaga.
>
> Praegu tuleb ostetud maht vastavalt soetuskuupäevale sisestada käsitsi mitme 1000 esitamisega pakendina.

## <a name="indicator-usage-by-feature"></a>Indikaator: kasutus funktsiooni järgi

See näidik näitab elektroonilise arveldamise funktsioonide kasutamist elektrooniliste arvete väljastamiseks määratletud perioodil.

- Kalkulatsioon:
  
    Kasutatud = loendamine, mitu korda iga elektroonilise arvelduse funktsiooni kasutati äridokumentide edastamisel elektroonilise arveldamise teenusele.

## <a name="indicator-usage-by-environment"></a>Indikaator: kasutus keskkonna järgi

See näidik näitab elektroonilise arveldamise teenuse keskkondade kasutamist määratletud perioodi jooksul.

- Kalkulatsioon:
    
    Kasutatud = loendamine, mitu korda iga elektroonilise arvelduse teenuse keskkonda kasutati äridokumentide edastamisel elektroonilise arveldamise teenusele.

## <a name="indicator-usage-per-month-import"></a>Näitaja: kasutus kuus (import)

See näidik näitab elektrooniliste arvete mahtu elektroonilise arveldamist Finance and Supply Chain Management kaudu määratletud perioodil.

- Ulatus:

    Finance and Supply Chain Management imporditud elektroonilised arved, sõltumata ridade arvust, mida need elektroonilised arved sisaldavad.

- Kalkulatsioon:

    Saadud = Finance and Supply Chain Management`ìst imporditud elektrooniliste arvete arv.

## <a name="functions"></a>Funktsioonid
### <a name="purchase"></a>Ost

Valige **Kasutus kuus (eksport)** vahekaardil **Ost**, et soetatud edastuste summa käsitsi registreerida.

Antud kuupäeval tehke valik **Uus** ja sisestage sel kuupäeval soetatud **pakendite arv**.

**Kogus** arvutatakse järgmiselt:

Kogus = Pakendid * 1000

Arvutatud **kogus** peegeldab välja **Ostetud** indikaatorilt **Kasutus kuus (eksport)**.

### <a name="update"></a>Värskendus

Tegevuspaanil valige **uuendamine**, et värskendada arvutust ja värskendada leheküljel ja diagrammil kuvatavaid andmeid.

### <a name="reset-history-data"></a>Lähtesta ajaloo andmed

Tegevuspaanil valige suvand **Lähtesta ajaloo andmed**, et värskendada andmebaasi näidikute arvutamise asukohast.




> [!NOTE]
> **Kasutushalduse** armatuurlaud ei näita rahasummasid. Selle asemel näitab see ainult loendatud ja imporditud dokumentide mahtu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
