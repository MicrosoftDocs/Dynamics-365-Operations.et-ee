---
title: Kassa välisseadmete ja teenuste seisundikontroll
description: Selles teemas antakse ülevaate kassa seisundikontrolli toimingust.
author: rubendel
manager: AnnBe
ms.date: 03/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 86f0964b6d929d0434a8bf04aaefc173bee21c6f
ms.sourcegitcommit: d77e902b1ab436e5ff3e78c496f5a70ef38e737c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/15/2020
ms.locfileid: "4411798"
---
# <a name="health-check-for-pos-peripherals-and-services"></a>Kassa välisseadmete ja teenuste seisundikontroll

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse kassa seisundikontrolli toimingut.

## <a name="overview"></a>Ülevaade

Kauplused võivad olla keerukad keskkonnad, kus on kasutusel mitmeid rakendusi ja seadmeid. Toimingute lisandumisel võib olla raske tagada, et need töötaksid alati vaevatult, näiteks välisseadmetest sõltumise tõttu, mis võivad päeva jooksul katki minna või juhuslikult vooluvõrgust välja tulla. Seadmete ja teenustega seotud probleemide tõrkeotsing võib olla kulukas suurematele kaupmeestele ja samamoodi ahastav väiksematele ettevõtetele.

Microsoft Dynamics 365 Commerce'i versioon 10.0.10 ja hilisemad versioonid sisaldavad seisundikontrolli toimingut, mis aitavad ennetada sellega seonduvat kulu ja muret. See toiming võimaldab seadmete testimise viisi otse kassast tavapäraste toimingute kõrvalt. See võimaldab jaemüüjatel probleeme tuvastada enne nende ilmnemist.

## <a name="key-terms"></a>Põhimõisted

| Mõiste | Kirjeldus |
|---|---|
| Välisseade | Mis tahes seade, mida kassarakendus kasutab kannete ja muude kaupluse toimingute hõlbustamiseks. Nendeks on näiteks sularahasahtlid, vöötkoodiskannerid ja makseterminalid. |
| Teenus | Selles teemas nimetatakse teenuseks lisarakendust, millest kassarakendus sõltub kannete ja igapäevaste toimingute sooritamiseks. Näidete hulka kuuluvad rakendused, mis aitavad maksude või tarne arvutamisel. |

## <a name="health-check-operation"></a>Seisundikontrolli toiming

Seisundikontroll on toiming 717 Commerce'i peakontori lehel **Kassatoimingud**. Seda saab kasutada siis, kui kassa on kassavälises režiimis. Kuid riistvarajaam peab olema aktiivne.

Vaikimisi testib seisundikontroll ainult neid seadmeid, mis on seadistatud riistvarajaama riistvara profiilis, mis on praegu registris aktiivne. Kui register kasutab päeva jooksul mitut riistvarajaama, peab neile kõigile seisundikontrolli tegemiseks ühendada ükshaaval samasse riistvarajaama. Kaupluse tasemel seisundikontrolli pole. Siiski on võimalik sellist tüüpi kontrolli teha Commerce'i serveri laiendatavuse kaudu.

### <a name="out-of-box-health-checks"></a>Seisundikontrolli valmislahendused

| Tüüp | Ühendus | Details |
|---|---|---|
| Printer | OPOS | See kontroll testib põhiobjekti, linkides ja manustades kassafunktsioonidele (OPOS). Järgmisena on toodud mõned näited.<ul><li>Avamiseks **Ava** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Sulgemiseks: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Sule**</li></ul> |
| Rea kuva | OPOS | See kontroll testib peamisi OPOS-i funktsioone. Järgmisena on toodud mõned näited.<ul><li>Avamiseks **Ava** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Sulgemiseks: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Sule**</li></ul> |
| Topeltkuva | &Aknad... | See kontroll tagab, et operatsioonisüsteem tuvastab teise Windowsi kuvari. | 
| Magnetribalugeja | OPOS | See kontroll testib peamisi OPOS-i funktsioone. Järgmisena on toodud mõned näited.<ul><li>Avamiseks **Ava** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Sulgemiseks: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Sule**</li></ul> |
| Koostaja | OPOS | See kontroll testib peamisi OPOS-i funktsioone. Järgmisena on toodud mõned näited.<ul><li>Avamiseks **Ava** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Sulgemiseks: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Sule**</li></ul> | 
| Skanner | OPOS | See kontroll testib peamisi OPOS-i funktsioone. Järgmisena on toodud mõned näited.<ul><li>Avamiseks **Ava** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Sulgemiseks: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Sule**</li></ul> | 
| Sobita | OPOS | See kontroll testib peamisi OPOS-i funktsioone. Järgmisena on toodud mõned näited.<ul><li>Avamiseks **Ava** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Sulgemiseks: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Sule**</li></ul> |
| PIN-klahvistik | OPOS | See kontroll testib peamisi OPOS-i funktsioone. Järgmisena on toodud mõned näited.<ul><li>Avamiseks **Ava** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Sulgemiseks: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Sule**</li></ul> |
| Makseterminal | SDK-maksed | See kontroll testib peamisi SDK-maksete pakutavaid makseterminali funktsioone. <ul><li>Lukusta</li><li>BeginTransaction</li><li>EndTransaction</li><li>ReleaseDevice</li><li>Sulgemine</li></ul> |

### <a name="using-the-health-check-operation-in-the-pos"></a>Seisundikontrolli toimingu kasutamine kassas

Kui kassas käivitatakse seisundikontrolli toiming, kuvatakse parempoolsel paanil konfigureeritud seadmete loend ja iga seadme olek. Ühele seadmele seisundikontrolli tegemiseks valige seade ja seejärel valige **Test valituid**. Kõiglei seadmetele seisundikontrolli tegemiseks valige **Testi kõiki**. Funktsioon **Testi kõiki** testib kõiki seadmeid ükshaaval ja uuendab iga seadme olekut veerus **Olek**.

Veerg **Viimane kontroll** kuvab viimase seisundikontrolli tegemise aega iga seadme kohta.

Kui seade läbib seisundikontrolli (st tõrkeid ei esine), kuvatakse seadme olekuks **OK**. Kui seisundikontroll nurjub, kuvatakse olekuks tõrke ilmnemine. Sel juhul kuvatakse parempoolsel paanil tõrkega seotud üksikasjad või juhendatakse kasutajat pöörduma süsteemiadministraatori poole.

Osade seadmete puhul (nt OPOS-klahvilukk) ei ole seisundikontrolli valmislahendusi saadaval. Kui mõne kasutatava seadme puhul ei tuvastata seisundikontrolli testi, siis kuvatakse olek **Ei ole toetatud**.

### <a name="extending-health-checks"></a>Seisundikontrolli laiendamine

Seisundikontrolli valmislahendused on konfigureeritud pakkuma mõningaid kasutajasõbralikke teateid tüüpilistele tõrgetele. Siiski ei ole kõik stsenaariumid kaetud. Laiendatavuse kaudu saavad kaupmehed vastendada kasutajasõbralikke veateateid, mis on kohandatud nende keskkonnale.

Kohandatud seisundikontrolle saab luua ka nende seadmete testimiseks, mille jaoks ei ole valmislahendusi saadaval või mis tahes teenuste testimiseks, millest kassa sõltub.

## <a name="related-articles"></a>Seotud artiklid

[Kaasaegse kassa (MPOS) päästikud ja printimine](dev-itpro/pos-trigger-printing.md)
