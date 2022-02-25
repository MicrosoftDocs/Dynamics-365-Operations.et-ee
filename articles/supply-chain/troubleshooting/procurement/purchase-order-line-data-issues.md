---
title: Ostutellimuse rea andmete lahknevused
description: Näete andmete lahknevusi või andmete rikkumist ostutellimuse ridadel.
author: SmithaNataraj
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: PurchLineManualCorrection, PurchTable, PurchLine, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: ee2cb9a07c8a00a92c71e3e99d8ec20aa27fb20e
ms.sourcegitcommit: b9799a58d6ec221df86788bc37c4fbd28b435e89
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/08/2022
ms.locfileid: "8100780"
---
# <a name="purchase-order-line-data-discrepancies"></a>Ostutellimuse rea andmete lahknevused

## <a name="symptoms"></a>Sümptomid

Kui vaatate üle ostutellimuse ridu, märkate ühte või enamat probleemi:

- Ostutellimuse ridade jäägis (tarne või arve) on andmete lahknevus või riknemine.
- Ostutellimuse real või päise olekus on rikutud.
- Te ei saa ostutellimust arveldada, kuna näiteks saate ühe või mitu järgmistest tõrketeadetest:

    - "Peatatud (tõrge): kanne on juba sisestatud."
    - "Kogust ei saa arveldada, sest laokandeid olekuga Saadud pole piisavalt."
    - "Ebapiisavad laokanded olekuga Ostetud" kauba koguse %0 jaoks %1."

- Ostutellimust ei saa lõpetada ega sulgeda nt järgmiste probleemide tõttu:

    - Nupp **Vii** lõpp pole saadaval.
    - Kinnitatud ja saadud olekus ostutellimuse rea tellitud kogust ei saa tühistada.

## <a name="cause"></a>Põhjus

Need väljaminek on tavaliselt põhjustatud andmeterääkimisest või ühe või mitme ostutellimuse rea jääkkoguste lahknevusest.

## <a name="resolution"></a>Lahendus

Tavaliselt saate need probleemid lahendada, uuendades vastavate ostutellimuse ridade ostu olekut, tarnejääke ja/või arve jääke, nagu kirjeldatud järgmises protseduuris.

1. Minge hanke **perioodiliste ülesannete puhastusse \>\> . \> Parandage ostutellimuse read käsitsi**.
1. **Leidke ja valige ostutellimuse** väljal Ostutellimus, mis annab teile probleeme.
1. **Valige jaotises Ostutellimuse read** rida, kus te avastate lahknevuse.
1. **Kontrollige jaotises** Laokanded kuvatavaid andmeid. Kui te teate mis tahes vastuolusid ostutellimuse rea ja selle laokannete vahel, valige tegevuspaanil üks järgmistest käskudest, sõltuvalt sellest, kus te näete vastuolusid:

    - **Arvuta tarnejääk \> ümber – uuenda** automaatselt ostutellimuse rida ja päise olekud. See funktsioon töötab ainult ladustatud ostutellimuse ridadel (st ridadel, kus kaup on ladustatud kaup). Ladustamata kaupu ja tegeliku kaaluga kaupu praegu ei toetata.
    - **Arvuta arve jääk \> ümber – uuenda** automaatselt ostutellimuse rida ja päise olekud. See funktsioon töötab ainult ladustatud ostutellimuse ridadel (st ridadel, kus kaup on ladustatud kaup). Ladustamata kaupu ja tegeliku kaaluga kaupu praegu ei toetata.
    - **Arvuta olek \> ümber – arvutage** valitud rea olek uuesti. See arvutus põhineb olemasoleval loogikal. Seetõttu uuendatakse ostutellimuse päise olekut vastavalt vajadusele, põhinedes uue ostutellimuse rea olekul.

1. Kui näete siiski jääkkogustes vastuolusid, saate neid otse vastavalt vajadusele redigeerida järgmiste väljade abil:

    - Tarne jääk
    - Lao tarnejääk
    - Arve jääk
    - Laoarve jääk
