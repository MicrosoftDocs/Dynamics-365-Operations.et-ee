---
title: Ülesandeloendite loomine ja ülesannete lisamine
description: Selles teemas kirjeldatakse, kuidas rakenduses Microsoft Dynamics 365 Commerce luua ülesandeloendeid ja lisada neile ülesandeid.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 2e6bd69435ee8fe58dbbf66eb0c5eee3d2ec09ee1998ef0218cdef643522c5bf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756521"
---
# <a name="create-task-lists-and-add-tasks"></a>Tööülesannete loendite loomine ja ülesannete lisamine

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas rakenduses Microsoft Dynamics 365 Commerce luua ülesandeloendeid ja lisada neile ülesandeid.

*Ülesanne* määratleb kindla töö või tegevuse, mille keegi peab täitma määratud tähtajal või enne seda. Rakenduses Dynamics 365 Commerce võib ülesanne sisaldada üksikasjalikke juhiseid ja teavet kontaktisiku kohta. See võib sisaldada ka linke kontori toimingutele kassatoimingutele või saidi lehtedele, et aidata parandada produktiivsust ja pakkuda konteksti, mida ülesande omanik ülesande tõhusaks täitmiseks vajab.

*Ülesandeloend* on ülesannete kogum, mis tuleb äriprotsessi osana täita. Näiteks võib olemas olla ülesandeloend, mille uus töötaja peab sisseelamise ajal lõpetama, ülesandeloend õhtustes vahetustes töötvatele kassapidajatele või ülesandeloend, mis tuleb lõpule viia, et valmistada pood ette eelseisvaks pühadeajaks. Rakenduses Commerce saab igale kauplusele või töötajale määrata iga loendi, millel on sihtkuupäev, ja selle saab konfigureerida korduvaks.

Nii juhid kui ka töötajad saavad luua rakenduse Commerce kontoris ülesandeloendeid ja seejärel määrata need poodide komplektile.

## <a name="create-a-task-list"></a>Ülesandeloendi loomine

Ülesandeloendi loomiseks tehke järgmist.

1. Avage **Jaemüük ja kaubandus \> Ülesannete haldus \> Ülesannete halduse administreerimine**.
1. Valige suvand **Uus** ja seejärel sisestage väärtused väljadele **Nimi**, **Kirjeldus** ja **Omanik**.
1. Valige käsk **Salvesta**.

## <a name="add-tasks-to-a-task-list"></a>Ülesandeloendisse ülesannete lisamine

Ülesandeloendisse ülesannete lisamiseks tehke järgmist.
 
1. Olemasoleva ülesandeloendi kiirkaardil **Ülesanded** valige ülesande lisamiseks suvand **Uus**.
1. Sisestage olemi nimi dialoogiboksis **Loo uus ülesanne** väljal **Nimi**.
1. Sisestage positiivne või negatiivne täisarvuline väärtus väljale **Tähtajaliste andmete nihe sihtkuupäevast alates**. Näiteks sisestage **–2**, kui ülesanne tuleb lõpetada kaks päeva enne ülesandeloendi tähtaega.
1. Sisestage üksikasjalised juhised väljale **Märkmed**.
1. Väljale **Kontaktisik** sisestage valdkonna asjatundja nimi, kellega ülesanne omanik saab abi saamiseks ühendust võtta.
1. Sisestage väljale **Ülesande link** ülesande olemuse põhjal link.

> [!TIP]
> Ehkki saate kasutada välja **Määratud:**, et määrata ülesanded kellelegi, kui ülesandeloendit loote, soovitame ülesandeloendi loomise ajal ülesannete määramist vältida. Selle asemel määrake ülesanded pärast seda, kui loend on üksikute poodide jaoks loodud.

## <a name="use-task-links-to-help-improve-worker-productivity"></a>Töötaja tootlikkuse parandamist ülesannete linkide kasutamine

Rakendus Commerce võimaldab teil linkida ülesanded konkreetsete kassatoimingutega, nagu müügiaruande käitamine, uue töötaja juhendamiseks veebipõhise õppevideo vaatamine või kontoritoimingute tegemine. See funktsioon aitab ülesannete omanikel saada teavet, mis on ülesande tõhusaks täitmiseks vaja.

Ülesande linkide lisamiseks ülesande loomise ajal toimige järgmiselt.

1. Olemasoleva ülesandeloendi kiirkaardil **Ülesanded** valige suvand **Redigeeri**.
1. Dialoogiboksis **Redigeeri ülesannet** väljal **Ülesande link** valige üks või mitu järgmistest valikutest.

    - Valige suvand **Menüü-üksus**, et konfigureerida kontori toiming, nagu „Tootekomplektid”.
    - Valige suvand **Kassatoiming**, et konfigureerida kassatoiming, näiteks „Müügiaruanded”.
    - Valige absoluutse URL-i konfigureerimiseks suvand **URL**.

Järgmisel joonisel on näidatud ülesande linkide valimine dialoogiboksis **Redigeeri ülesannet**.

![Ülesande linkide valimine ülesande redigeerimise dialoogiboksis.](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a>Kassatoimingu konfigureerimine, et selle saaks ülesandega linkida

Kassatoimingu konfigureerimine, et selle saaks ülesandega linkida, tehke järgmist.

1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassa \> Kassatoimingud**.
1. Valige käsk **Redigeer**, leidke kassatoiming ja märkige seejärel selle märkeruut **Luba ülesande haldus**.

## <a name="additional-resources"></a>Lisaressursid

[Ülesannete halduse ülevaade](task-mgmt-overview.md)

[Ülesannete halduse konfigureerimine](task-mgmt-configure.md)

[Ülesandeloendite määramine poodidele või töötajatele](task-mgmt-assign-lists.md)

[Ülesannete haldus kassas](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
