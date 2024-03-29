---
title: Põhivara kulumiarvestusreeglid
description: Selles artiklis kirjeldatakse põhivarade kulumiarvestusreeglid.
author: moaamer
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d791461a344611437e77514e47dd5dd9b7ddb10
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858387"
---
# <a name="fixed-asset-depreciation-conventions"></a>Põhivara kulumiarvestusreeglid

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse põhivarade kulumiarvestusreeglid. Kulumiarvestusreegleid kasutatakse määramaks, millal ja kuidas kulumit arvestatakse nii aastal, mil põhivara soetatakse, kui ka aastal, mil see likvideeritakse.

Kulumiarvestusreegleid saab määrata põhivaragrupi raamatu häälestuseks. Kulumiarvestusreegli vaatamiseks või määramiseks valige põhivarade seadistusalal **põhivara** rühmad. Valige nupp **Raamatud**. Selles näites kasutatakse määratud kulumiarvestusreegleid põhivararaamatute loomisel vaikeväärtustena. Kulumiarvestusreegleid saab määrata ka üksikule põhivararaamatule. Selleks valige põhivara seadistusalal nupp **Raamatud** ja seejärel nupp **Põhivarade rühmad**.

| Kulumiarvestusreegel   | Kirjeldus |
|---------------------------|-------------|
| Puudub                      | Varad hakkavad vähenema <strong>teenusesse saatmise</strong> kuupäeval. |
| Poolaasta                 | Atribuudi vähendamisel lähevad mahaarvestamisele nii esimese kui ka viimase aasta poolaastakulumid. Taasteperioodi jooksul läheb mahaarvestamisele iga teise aasta täisaastakulum. |
| Terve kuu                | Ükskõik millal kuu alguses oleva <strong>teenusesse saatmise</strong> kuupäevaga olevate varade mahaarvestamine algab selle kuu esimesel päeval. Kulumiarvestuse eesmärgil loetakse varad tühistatuks eelneva kuu viimasest päevast. Arvesse ei võeta seda päeva kuus, mil need tühistati. |
| Kvartali keskel               | Atribuudi kasutusse rakendamise aastal olevaks kulumiarvestuseks korrutage täisaasta kulum atribuudi kasutusse rakendamise perioodi kvartali protsendiga, nagu on näidatud järgmises tabelis.<table><thead><tr><th>Kvartal</th><th>Protsent</th></tr></thead><tbody><tr><td>Esimene</td><td>87,5</td></tr><tr><td>Teine</td><td>62,5</td></tr><tr><td>Kolmas</td><td>37,5</td></tr><tr><td>Neljas</td><td>12.5</td></tr></tbody></table>Poole kvartali kulumiarvestus sooritatakse kvartalis, mil vara likvideeriti (või kvartalis, mil see täielikult amortiseeriti). |
| Kuu keskel (kuu 1. päev)  | Kuu esimesel poolel (päevad 1 kuni 15) olevate <strong>teenusesse saatmise</strong> kuupäevadega varade kulumiarvestus algab <strong>teenusesse saatmise</strong> kuupäeva kuu esimesel päeval. Kuu teisel poolel (päevad 16 kuni kuu lõpp) olevate <strong>teenusesse saatmise</strong> kuupäevadega varade kulumiarvestus algab <strong>teenusesse saatmise</strong> kuupäeva järgse kuu esimesel päeval. Kuu esimesel poolel (päevad 1 kuni 15) tühistatavate varade kulumiarvestus tühistatakse eelmise kuu viimasel päeval. Kuu teisel poolel (päevad 16 kuni kuu lõpp) tühistatavate varade kulumiarvestus tühistatakse kõrvaldamise kuu viimasel päeval. |
| Kuu keskel (kuu 15. päev) | Vara kasutuselevõtmise aasta kohta kulumi mahaarvamiseks korrutage täisaasta kulum murruga. Selle murru lugeja (Ülemine number) on täis, pluss 1/2 või (0,5) paikneb aasta kuude arv. Nimetaja (alumine number) on 12. Kui likvideerite vara enne taasteperioodi lõppu, kasutage sama meetodit likvideerimise aastal kulumi mahaarvestamiseks. |
| Poolaasta (aasta algus) | Aasta esimesel poolel olevate <strong>teenusesse saatmise</strong> kuupäevadega varade kulumiarvestus algab aasta (täisaasta) esimesel päeval. Aasta teisel poolel olevate <strong>teenusesse saatmise</strong> kuupäevadega varade kulumiarvestus algab aasta keskel. |
| Poolaasta (järgmine aasta)     | Aasta esimesel poolel olevate <strong>teenusesse saatmise</strong> kuupäevadega varade kulumiarvestus algab aasta (täisaasta) esimesel päeval. Aasta teisel poolel olevate <strong>teenusesse saatmise</strong> kuupäevadega varade kulumiarvestus algab järgmise aasta esimesel päeval. Aasta esimesel poolel tühistatavate varade kulumiarvestus tühistatakse eelmise aasta viimasel päeval. Käesoleval aastal postitatud kulumiarvestus peab olema tühistatud või korrigeeritud. Aasta teisel poolel tühistatavate varade kulumiarvestus tühistatakse aasta viimasel päeval. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
