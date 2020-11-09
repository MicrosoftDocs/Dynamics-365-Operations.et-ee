---
title: Elektroonilise arvelduse lisandmooduli ülevaade
description: See teema sisaldab teavet selle kohta, kuidas seadistada rakendustes Microsoft Dynamics 365 Finance ja Dynamics 365 Supply Chain Management elektroonilise arvelduse lisandmoodulit.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ffd48e173b66cc6d2571e666d5452a5eff05176c
ms.sourcegitcommit: d6250ee5ced43be39e789324a895fd1c07178935
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/19/2020
ms.locfileid: "4039742"
---
# <a name="electronic-invoicing-add-on-overview"></a>Elektroonilise arvelduse lisandmooduli ülevaade

[!include [banner](../includes/banner.md)]

Elektroonilise arvelduse lisandmoodul rakenduste Microsoft Dynamics 365 Finance ja Dynamics 365 Supply Chain Management jaoks on hüperskaleeritav mitme rentnikuga teenus, mis võimaldab konfigureerida elektrooniliste arvedokumentide töötlemist ja dokumendivahetust. Töötlemis- ja integratsioonireeglid on täielikult konfigureeritavad ning loogikat käitatakse väljaspool rakendusi Finance ja Supply Chain Management. Teenus on mõeldud peamiselt e-arvete töötlemiseks ettevõtete ja valitsuse vahelistes stsenaariumides, kuid seda saab kohandada ka muuks otstarbeks.

Elektroonilise arvelduse lisandmoodul aitab teil saavutada järgmisi eesmärke.

- Riigi-/regioonipõhiste nõuete kiire ja hõlbus kasutuselevõtt
- Elektroonilise arvelduse lisandmooduli lahenduse standardiseeritud juurutamine
- Dokumendiajaloo täiustatud jälgitavus
- Lühem juurutustsükkel
- Väiksem omanduse kogukulu (TCO)
- Kergesti kohandatavad konfiguratsioonid, mille jaoks pole vaja koodi muuta
- Lihtsustatud konfiguratsioonipakett
- Sisseehitatud eksportimine, importimine ja integratsioon ning e-arve dokumentide töötlemise lihtne laiendatavus
- Ekspordi-, impordi- ja integratsioonikonfiguratsioonide lihtne taaskasutamine ettevõtete vahel

Elektroonilise arvelduse lisandmooduli kasutamiseks peate selle installima oma projektis rakenduses Microsoft Dynamics Lifecycle Services (LCS). Järgmiseks järgige seadistusjuhiseid, et lülitada sisse integratsioon rakendusega Finance või Supply Chain Management. Lisateavet leiate teemast [Elektroonilise arvelduse lisandmooduli kasutamise alustamine](e-invoicing-get-started.md).

## <a name="availability"></a>Kättesaadavus

Esialgu on elektroonilise arvelduse lisandmoodul saadaval valitud klientidele eelversiooniprogrammi kaudu. Hiljem avatakse eelversioon rohkematele klientidele. Lõpuks muutub teenus üldiselt kättesaadavaks. Kuna riigi-/regioonipõhiste nõuetega seotud funktsioonid võivad olla väljalaske eri faasides piiratud, peaksite alati lugema kõige ajakohasemat dokumentatsiooni, milles käsitletakse toetatud riigi-/regioonipõhiste lahenduste ulatust.

Elektroonilise arvelduse lisandmoodul juurutatakse järgmistes Azure'i geograafilistes piirkondades.

- Ameerika Ühendriigid
- Euroopa

> [!NOTE]
> Elektroonilise arvelduse lisandmoodul ei toeta kohapealseid juurutusi.

## <a name="extended-configurability"></a>Laiendatud konfigureeritavus

Elektroonilise arvelduse lisandmoodulit saab kasutada olukordades, kus te peate looma elektroonilise dokumendi ja saatma selle määratud pooltele. See on spetsiaalselt loodud töötlemistegevuste konfigureeritava voo käivitamiseks saadud andmete põhjal. Rakendustes Finance ja Supply Chain Management saadaval konfigureerimissuvandid piirduvad dokumendi teisendamisega. See teenus laiendab neid suvandeid, lisades selles saadaolevad konfigureeritavad integratsioonid. Lisaks kasutavad kõik varem saadaval olnud elektroonilise arve funktsioonid (näiteks Brasiilia Nota fiscal eletrônica (NF-e), Mehhiko Comprobante Fiscal Digital por Internet (CFDI) või muu Lääne-Euroopa Universal Business Language (UBL) / Euroopa-ülene Public Procurement OnLine (PEPPOL)) konfiguratsioone eksportimiseks ja importimiseks ning integratsiooni lubamiseks väliste veebiteenustega.

## <a name="feature-highlights"></a>Esiletõstetud funktsioonid

