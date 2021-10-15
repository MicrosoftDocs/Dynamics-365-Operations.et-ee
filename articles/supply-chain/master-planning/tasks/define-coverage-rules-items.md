---
title: Kaubakatte reeglite määratlemine
description: See protseduur näitab, kuidas luua laovarude reegleid ja tühistada kindla kaupa laovarude sätteid. Samuti näitab see, kuidas määrata varude vaikesätteid.
author: ChristianRytt
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15b0ad9faf2bcac25dec01a7ab44f804ad2345cd
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567219"
---
# <a name="define-coverage-rules-for-items"></a>Kaubakatte reeglite määratlemine

[!include [banner](../../includes/banner.md)]

Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. See protseduur näitab, kuidas luua laovarude reegleid ja tühistada kindla kaupa laovarude sätteid. Samuti näitab see, kuidas määrata varude vaikesätteid.

## <a name="create-a-coverage-group"></a>Laovarude grupi loomine

Looge laovarude grupp järgmiselt:

1. Avage **Navigeerimispaan > Moodulid > Koondplaneerimine > Häälestus > Laovarude grupid**.
1. Valige suvand **Uus**.
1. Sisestage väärtus väljale **Laovarude grupp**.
1. Sisestage väärtus väljale **Nimi**.
1. Sisestage väärtus väljale **Kalender**. Valige kalender, mida kasutatakse koondplaneerimises gruppi kuuluvate kaupade täiendamissoovituste loomisel.  
1. Valige suvand väljal **Laovarude kood**. Valige nõue selle protseduuri jaoks.  
1. Sisestage väärtus „90” **väljale Laovarude ajapiir (päevades)**. Sellesse gruppi kuuluvate kaupade jaoks loob koondplaneerimine täiendamise soovitused kuni 90 päeva ette.  
1. Sisestage väärtus „1” väljale **Negatiivsed päevad**.
1. Sisestage väärtus „1” väljale **Positiivsed päevad**.
1. Laiendage või ahendage jaotist **Muu**.
1. Sisestage jaotises **Ohutuspiirid päevades** väljale **Vajaduse kuupäeva sissetuleku ohutusvaru** sisestage 1. Näiteks kui sissetuleku ohutusvaru on seatud 1 päevale ja ostutellimuse rida on planeeritud sissetulekuks 15. mail, siis arvutatakse planeerimisel korrigeeritud sissetulekukuupäevaks 16. mai.
1. Sisestage väärtus „1” väljale **Vajaduse kuupäevast maha arvatud väljamineku ohutusvaru**. Näiteks kui ohutusvaru on seatud 1 päevale ja müügitellimuse rida on planeeritud tarnimiseks 15. mail, siis arvutatakse koondplaneerimisel korrigeeritud tarnekuupäevaks 14. mai.  
1. Sisestage väärtus „1” väljale **Kauba täitmisajale lisatud lisatellimuse ohutusvaru**.
1. Valige käsk **Salvesta**.

## <a name="create-a-new-product"></a>Uue toote loomine

Looge uus toode järgmiselt:

1. Avage **Navigeerimispaan > Moodulid > Tooteteabe haldus > Tooted > Väljastatud tooted**.
1. Valige suvand **Uus**.
1. Sisestage väärtus väljale **Toote number**.
1. Sisestage väärtus väljale **Toote nimi**.
1. Klõpsake väljal **Kauba mudeli rühm** otsingu avamiseks ripploendi nuppu.
1. Otsige loendist ja valige soovitud kirje.
1. Valige loendis link valitud reas.
1. Klõpsake väljal **Kauba rühm** otsingu avamiseks ripploendi nuppu.
1. Otsige loendist ja valige soovitud kirje.
1. Valige loendis link valitud reas.
1. Klõpsake väljal **Laoala dimensiooni rühm** otsingu avamiseks ripploendi nuppu.
1. Otsige loendist ja valige soovitud kirje.
1. Valige loendis link valitud reas.
1. Klõpsake väljal **Jälgimisdimensiooni rühm** otsingu avamiseks ripploendi nuppu.
1. Otsige loendist ja valige soovitud kirje.
1. Valige loendis link valitud reas.
1. Valige nupp **OK**.

## <a name="set-up-default-order-settings"></a>Seadistage tellimuse vaikeseaded

Seadistage tellimuse vaikeseaded järgmiselt:

1. Valige **Toimingupaanil** nupp **Plaan**.
1. Suvandil **Tellimuse sätted** valige **Tellimuse vaikesätted**.
1. Sisestage **Ostutellimuste** loomisel vaikekohana kasutatav koht väljal **Ostukoht**.
1. Sisestage väljale **Varude tegevuskoht** kaupa hoidmise asukoht.
1. Laiendage või ahendage jaotist **Laoseis**.
1. Sisestage väljale **Mitu** väärtus „10“.
1. Tippige väljale **min. tellimuse kogus** väärtus 10.
1. Tippige väljale **maks. tellimuse kogus** väärtus 100.
1. Tippige väljale **standard tellimuse kogus** väärtus 10.
1. Sisestage number väljale **Ostu täitmisaeg**.
1. Valige või puhastage märkeruut **Tööpäevad**.
1. Valige käsk **Salvesta**.
1. Väljal **Vaiketellimuse tüüp** valige „Ostutellimus“.
1. Valige käsk **Salvesta**.
1. Sulgege leht. Sulgege leht Tellimuse vaikesätted.  

## <a name="add-an-item-to-a-coverage-group"></a>Kauba lisamine laovarude gruppi

Lisage toode laovarude gruppi järgmist tehes:

1. Laiendage või ahendage jaotist **Plaan**.
1. Valige väljal **Laovarude grupp** otsingu avamiseks ripploendi nuppu.
1. Leidke loendist loodud **laovarude grupp**.
1. Valige loendis link valitud reas.

## <a name="create-item-coverage-rules"></a>Kauba laovarude reeglite loomine

Looge kaubavarude reeglid järgmiselt:

1. Valige **Toimingupaanil** nupp **Plaan**.
1. Jaotises **Laovarud** klõpsake valikut **Kaubavaru**.
1. Valige suvand **Uus**.
1. Valige vahekaart **Üldine**.
1. Märkige ruut suvandi **Tühista laovarude rühma** sätted päises.
1. Sisestage väärtus „60” väljale **Laovarude ajapiir (päevades)**. Kuigi kaubad laovarude grupis Vajadus on plaanitud 90 päeva ette, plaanitakse see kaup 60 päeva ette.  
1. Sisestage väärtus „2” väljale **Negatiivsed päevad**.
1. Sisestage väärtus „2” väljale **Positiivsed päevad**.
1. Klõpsake vahekaarti **Täitmisaeg**.
1. Märkige ruut suvandi **Ost** päises.
1. Sisestage väljale **Ostu aeg** väärtus „5“.
1. Valige käsk **Salvesta**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]