---
title: Registreerimismärgi sildi printimise lubamine
description: Selles teemas näidatakse, kuidas lubada SSCC (serial shipping conteiner code) sildi automaatne printimine pärast seda, kui viimane üksus on müügivalimise tööprotsessis laost valitud.
author: perlynne
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd79abfc1029c4e0ef41d0e9b0f33ff524f50e36b70cf4fa3ed50dcdc4cb7f03
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751667"
---
# <a name="enable-license-plate-label-printing"></a>Registreerimismärgi sildi printimise lubamine

[!include [banner](../../includes/banner.md)]

Selles teemas näidatakse, kuidas lubada SSCC (serial shipping conteiner code) sildi automaatne printimine pärast seda, kui viimane üksus on müügivalimise tööprotsessis laost valitud. Võite seda protseduuri käitada demoettevõtte USMF-i andmetega. Kui käitate seda omaenda andmeid kasutades, peaksite määrama litsentsiplaatide numbriseeria. Enne ülesande juurde asumist peaksite määrama sildiprinteri. Avage Organisatsiooni haldus > Seadistus > Võrguprinterid. Klõpsake Toimingupaanil Suvandid, seejärel klõpsake nuppu Laadi dokumendi marsruudivaliku agendi installer alla. Käitage installer ja veenduge enne protseduuriga jätkamist, et töötav võrguprinter on seatud olekusse Aktiivne.


## <a name="set-up-the-gs1-company-prefix"></a>GS1 ettevõtteprefiksi seadistus
1. Minge **Navigeerimispaan > Moodulid > Laohaldus > Seadistus > Laohalduse parameetrid**.
2. Sisestage väljale **GS1 ettevõtte eesliide** oma GS1 ettevõtte numbri 7 numbrit.
3. Valige käsk **Salvesta**.
4. Sulgege leht.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>SSCC-identifitseerimisnumbri numbriseeria seadistus
1. Avage **Navigeerimispaan > Moodulid > Organisatsiooni haldus > Numbriseeriad > Numbriseeriad**.
2. Väljal **Ala** valige sobiv valik.
3. Väljal **Viide** valige sobiv valik.
4. Sisestage väärtus väljale **Ettevõte**.
5. Laiendage jaotist **Segmendid**.
6. Valige suvand **Redigeeri**.
7. Tabelis **Segmendid** valige esimene rida
8. Valige **Eemalda**.
9. Valige **Eemalda**.
10. Valige käsk **Salvesta**.
11. Sulgege leht.

## <a name="create-the-document-route-layout"></a>Dokumendi marsruudivaliku paigutuse loomine
1. Avage **Navigeerimispaan > Moodulid > Laohaldus > Seadistus > Dokumentide suunamine > Dokumentide suunamise paigutused**. Saate lubada SSCC-paigutuse.  
2. Valige suvand **Uus**.
3. Sisestage väärtus väljale **Paigutuse ID**.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Valige **Lisa teksti lõppu**.
6. Valige käsk **Salvesta**.
7. Sulgege leht.

## <a name="set-up-the-document-routing"></a>Dokumendi marsruudivaliku häälestamine
1. Avage **Navigeerimispaan > Moodulid > Laohaldus > Seadistus > Dokumentide suunamine > Dokumentide suunamine**.
2. Väljal **Töökäsu tüüp** valige sobiv valik.
3. Valige suvand **Uus**.
4. Sisestage väärtus väljale **Ladu**.
5. Sisestage väärtus väljale **Nimi**.
6. Valige suvand **Uus**.
7. Väljale **Paigutuse ID** sisestage või valige väärtus.
8. Sisestage väljale **Nimi** printeri nimi, mida soovite kasutada.
9. Valige käsk **Salvesta**.
10. Sulgege leht.

## <a name="create-mobile-device-menu"></a>Mobiilse seadme menüü loomine
1. Avage **Navigeerimispaan avage Moodulid > Laohaldus > Seadistus > Mobiiliseade > Mobiiliseadme menüü-üksused**.
2. Valige suvand **Uus**.
3. Sisestage väärtus väljale **Menüü-üksuse nimi**.
4. Sisestage väärtus väljale **Pealkiri**.
5. Väljal **Režiim** valige sobiv valik.
6. Valige väärtus **Jah** väljal **Kasuta olemasolevat tööd**.
7. Valige väärtus **Jah** väljal **Loo litsentsi plaat**.
8. Laiendage jaotist **Tööklassid**.
9. Valige suvand **Uus**.
10. Väljale **Tööklassi ID** sisestage väärtus.
11. Valige käsk **Salvesta**.
12. Sulgege leht.
13. Avage **Navigeerimispaan avage Moodulid > Laohaldus > Seadistus > Mobiiliseade > Mobiiliseadme menüü**.
14. Valige puus menüüelement, mille olete varem loonud.
15. Valige suvand **Redigeeri**.
16. Menüüelemendi menüüsse lisamiseks valige nool.
17. Valige käsk **Salvesta**.
18. Sulgege leht.

## <a name="update-a-work-template"></a>Töömalli värskendus
1. Minge **Navigeerimispaan > Moodulid > Laohaldus > Seadistus > Töö > Töö mallid**.
2. Valige suvand **Redigeeri**.
3. Valige suvand **Uus**.
4. Väljal **Töö tüüp** valige **Prindi**.
5. Väljal **Tööklassi ID** sisestage või valige väärtus.
6. Valige **Nihuta üles**.
7. Valige käsk **Salvesta**.
8. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]