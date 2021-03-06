---
title: Elektroonilise arvelduse ülevaade
description: See teema pakub teavet Elektroonilise arvelduse kohta Microsoft Dynamics 365 Finance -is and Dynamics 365 Supply Chain Management- is.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: a6a8ea3fcad980dc02f489e07a7b21fe1c1b5a5a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839976"
---
# <a name="electronic-invoicing-overview"></a>Elektroonilise arvelduse ülevaade

[!include [banner](../includes/banner.md)]

Elektrooniline arveldus Microsoft Dynamics 365 Finance ja Dynamics 365 Supply Chain Management -i jaoks on hüperskaleeritav mitme rentnikuga teenus, mis võimaldab konfigureerida elektrooniliste arvedokumentide töötlemist ja dokumendivahetust. Töötlemis- ja integratsioonireeglid on täielikult konfigureeritavad ning loogikat käitatakse väljaspool rakendusi Finance ja Supply Chain Management. Teenus on mõeldud peamiselt e-arvete töötlemiseks ettevõtete ja valitsuse vahelistes stsenaariumides, kuid seda saab kohandada ka muuks otstarbeks.

Elektrooniline arveldus aitab teil saavutada järgmisi eesmärke:

- Riigi-/regioonipõhiste nõuete kiire ja hõlbus kasutuselevõtt
- Elektroonilise arvelduse lahenduse standardiseeritud juurutamine
- Dokumendiajaloo täiustatud jälgitavus
- Lühem juurutustsükkel
- Väiksem omanduse kogukulu (TCO)
- Kergesti kohandatavad konfiguratsioonid, mille jaoks pole vaja koodi muuta
- Lihtsustatud konfiguratsioonipakett
- Sisseehitatud eksportimine, importimine ja integratsioon ning e-arve dokumentide töötlemise lihtne laiendatavus
- Ekspordi-, impordi- ja integratsioonikonfiguratsioonide lihtne taaskasutamine ettevõtete vahel

Elektroonilise arvelduse kasutamiseks peate selle installima oma projektis Microsoft Dynamics Lifecycle Services (LCS). Järgmiseks järgige seadistusjuhiseid, et lülitada sisse integratsioon rakendusega Finance või Supply Chain Management. Lisateavet leiate teemast [Elektroonilise arvelduse kasutamise alustamine](e-invoicing-get-started.md).

## <a name="service-availability"></a><a name="availability"></a>Teenuse saadavus

Praegu on elektrooniline arveldus saadaval klientidele eelvaateprogrammi kaudu ja järgmises faasis muutub teenus üldiselt kättesaadavaks. Kuna riigi-/regioonipõhiste nõuetega seotud funktsioonid võivad olla väljalaske eri faasides piiratud, peaksite alati lugema kõige ajakohasemat dokumentatsiooni, milles käsitletakse toetatud riigi-/regioonipõhiste lahenduste ulatust.

Elektrooniline arveldus juurutatakse järgmistes Azure'i geograafilistes piirkondades:

- Ameerika Ühendriigid
- Euroopa

> [!NOTE]
> Elektrooniline arveldus ei toeta kohapealseid juurutusi.

## <a name="extended-configurability"></a>Laiendatud konfigureeritavus

Elektroonilist arveldust saab kasutada olukordades, kus te peate looma elektroonilise dokumendi ja saatma selle määratud pooltele. See on spetsiaalselt loodud töötlemistegevuste konfigureeritava voo käivitamiseks saadud andmete põhjal. Rakendustes Finance ja Supply Chain Management saadaval konfigureerimissuvandid piirduvad dokumendi teisendamisega. See teenus laiendab neid suvandeid, lisades selles saadaolevad konfigureeritavad integratsioonid. Lisaks kasutavad kõik varem saadaval olnud elektroonilise arve funktsioonid (näiteks Brasiilia Nota fiscal eletrônica (NF-e), Mehhiko Comprobante Fiscal Digital por Internet (CFDI) või muu Lääne-Euroopa Universal Business Language (UBL) / Euroopa-ülene Public Procurement OnLine (PEPPOL)) konfiguratsioone eksportimiseks ja importimiseks ning integratsiooni lubamiseks väliste veebiteenustega.