- Valmiskujul integratsioon rakendustega Finance ja Supply Chain Management
- Järjekindel kasutajakogemus e-arvete protsessi konfigureerimisel ja jälgimisel kõigi riikide või regioonide puhul
- Elektroonilise arvelduse lisandmooduli lahenduste kiirem, lihtsam ja odavam kasutuselevõtt uutes riikides või regioonides
- Teenuse konfigureerimine teenuse Regulatory Configuration Service (RCS) kaudu ja globaliseerimisfunktsiooni seadistamine
- Äriandmete teisendamine mitmesse e-arve vormingusse (XML, JavaScript Object Notation \[JSON\], TXT ja komaeraldusega väärtused \[CSV\]) RCS-is määratletud konfiguratsioonide abil.

    - Elektroonilise aruandluse vormingud, mis on saadaval riikides või regioonides, kus e-arve teisendamise konfigureerimine pole saadaval

- E-arvete konfigureeritav edastamine välistele veebiteenustele, sh sertide haldamine digitaalallkirjade kaudu.

    - Sisseehitatud, kergesti laiendatav ja konfigureeritav integratsioon täiendava sisuga mitme riigi jaoks

    > [!NOTE]
    > Praegu toetatakse piiratud arvu otseedastusi. Lisateavet leiate selle teema varasemast jaotisest [Kättesaadavus](#availability). Toetust laiendatakse tulevikus.

- Veebiteenuste vastuste haldamine, sh konfigureeritav eranditeadete haldamine
- Elektrooniliste allkirjade tugi (nt allkirjastamise algoritmi XMLDSig abil)
- E-arve teadete pakktöötlus

## <a name="architecture-and-data-flow"></a>Arhitektuur ja andmevoog

Kui elektroonilise arvelduse lisandmoodul on LCS-ist installitud ja vajalik seadistus on lõpetatud kõikides vajalikes rakendustes, luuakse turvaline ühendus. Teenus asub praegu Ameerika Ühendriikides ja Euroopas asuvates andmekeskustes. Seetõttu võib teenuse asukoht erineda seotud rakenduse Finance või Supply Chain Management eksemplari asukohast. Pärast elektroonilise arvelduse lisandmooduli seadistamise lõpetamist ja integratsiooni sisselülitamist saadetakse elektroonilise arve saatmise korral kindla dokumendiga seotud põhi- ja kandeandmed elektroonilise arvelduse lisandmoodulisse.

> [!NOTE]
> Kui teie elektrooniline arve või muu dokument sisaldab isikuandmeid, kontrollige, kas selle funktsiooni kasutamine vastab isikuandmete kaitse üldmääruse (GDPR) ja muude isikuandmete edastamisega seotud määruste nõuetele.

### <a name="high-level-description-of-the-data-flow"></a>Andmevoo kõrgetasemeline kirjeldus

1. Klient saadab teenusele kanoonilise äridokumendi.
2. Kliendist saadud kontekstiteabe põhjal valib teenus sobiva töötlusvoo.
3. Teenus käivitab töötlustegevused. Need tegevused võivad hõlmata äridokumendi teisendamist elektrooniliseks arveks, digitaalallkirja rakendamist ja dokumendi edastamist välisele veebiteenusele.
4. Kõik saadud ja töödeldud dokumendid talletatakse kliendi Azure'i bloobimälus.
5. Kõik töötlemiseks kasutatud rentnikusaladused ja serdid talletatakse kliendi Azure'i võtmehoidlas.
6. Teenus saadab nõudmisel klienti teavet saadetud äridokumendi töötlemise oleku kohta.
7. Klient võtab vastu teabe lõpetatud töötlemise kohta ja teeb kogu logiteabe kättesaadavaks. Samuti teeb see kättesaadavaks dokumendi, mis loodi või saadi voo töötlemise käigus.

Järgmisel illustratsioonil on kujutatud, kuidas andmed elektroonilise arvelduse lisandmoodulisse sisenevad ja sealt väljuvad.

![Elektroonilise arvelduse lisandmooduli andmevoog](media/e-invoicing-service-data-flow-diagram-overview.png)

## <a name="privacy-notice"></a>Privaatsusavaldus
Elektroonilise arvelduse lubamise ja kasutamise korral on võimalik, et saata tuleb piiratud andmeid, sealhulgas organisatsiooni maksukohustuslasena registreerimise ID. See edastatakse maksuameti volitatud kolmandatest isikutest asutustele, mille eesmärk on saata elektroonilisi arveid eelmääratletud vormingutes, mis on vajalikud integratsiooniks valitsuse veebiteenustega. Nendest välissüsteemidest sellesse Dynamics 365 võrguteenusesse imporditud andmete puhul kehtib meie [privaatsusavaldus](https://go.microsoft.com/fwlink/?LinkId=512132). Lisateavet leiate riigipõhise funktsiooni dokumentatsioonis asuvatest privaatsusavalduse jaotistest.

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise arvelduse lisandmooduli kasutamise alustamine](e-invoicing-get-started.md)
- [Brasiilia elektroonilise arvelduse lisandmooduli kasutamise alustamine](e-invoicing-bra-get-started.md)
- [Mehhiko elektroonilise arvelduse lisandmooduli kasutamise alustamine](e-invoicing-mex-get-started.md)
- [Itaalia elektroonilise arvelduse lisandmooduli kasutamise alustamine](e-invoicing-ita-get-started.md)
- [Elektroonilise arvelduse lisandmooduli seadistamine](e-invoicing-setup.md)
