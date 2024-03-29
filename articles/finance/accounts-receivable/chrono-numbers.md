---
title: Dokumentide ja kannete nummerdamine kronoloogiliselt
description: See artikkel selgitab, kuidas seadistada ja kasutada rakendatavate dokumentide ja seotud kannete kronoloogilised numbrid.
author: ikond
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.custom: 401195
ms.search.form: NumberSequenceGroup
ms.openlocfilehash: 1a1b8887eff625d9e4095380fbb7c8963682ef3c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272424"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a>Dokumentide ja kannete nummerdamine kronoloogiliselt

[!include [banner](../includes/banner.md)]


Mõnes riigis on dokumentide ja seotud kannete kronoloogilises järjestuses nummerdamine juriidiliselt nõutud. Kronoloogia peab hõlmama perioode. Kõik varasemate perioodide numbrid peavad olema hilisemate perioodide numbritest väiksemad. Selle nõude täitmiseks on juurutatud kronoloogilise nummerdamise funktsioon. See artikkel selgitab, kuidas konfigureerida ja kasutada rakendatavate dokumentide ja seotud kannete kronoloogilised numbrid.

## <a name="prerequisites"></a>Eeltingimused

Lülitage tööruumis Funktsioonihaldus sisse funktsioon **Kronoloogiline nummerdamine**. Lisateavet vt [Funktsioonihalduse ülevaatest](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-chronological-numbering"></a>Kronoloogilise nummerdamise konfigureerimine

Kronoloogiline nummerdamine mõjutab järgmisi dokumente.

**Müügireskontro**
- Kliendiarve
- Kliendiarve kanne
- Müügi kreeditarve
- Müügi kreeditarve kanne
- Vabas vormis arve
- Vabas vormis arve kanne
- Vabas vormis kreeditarve
- Vabas vormis kreeditarve kanne
- Saateleht
- Saatelehe kanne
- Saatelehe paranduskanne
- Viivisearve kanne
- Märgukirja kanne

**Ostureskontro**
- Arve kanne
- Kreeditarve kanne
- Toote sissetuleku kanne

**Projektihaldus**
- Arve
- Arve kanne
- Kreeditarve
- Kreeditarve kanne 

### <a name="define-number-sequences"></a>Numbriseeriate määratlemine

Numbriseeriate määratlemiseks minge jaotisse **Organisatsiooni haldus** > **Numbriseeriad** > **Numbriseeriad**. Saate määratleda nii palju numbriseeriaid, kui on nõutud dokumentide mõjutatud perioodide katmiseks vaja. 

Määrake igale numbriseeriale ettevõte. Numbriseeriate segmendid tuleb määratleda nii, et need korraldavad perioodid kronoloogilisse järjestusse. Näiteks võivad segmentide nimed hõlmata spetsiaalset prefiksit, mis tuvastab konkreetse perioodi.

![Numbriseeriate seadistamine.](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a>Numbriseeriate gruppide konfigureerimine

Numbriseeriate gruppide konfigureerimiseks minge jaotisse **Müügireskontro** > **Seadistus** > **Müügireskontro parameetrid**. Määratlege vahekaardil **Numbriseeriad** mõjutatud perioodide katmiseks vajalike numbriseeriate gruppide arv. 

Valige iga grupi jaoks jaotises **Viide** üks toetatud dokumendiviidetest ja vaadake väljal **Numbriseeria kood** vastava perioodi jaoks eelnevalt loodud numbriseeriat.

![Numbriseeriagrupi seadistus.](media/chrono-num-sequence-group.jpg)

Samuti konfigureerige numbriseeriate grupid moodulites **Ostureskontro** ja **Projektihaldus ja raamatupidamine**.

### <a name="configure-number-sequence-groups-chronology"></a>Numbriseeriate gruppide kronoloogia konfigureerimine

Numbriseeriate gruppide kronoloogia konfigureerimiseks minge jaotisse **Organisatsiooni haldus** > **Numbriseeriad** > **Kronoloogilised numbriseeriate grupid**. Määratlege numbriseeriate gruppide kohaldatavuse tingimused.

![Numbrite seadistamine kronoloogiliselt.](media/chrono-num-sequence-group-period.jpg)

| Field            | Kirjeldus                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jõustunud  | Numbriseeriate grupi kohaldatavuse alguskuupäev. |
| Aegumine      | Numbriseeriate grupi kohaldatavuse lõppkuupäev. Kui lõppkuupäeva ei rakendata, valige **Mitte kunagi**. |
| Numbriseeria grupp | Numbriseeriate grupp, mida kasutatakse selle perioodi jooksul dokumendinumbrite loomiseks. |
| Algne numbrite seeriagrupp | Seda numbriseeriate grupi koodi kasutatakse nende juhtumite täiendavaks filtreerimiseks, kus dokumentidele on juba määratud konkreetne *püsiv* numbriseeriate grupp. Tühja väärtust loetakse konkreetseks väärtuseks. Kui peate algselt määratud gruppi ignoreerima, kasutage selle seadistuse puhul suvandit **Vaikeväärtus**. |
| Vaikimisi | Kui see on sisse lülitatud, ignoreerib süsteem algselt määratud dokumendi numbriseeriate gruppi ja kasutab kohaldatavuse analüüsis ainult perioodide algus- ja lõppkuupäeva. Kui see on välja lülitatud, kasutab süsteem valikute jaoks täiskombinatsiooni **Jõustumine** + **Aegumine** + **Algne numbriseeriate grupp**. |

## <a name="document-posting"></a>Dokumendi sisestamine
Dokumendi sisestamisel määratakse dokumendile selle sisestuskuupäeval põhinev sobiv numbriseeriate grupp ja seejärel kasutatakse seda tuvastatud numbriseeria alusel dokumendi numbri loomiseks. Süsteem edastab numbriseeriate grupi määramise kohta teate.

![Dokumendi number.](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> Mõnes riigis on dokumentide nummerdamiseks juba rakendatud kindel loogika. Sellisel juhul alistab riigipõhine loogika funktsiooni **Kronoloogiline nummerdamine**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
