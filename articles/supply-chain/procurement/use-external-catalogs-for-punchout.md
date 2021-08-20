---
title: Väliskataloogide kasutamine e-hanke väljaregistreerimiseks
description: See teema selgitab, kuidas kasutada väliseid katalooge ostutaotluste koostamiseks ja esitamiseks.
author: kamaybac
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchVendorPortalRequests, CatExternalCatalogBasketWizard, CatExternalCatalogPunchoutDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e360204bdb71dca35337e1b95bdf1837a16a25caa00e979f70876dd5ffd9139
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774050"
---
# <a name="use-external-catalogs-for-punchout-e-procurement"></a>Väliskataloogide kasutamine e-hanke väljaregistreerimiseks

[!include [banner](../includes/banner.md)]

Kasutades väliseid katalooge e-hanke väljaregistreerimiseks pole teil vaja hoida oma koondandmetes teavet oma hankija toodete kohta. Selle asemel teisendatakse ostukorv hankija veebisaidil ostutaotluse ridadeks, millel on õiged tooteandmed. 

Peaksite vältima oma hankija toodete kirjelduste ja hindade hoidmist oma toote koondandmetes. Selle asemel kasutage e-hanke väljaregistreerimiseks väliseid katalooge. Siis, kui töötajad koostavad ostutaotlusi, saavad nad registreerida end välja hankija välisele kataloogisaidile (teisisõnu lahkuvad nad teie süsteemist ja lähevad hankija saidile). Siis saab tooted, mis lisatakse hankija veebisaidil ostukorvi, teisendada ostutaotluse ridadeks. Seetõttu saate õige tooteteabe: toote ID, nimi, hind jne.

Väliste kataloogide kasutamiseks peab töötaja looma ostutaotluse lehel **Minu ostutaotlused**.

Töötajat, kes ostutaotluse loob, nimetatakse ostutaotluse koostajaks. Koostajana võite teha järgmised toimingud.

Kasutage reatoimingut **Välised kataloogid**, et avada leht, mis sisaldab kõiki konkreetse nõude esitaja, ostva juriidilise isiku ja vastuvõtva tootmisüksuse puhul saadaolevaid väliseid katalooge.

Olenevalt teie õigustest muutke nõude esitajat, ostvat juriidilist isikut ja vastuvõtvat tootmisüksust. Nende väärtuste muutmisel võib muutuda nõude esitajale kättesaadavate väliste kataloogide loend. Saadaolevad välised kataloogid olenevad ostva juriidilise isiku või vastuvõtva tootmisüksuse kehtivatest aktiivsetest ostupoliitikatest. Need poliitikad võivad lubada või keelata juurdepääsu konkreetsetele hankekategooriatele. Seetõttu võib see mõjutada nende hankekategooriatega vastendatud väliste kataloogide loendit.

Poliitikate seadistamise kohta leiate lisateavet jaotisest [Ostupoliitikate ülevaade](../procurement/purchase-policies.md).

- Konkreetsete hankekategooriate puhul väliste kataloogide leidmiseks sisestage tekst kataloogi otsinguväljale.
- Toodete lisamiseks hankija välisest kataloogist hankija veebisaidil klõpsake välist kataloogi. Seejärel lisage ostukorvi tooteid ja makske. Ostukorvi read edastatakse rakendusse Microsoft Dynamics 365.

Kui hankekategooriate puhul on mitu valikut, siis valige enne ostutaotlusele ridade lisamist õige hankekategooria.
Pärast ostutaotlusele ridade lisamist võite lisada veel ridu, väliseid katalooge kasutamata. Teise võimalusena võite jätkata väliste kataloogide kasutamist ridade lisamiseks.

Kui ostutaotlus on valmis, kasutage toimingut **Töövoog** > **Edasta**, et edastada see kinnitamiseks.

### <a name="additional-resources"></a>Lisaressursid

- [Väliskataloogi häälestamine e-hanke väljaregistreerimiseks](set-up-external-catalog-for-punchout.md)
- [cXML-i täiustuste ostmine](purchasing-cxml-enhancements.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]