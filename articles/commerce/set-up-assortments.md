---
title: Sortimentide seadistamine
description: Selles artiklis kirjeldatakse, mis asi on sortiment, ja selgitatakse, kuidas sortimente rakenduses Dynamics 365 Commerce seadistada.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: bbe7749e6c8293ded933611d6f1084b89223302c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790978"
---
# <a name="set-up-assortments"></a>Sortimentide häälestamine

[!include [banner](includes/banner.md)]

Selles artiklis kirjeldatakse, mis asi on sortiment, ja selgitatakse, kuidas sortimente rakenduses Dynamics 365 Commerce seadistada.

Sortiment on kogum seotud tooteid, mille määrate kaubanduse kanalile, nagu füüsiline kauplus või veebipood. Sortimentide abil saate tuvastada igas kaupluses saadaolevaid tooteid. Sortiment võib sisaldada tootekategooriaid. Seega sisaldab sortiment kindlale kategooriale määratud tooteid. Sortiment võib sisaldada ka kindlaid tooteid ja tootevariante. Sortimendi seadistamisega saate määrata oma kanalitele samal ajal mis tahes kombinatsioonis, mida teie kauplused vajavad, tuhandeid tooteid. Saate seadistada nii palju tootesortimente kui vaja. Iga toote saab lisada ühte või mitmesse sortimenti ja iga sortimendi saab määrata ühele või mitmele kanalile. Näiteks määratlete ühe sortimendi, mis sisaldab toodete põhikomplekti. Selle sortimendi saavad kõik kauplused. Seejärel määratlete teise sortimendi, mis sisaldab ainult suuri spordivahendeid. Selle sortimendi saavad ainult teie suuremad kauplused. Järgmisel joonisel on näidatud, kuidas saab tooteid sortimentidele määrata ja kuidas neid sortimente kanalitele määrata.

![Tootesortimendi seosed](./media/assortments_relationship.gif)

## <a name="prerequisites"></a>Eeltingimused

Enne kui saate sortimendi seadistada ja kaubanduse kanalile määrata, peate täitma järgmised ülesanded.

| Ülesanne                              | Kirjeldus |
|-----------------------------------|-------------|
| Seadistage kanal.          | Kanalid kujutavad endast füüsilist kauplust, veebipoodi või võrguturuplatsi. Peate seadistama vähemalt ühe kanali ja konfigureerima kaupluse jaoks suvandid. Sortimendid määratakse kauplustele, et tuvastada tooted, millega kindel kauplus tegeleb. |
| Organisatsioonihierarhia loomine. | Kui olete oma organisatsiooni jaoks kaubanduse kanalid seadistanud, peate konfigureerima organisatsioonihierarhia, mis kujutab teie kanalite organisatsioonilist struktuuri. Organisatsioonihierarhiat saab kasutada sortimentide, täiendamise ja aruandluse jaoks. Lisades kanalid organisatsioonihierarhiasse, saate määrata sortimendid kaupluste gruppidele. Selle asemel, et määrata igale kauplusele eraldi sortiment, määrate sortimendi kõrgemal tasemel organisatsioonisõlmele. Kui nüüd kõrgemal tasemel organisatsioonisõlmele lisatakse uus kanal, pärib see kanal automaatselt kõik sortimendid, mis on kõrgemal tasemel organisatsioonisõlmele määratud. Saate määrata sortimentid ainult kanalitele, mis kuuluvad organisatsioonihierarhiasse, millele on määratud otstarve **Kaubanduse sortiment**. |
| Toodete määratlemine.                  | Enne kui saate tooteid sortimenti lisada, peate need lisama Commerce’is. Saate tooteid lisada käsitsi või importida need hankijalt. Pärast toodete lisamist peate need juriidilisele isikule väljastama. Kanalitele saab kättesaadavaks teha ainult juriidilisele isikule väljastatud tooteid. Tooted, mis pole veel juriidilisele isikule väljastatud, saab sortimenti lisada ja sortimendi saab kinnitada. Tooteid ei saa siiski kanalitele enne kättesaadavaks teha, kui need on juriidilisele isikule väljastatud. |
| Kategooriahierarhia seadistamine.      | Kaubanduse toodete loomisel saate grupeerida ja kategoriseerida need kategooriahierarhia funktsiooni abil. Saate luua ühe tuumhierarhia kõigi toodete grupeerimiseks ja kategoriseerimiseks, mida oma kanalite kaudu levitate. Saate luua ka eraldi täiendavaid kategooriahierarhiaid toodete grupeerimiseks või kategoriseerimiseks kindlal otstarbel, näiteks kampaaniate või sortimentide jaoks. Kategooriahierarhiate abil saate määrata sortimendile kõik kindlas kategoorias olevad tooted. Kõik sortimenti kuuluvasse kategooriasse lisatud tooted lisatakse automaatselt sortimenti. Kaubanduse sortimendi ajasti järgmisel käivitamisel muutuvad need tooted kättesaadavaks kanalitele, millele sortiment on määratud. |

## <a name="setting-up-an-assortment"></a>Sortimendi seadistamine

Pärast eeltingimuste täitmist saate luua sortimendi ja määrata selle oma kanalitele. Sortimendi seadistamiseks täitke järgmised ülesanded.

1. Looge uus sortiment või kopeerige olemasolev.
2. Valige kanalid või kanalite kõrgema taseme grupid, millele sortiment kohaldub.
3. Lisage sortimendile tootekategooriad, üksikud tooted või tootevariandid. Saate kaasata kõik kindla kategooria tooted või välistada valitud tooteid sortimenti kaasatud kategooriast.
4. Avaldage sortiment. Sortimendi avaldamisel käivitatakse sortimendi ajasti automaatselt. See protsess loob toodete loendi. Kui see protsess on lõpule viidud, muutuvad tooted kättesaadavaks kanalitele, millele on tootesortiment määratud. Avaldatud sortimendi või kanalite, millele sortiment on määratud, muutmisel tuleb sortimenti värskendada. Sortimendi värskendamiseks pärast muudatuste tegemist saate käivitada sortimendi ajasti pakett-tööna.


[!INCLUDE[footer-include](../includes/footer-banner.md)]