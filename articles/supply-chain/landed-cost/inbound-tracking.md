---
title: Sissetulevate reiside ja saatmiskonteinerite teekondade jälgimine
description: See teema selgitab, kuidas saate kasutada lehte Sissetulevate jälgimine, et jälgida oma reiside edenemist ja saatmiskonteinerite teekondi.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainerActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 67ee22af7a73c18d4f77018fedf5a89f0777774d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580764"
---
# <a name="track-inbound-voyages-and-shipping-container-journeys"></a>Sissetulevate reiside ja saatmiskonteinerite teekondade jälgimine

[!include [banner](../../includes/banner.md)]

Leht **Sissetulevate jälgimine** võimaldab teil jälgida oma reiside edenemist ja saatmiskonteinerite teekondi. Iga reis ja teekond on jaotatud *tegevusteks*, millest igaühel on lehel oma rida. Saate kasutada lehte, et vaadata ja sisestada hinnangulisi kuupäevi ja tegelikke kuupäevi tegevuse kaupa.

Tavaliselt näitavad tegevused automaatselt eeldatud maabumisaega lõppsihtkohas, olenevalt menüü [Jälgimiskeskus](delivery-information-setup.md#tracking-control-center) seadistusest. Sõltuvalt seadistusest värskendab lõppkuupäev tavaliselt ostutellimuse ridadel ka tarnekuupäeva või kinnitatud kuupäeva. Üleviimistellimuse ridade korral saate seadistada süsteemi värskendama vastuvõtukuupäeva.

Lehe **Sissetulevate jälgimine** avamiseks valige **Väljalaadimiskulu \> Jälgimine \> Sissetulevate jälgimine**.

## <a name="filter-the-activities-list"></a>Tegevuste loendi filtreerimine

Saate lehe **Sissetulevate jälgimine** ülaserva välju **Reis** ja **Saatmiskonteiner** kasutada lehe filtreerimiseks nii, et see näitab ainult valitud reisiga ja/või saatmiskonteineriga seostatud tegevusi.

## <a name="update-tracking-information"></a>Jälgimisteabe värskendamine

Reisi või teekonna graafiku värskendamiseks sisestage esimese tegevuse alguskuupäev. Seejärel värskendatakse viimase tegevuse hinnanguline lõppkuupäev. Menüü [Jälgimiskeskus](delivery-information-setup.md#tracking-control-center) seadistus iga etapi ja teekonnamalli jaoks määrab kindlaks eeldatavad täitmisajad. Eeldatavad lõppkuupäevad kasutavad täitmisaega alates tegevuse alguskuupäevast. Seejärel värskendatakse pärast tegeliku lõppkuupäeva registreerimist järgmise tegevuse alguskuupäev eelmise tegevuse tegeliku lõppkuupäevaga samaks kuupäevaks. Võrdluse ja analüüsi võimaldamiseks värskendatakse tegelik täitmisaeg. Lisamärkused saab sisestada väljale **Märkus**.

Tegevuste järjestus ruudustikus määratakse vastava teekonnamalli etappide järjestuse järgi. Kui seotud teekonna etappide järjestus muutub, muutub ka jälgimiskontroll.

Kõigi konteinerite kuupäevade värskendamiseks valige toimingupaanil **Värskenda alguskuupäeva** või **Värskenda tegelikku lõppkuupäeva**. Teise võimalusena saate sisestada saadetise kuupäevad konteineri kaupa. See viis on paindlikum, kuna konteinerid saab mitme teekonnaga keskkonnas jaotada.

## <a name="buttons-on-the-action-pane"></a>Toimingupaani nupud

Lehe **Sissetulevate jälgimine** toimingupaani nuppe saate kasutada sissetulevate reisidega ja teekondadega töötamiseks. Järgmises tabelis on saadaolevaid nuppe lähemalt kirjeldatud.

| Nupp | Kirjeldus |
|---|---|
| Redigeeri | Redigeerige reisi või saatmiskonteineri teekonda. |
| New | Looge uus reis või saatmiskonteineri teekond. |
| Kustutamine | Kustutage valitud reis või saatmiskonteineri teekond. |
| Uuenda alguskuupäeva | Värskendage reisi kõigi konteinerite tegevuse alguskuupäeva. Kui kindla tegevuse või teekonnaetapi alguskuupäeva värskendatakse, värskendatakse määratud täitmisaja põhjal järgnevad eeldatavad alguskuupäevad. |
| Uuenda tegelikku lõppkuupäeva | Värskendage reisi kõigi konteinerite tegevuse lõppkuupäeva. Kui kindla tegevuse lõppkuupäeva värskendatakse, värskendatakse määratud täitmisaja põhjal järgnevad tegevused. |
| Lisa tegevused | Lisage reisile tegevus käsitsi. Näiteks saate soovi korral lisada suitsutamistegevuse. Lisanduse korral võib muutuda laeva või teekonna kaupade kinnitatud tarnekuupäev. Kui teekonda lisatakse tegevus, ei sisestata hinnangulisi päevi enne, kui teekonnaetapi alguskuupäev on värskendatud. |

## <a name="information-and-settings-on-the-overview-tab"></a>Teave ja sätted vahekaardil Ülevaade

Vahekaart **Ülevaade** kuvab loendi kõikidest tegevustest, mis kuuluvad lehe ülaosas valitud reisi ja/või saatmiskonteinerisse. Järgmises tabelis kirjeldatakse iga tegevuse jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Etapp | Tegevuse etapi ID, nagu on määratud teekonnamallis. |
| Tarneviis | Tegevuse eeldatav tarneviis. |
| Tegevus | See väli tähistab tavaliselt tegevusega seostatud tööd või ülesannet. Tüüpilised näited on *Laevasõit* ja *Tolli läbimine*. |
| Kirjeldus | Tegevuse pikem kirjeldus. |
| Alguskuupäev | Sellel väljal kuvatakse algselt tegevuse eeldatav alguskuupäev. Kuid pärast eelmise tegevuse tegeliku lõppkuupäeva sisestamist näitab see tegelikku alguskuupäeva. Seda välja kasutatakse täitmisaja alusel eeldatava lõppkuupäeva kindlaksmääramiseks. |
| Eeldatav lõppkuupäev | Selle välja väärtus arvutatakse alguskuupäeva ja täitmisaja alusel. Tavaliselt ei redigeeri te väärtust otse. |
| Tegelik lõppkuupäev | Kasutaja peaks seda välja värskendama võimalikult kiiresti pärast tegevuse toimumist. Seejärel värskendatakse tegelik täitmisaeg. |
| Prognoositud päevad | Prognoositud aeg (päevades), mis on vajalik tegevuse lõpuleviimiseks. |
| Tegelikud päevad | Tegelik aeg (päevades), mis on vajalik tegevuse lõpuleviimiseks. |
| Paberraha | Sellel väljal saate lisada tegevuse kohta muid lisamärkusi ja üksikasju. |

## <a name="information-and-settings-on-the-general-tab"></a>Teave ja sätted vahekaardil Üldine

Vahekaardil **Üldine** kuvatakse vahekaardil **Ülevaade** valitud etapi teave. Kuigi sellel kordub osa vahekaardil **Ülevaade** kuvatavat teavet, sisaldab see valitud etapi kohta ka lisateavet.