## <a name="feature-highlights"></a>Esiletõstetud funktsioonid

- Valmiskujul integratsioon rakendustega Finance ja Supply Chain Management
- Järjekindel kasutajakogemus e-arvete protsessi konfigureerimisel ja jälgimisel kõigi riikide või regioonide puhul
- Kiirema, lihtsama ja odavama Elektroonilise arvelduse lahenduse kohandamine uutele riikidele või piirkondadele
- Teenuse konfigureerimine teenuse Regulatory Configuration Service (RCS) kaudu ja globaliseerimisfunktsiooni seadistamine
- Äriandmete teisendamine mitmesse e-arve vormingusse (XML, JavaScript Object Notation \[JSON\], TXT ja komaeraldusega väärtused \[CSV\]) RCS-is määratletud konfiguratsioonide abil.

    - Elektroonilise aruandluse vormingud, mis on saadaval riikides või regioonides, kus e-arve teisendamise konfigureerimine pole saadaval

- E-arvete konfigureeritav edastamine välistele veebiteenustele, sh sertide haldamine digitaalallkirjade kaudu.

    - Sisseehitatud, kergesti laiendatav ja konfigureeritav integratsioon täiendava sisuga mitme riigi jaoks

    > [!NOTE]
    > Praegu toetatakse piiratud arvu otseedastusi. Lisateavet leiate selle teema varasemast jaotisest [Teenuse saadavus](#availability). Toetust laiendatakse tulevikus.

- Veebiteenuste vastuste haldamine, sh konfigureeritav eranditeadete haldamine
- Elektrooniliste allkirjade tugi (nt allkirjastamise algoritmi XMLDSig abil)
- E-arve teadete pakktöötlus

## <a name="architecture-and-data-flow"></a>Arhitektuur ja andmevoog

Kui elektrooniline arveldus on LCS-ist installitud ja vajalik seadistus on lõpetatud kõikides vajalikes rakendustes, luuakse turvaline ühendus. Teenus asub praegu Ameerika Ühendriikides ja Euroopas asuvates andmekeskustes. Seetõttu võib teenuse asukoht erineda seotud rakenduse Finance või Supply Chain Management eksemplari asukohast. Pärast elektroonilise arvelduse lisandmooduli seadistamise lõpetamist ja integratsiooni sisselülitamist saadetakse elektroonilise arve saatmise korral kindla dokumendiga seotud põhi- ja kandeandmed elektroonilise arvelduse lisandmoodulisse.

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

Järgmine illustratsioon näitab, kuidas andmed elektroonilisse arveldusse sisenevad ja sealt väljuvad.

![Elektroonilise arvelduse lisandmooduli andmevoog](media/e-invoicing-service-data-flow-diagram-overview.png)

## <a name="privacy-notice"></a>Privaatsusavaldus
Elektroonilise arvelduse lubamise ja kasutamise korral on võimalik, et saata tuleb piiratud andmeid, sealhulgas organisatsiooni maksukohustuslasena registreerimise ID. See edastatakse maksuameti volitatud kolmandatest isikutest asutustele, mille eesmärk on saata elektroonilisi arveid eelmääratletud vormingutes, mis on vajalikud integratsiooniks valitsuse veebiteenustega. Nendest välissüsteemidest sellesse Dynamics 365 võrguteenusesse imporditud andmete puhul kehtib meie [privaatsusavaldus](https://go.microsoft.com/fwlink/?LinkId=512132). Lisateavet leiate riigipõhise funktsiooni dokumentatsioonis asuvatest privaatsusavalduse jaotistest.

## <a name="additional-resources"></a>Lisaressursid
- [Teenuse haldus](e-invoicing-service-administration.md)
- [Elektrooniliste arvete konfigureerimine RCS-is](e-invoicing-configuration-rcs.md)
- [Elektroonilise arvete väljastamine teenustes Finance ja Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
