---
title: Kordustellimuse arvelduse Power BI sisu
description: See artikkel kirjeldab, mida kaasatakse kordustellimuse arvelduse sisusse Microsoft Power BI.
author: JodiChristiansen
ms.date: 04/13/2022
ms.topic: article
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-04-13
ms.openlocfilehash: 6cee01eb5b8bb8296b6e7f638b565c999ccc023e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849956"
---
# <a name="subscription-billing-power-bi-content"></a>Kordustellimuse arvelduse Power BI sisu

[!include[banner](../includes/banner.md)]

See artikkel kirjeldab, mida kaasatakse kordustellimuse arvelduse sisusse Microsoft Power BI. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele, ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks. 

## <a name="overview"></a>Ülevaade

Kordustellimuse arveldussisu Power BI loodi kordustellimuse arveldusametnike ja haldurite jaoks. See pakub kordustellimuse arvelduse võtmemõõdikuid, nagu korduv igakuine tulu (MRR) arveldusgraafikute jaoks, ning väheneva saldo ja viitvõlagraafikute teabe. See kasutab arveldusgraafikute ja viitvõlagraafikute andmeid korduvate tulude ja tulude ülevaate andmiseks.

Sisul Power BI on kolm järgmist vahekaarti, mis pakuvad kokku nelja analüütilist aruannet: 

- **Analüüs – MRR** – see vahekaart annab igakuise korduva **arvelduse** aruande ja arveldusgraafiku **üksikasjade** aruande.
- **Analüüs – Saate** sellel vahekaardil luua **aruande** Tulud.
- **Analüüs – vähenev saldo** – see vahekaart annab väheneva **saldo** aruande.

## <a name="view-data-on-the-analytical-reports"></a>Analüütiliste aruannete andmete kuvamine

Enne, kui saate vaadata analüütiliste aruannete andmeid, peate käivitama perioodilise protsessi, mis loob aruande andmed iga aruande jaoks. Need andmed, mida aruanded nõuavad, peavad olema loodud, kuna neid ei talletata otse andmebaasi. 

1. Minge kordustellimuse **arveldamise \> korduva lepingu arvelduse perioodiliste \> ülesannete \> MRR-i analüütilise aruande pakktöötlusesse** ja järgige neid samme.

    1. Saate sisestada kuupäevavahemiku, mis ei ole suurem kui kolm aastat.
    2. Valikuline: seadistage korduv pakett-töö andmete perioodiliseks värskendamiseks.
    3. Valige nupp **OK**.

2. Kui pakett-töö on käitamise lõpetanud, minge süsteemihalduse **\> häälestusüksuse \> kauplusesse** ja värskendage **MRR-aruande agregaatormõõtu**. 
3. Minge kordustellimuse **arveldustulu \> ja kulu viitvõlgade perioodiliste ülesannete analüütilise \> aruande \>** analüütilise aruande pakktöötluse juurde ja järgige neid samme.

    1. Sisestage alguskuupäev ja lõppkuupäev, mis hõlmab kuni 26 perioodi. 
    2. Kui soovite vaadata praeguse perioodi möödunud perioodide prognoositud summat, **määrake praeguse perioodi prognoosi möödunud** **summade suvandiks Jah**.
    3. Valikuline: seadistage korduv pakett-töö andmete perioodiliseks värskendamiseks.
    4. Valige nupp **OK**. 

4. Kui pakett-töö on käitamise lõpetanud, minge Süsteemihalduse **\> häälestusüksuse \> kauplusesse** ja värskendage Mõõtühiku aruande **kokkuvõtte** mõõtmist.
5. Minge kordustellimuse **arveldamise \> tulu ja kulu viitvõlgade perioodiliste ülesannete \> alla \>, mis vähenevad saldo analüüsiaruande pakktöötlusega**, ja järgige neid samme.

    1. Sisestage alguskuupäev ja lõppkuupäev, mis hõlmab kuni 26 perioodi. 
    2. Kui soovite vaadata praeguse perioodi möödunud perioodide prognoositud summat, **määrake praeguse perioodi prognoosi möödunud** **summade suvandiks Jah**.
    3. Valikuline: seadistage korduv pakett-töö andmete perioodiliseks värskendamiseks.
    4. Valige nupp **OK**.

6. Kui pakett-töö on käitamise lõpetanud, minge süsteemihalduse **\>\> häälestusüksuse** kauplusesse ja värskendage **väheneva saldo aruande kokkuvõtte** mõõtmist.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule

Kordustellimuse arveldussisu Power BI kuvatakse kordustellimuse arvelduse **tööruumis**.
