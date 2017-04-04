---
title: Sortimentide seadistamine
description: "Selles artiklis kirjeldatakse, mida valik on ja selgitatakse, kuidas seadistada Microsoft Dynamics 365 toiminguteks - jaemüügi sortimentide."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 906fc6eb42eb54cb3a3d5621377f250f59de20d7
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-assortments"></a>Sortimentide seadistamine

Selles artiklis kirjeldatakse, mida valik on ja selgitatakse, kuidas seadistada Microsoft Dynamics 365 toiminguteks - jaemüügi sortimentide.

Valik on määrata jaemüügi kanali, näiteks tellis-ja uhmris poes või poe seonduvate toodete kogum. Sortimentide abil saate tuvastada igas kaupluses saadaolevaid tooteid. Sortiment võib sisaldada tootekategooriaid. Seega sisaldab sortiment kindlale kategooriale määratud tooteid. Sortiment võib sisaldada ka kindlaid tooteid ja tootevariante. Sortimendi seadistamisega saate määrata oma jaemüügikanalitele samal ajal mis tahes kombinatsioonis, mida teie kauplused vajavad, tuhandeid tooteid. Saate seadistada nii palju tootesortimente kui vaja. Iga toote saab lisada ühte või mitmesse sortimenti ja iga sortimendi saab määrata ühele või mitmele jaemüügikanalile. Näiteks määratlete ühe sortimendi, mis sisaldab toodete põhikomplekti. Selle sortimendi saavad kõik kauplused. Seejärel määratlete teise sortimendi, mis sisaldab ainult suuri spordivahendeid. Selle sortimendi saavad ainult teie suuremad kauplused. Järgmisel joonisel on näidatud, kuidas saab tooteid sortimentidele määrata ja kuidas neid sortimente jaemüügikanalitele määrata. ![Tootesortimendi seosed](./media/assortments_relationship.gif)

## <a name="prerequisites"></a>Eeltingimused 
Enne kui saate sortimendi seadistada ja jaemüügikanalile määrata, peate täitma järgmised ülesanded.

| Ülesanne                              | Kirjeldus                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jaemüügikanali seadistamine.          | Jaemüügikanal kujutab endast traditsioonilist kauplust, võrgupoodi või võrguturuplatsi. Peate seadistama vähemalt ühe jaemüügikanali ja konfigureerima kaupluse jaoks suvandid. Sortimendid määratakse kauplustele, et tuvastada tooted, millega kindel kauplus tegeleb.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Organisatsioonihierarhia loomine. | Kui olete oma organisatsiooni jaoks jaemüügikanalid seadistanud, peate konfigureerima jaemüügi organisatsioonihierarhia, mis kujutab teie jaemüügikanalite organisatsioonilist struktuuri. Organisatsioonihierarhiat saab kasutada sortimentide, täiendamise ja aruandluse jaoks. Lisades jaemüügikanalid organisatsioonihierarhiasse, saate määrata sortimendid kaupluste gruppidele. Selle asemel, et määrata igale kauplusele eraldi sortiment, määrate sortimendi kõrgemal tasemel organisatsioonisõlmele. Kui nüüd kõrgemal tasemel organisatsioonisõlmele lisatakse uus jaemüügikanal, pärib see automaatselt kõik sortimendid, mis on kõrgemal tasemel organisatsioonisõlmele määratud. Saate määrata sortimentid ainult jaemüügikanalitele, mis kuuluvad organisatsioonihierarhiasse, millele on määratud otstarve **Jaemüügi sortiment**. |
| Toodete määratlemine.                  | Enne kui saate tooteid sortimenti lisada, peate need lisama Microsoft Dynamics AX-is. Saate tooteid lisada käsitsi või importida need hankijalt. Pärast toodete lisamist peate need juriidilisele isikule väljastama. Jaemüügikanalitele saab kättesaadavaks teha ainult juriidilisele isikule väljastatud tooteid. Tooted, mis pole veel juriidilisele isikule väljastatud, saab sortimenti lisada ja sortimendi saab kinnitada. Tooteid ei saa siiski jaemüügikanalitele enne kättesaadavaks teha, kui need on juriidilisele isikule väljastatud.                                                                                                                                                                                                                                                                                     |
| Kategooriahierarhia seadistamine.      | Jaemüügi tooted loomisel saate rühmitada ja liigitada neid operatsioonide Dynamics 365 kategooria hierarhia funktsiooni abil. Saate luua ühe tuumhierarhia kõigi toodete grupeerimiseks ja kategoriseerimiseks, mida oma jaemüügikanalite kaudu levitate. Saate luua ka eraldi täiendavaid kategooriahierarhiaid toodete grupeerimiseks või kategoriseerimiseks kindlal otstarbel, näiteks kampaaniate või sortimentide jaoks. Kategooriahierarhiate abil saate määrata sortimendile kõik kindlas kategoorias olevad tooted. Kõik sortimenti kuuluvasse kategooriasse lisatud tooted lisatakse automaatselt sortimenti. Jaemüügisortimendi ajasti järgmisel käivitamisel muutuvad need tooted kättesaadavaks jaemüügikanalitele, millele sortiment on määratud.                                            |

## <a name="setting-up-an-assortment"></a>Sortimendi seadistamine
Pärast eeltingimuste täitmist saate luua sortimendi ja määrata selle oma jaemüügikanalitele. Sortimendi seadistamiseks täitke järgmised ülesanded.

1.  Looge uus sortiment või kopeerige olemasolev.
2.  Valige jaemüügikanalid või jaemüügikanalite kõrgema taseme grupid, millele sortiment kohaldub.
3.  Lisage sortimendile tootekategooriad, üksikud tooted või tootevariandid. Saate kaasata kõik kindla kategooria tooted või välistada valitud tooteid sortimenti kaasatud kategooriast.
4.  Avaldage sortiment. Sortimendi avaldamisel käivitatakse jaemüügisortimendi ajasti automaatselt. See protsess loob toodete loendi. Kui see protsess on lõpule viidud, muutuvad tooted kättesaadavaks jaemüügikanalitele, millele on tootesortiment määratud. Avaldatud sortimendi või jaemüügikanalite, millele sortiment on määratud, muutmisel tuleb sortimenti värskendada. Sortimendi värskendamiseks pärast muudatuste tegemist saate käivitada jaemüügisortimendi ajasti pakett-tööna.



