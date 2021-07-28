---
title: Sissejuhatus -i lokaliseerimisfunktsioonidesse
description: Selles teemas antakse ülevaade funktsionaalsetest asukohtadest varahalduses.
author: johanhoffmann
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationEditSubLocations, EntAssetFunctionalLocationLookup, EntAssetFunctionalLocationRename, EntAssetFunctionalLocation
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2214"
- intro-internal
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f31504d2e4ce61e64eb96c2b69326bcb4f1f2560
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/03/2021
ms.locfileid: "6337095"
---
# <a name="introduction-to-functional-locations"></a>Sissejuhatus -i lokaliseerimisfunktsioonidesse

[!include [banner](../../includes/banner.md)]

 

Selles teemas antakse ülevaade funktsionaalsetest asukohtadest varahalduses. Funktsionaalsed asukohad on tehnilise struktuuri elemendid, näiteks süsteemi funktsionaalsed üksused. Funktsionaalseid asukohti luuakse hierarhiliselt ja te installite neile varasid. Funktsionaalsete asukohtade seadistamine teie ettevõttes sõltub ettevõtte vajadustest.

Siin on mõned näited selle kohta, kuidas funktsionaalseid asukohti kasutada.

- **Funktsionaalne** – funktsionaalsed asukohad võivad olla kasutajapõhised ja neid võib kasutada sarnase kätimusega varade haldamiseks.
- **Protsessiga seotud** – funktsionaalsed asukohad võivad olla töövoopõhised.
- **Ruumiline** – funktsionaalsed asukohad võivad esindada geograafilisi asukohti või saite.

Iga funktsionaalset asukohta hallatakse varahalduses eraldi. Järgnevalt on toodud mõned nõudluse prognoosimise peamised funktsioonid:

- Seadistage funktsionaalse asukoha täpsustused.
- Seadistage vara täpsustuse vajadused.
- Seadistage hoolduse järjestused ennetava ja reaktiivse hoolduse jaoks.
- Installitud varade haldamine.
- Jälgige aktiivseid taotlusi ja töötellimusi, mis on seotud installitud varadega.
- Jälgige varadega registreeritud vigu.
- Saate jälgida hoolduskulusid, mis on seotud funktsionaalse asukohaga igal ajal.

Funktsionaalsed asukohad võimaldavad varade jälgitavust seoses taotluste, töötellimuste, vigade registreerimiste, seisundi hindamiste, tootmise peatamise registreerimiste ja varade loenduri registreerimistega.

> [!NOTE]
> Isegi kui vara on paigaldatud eri funktsionaalsetele asukohtadele selle eluea jooksul, võivad kulud olla seotud iga asukohaga. Teisisõnu, varakulud on alati seotud funktsionaalse asukohaga, kuhu vara konkreetsel ajal installiti.

Funktsionaalsed asukohad **ei ole** paindlikud. Seetõttu pärast funktsionaalse asukoha hierarhia häälestamist ei saa asukohti teisaldada. 

Pärast funktsionaalse asukoha hierarhia loomist on järgmiseks sammuks sellele vara installimine. Lisateavet leiate teemast [Objektide installimine funktsionaalsetes asukohtades](../functional-locations/install-objects-on-functional-locations.md).

## <a name="all-functional-locations"></a>Kõik funktsionaalsed asukohad

Valige **Varahaldus**\>**Ühised**\>**Funktsionaalsed asukohad**\>**Kõik funktsionaalsed asukohad**, et avada loendileht **Kõik funktsionaalsed asukohad**. Sellel lehel kuvatakse kõik funktsionaalsed asukohad ja osa iga asukohaga seotud teabest. Ainult aktiivsete funktsionaalsete asukohtade vaatamiseks valige **Aktiivsed funktsionaalsed asukohad**. Ainult töötajana seotud funktsionaalsete asukohtade vaatamiseks valige **Minu aktiivsed funktsionaalsed asukohad**. (See seos on seadistatud lehel **Töötajad**. Lisateavet lugege teemast [Hooldustöötajad ja töötajate grupid](../setup-for-objects/workers-and-worker-groups.md).)

Loendilehel **Kõik funktsionaalsed asukohad** valige link veerus **Funktsionaalne asukoht**, et vaadata valitud kirje üksikasju. Funktsionaalse asukoha redigeerimiseks valige nupp **Redigeeri**. Üksikasjade vaade näitab üksikasjalikku teavet, mis on seotud asukohaga. See sisaldab ka paani **Seotud teave**, mis asub paremal. Sellel paanil kuvatakse funktsionaalse asukoha hierarhia. Saate laiendada ja ahendada paani **Seostuv teabe**.

Tegumiriba nupud on korraldatud vahekaartidel. Järgmises tabelis kirjeldatakse lühidalt mooduli Asse Management nuppe.

| Nupu nimi                         | Kirjeldus                                                                                                                                  |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Redigeerimine                                | Saate vahetada lehe redigeerimisrežiimi ja vaaterežiimi vahel.                                                                                         |
| Uus                                 | Uue hüvitise asukoha loomine                                                                                                            |
| Kustutamine                              | Valitud hüvitise asukoha kustutamine                                                                                                     |
| Nimeta ümber                              | Nimetage valitud funktsionaalne asukoht ümber.                                                                                                     |
| Kopeeri funktsionaalne asukohastruktuur  | Kopeerige funktsionaalse asukoha hierarhia.                                                                                                      |
| Vara installimine                       | Installige vara, sh tütarvara, funktsionaalses asukohas.                                                                        |
| Vara asendamine                       | Asendage varade hierarhia muu vara hierarhiaga funktsionaalses asukohas.                                                         |
| Kulude jälitamine                        | Avage leht **Funktsionaalse asukoha kulude jälitamine**, kus saate teha valitud funktsionaalse asukoha kulu kalkulatsiooni.                |
| Tundide kontroll                        | Avage leht **Funktsionaalse asukoha tundide kontroll**, kus saate teha valitud funktsionaalse asukoha kulu kalkulatsiooni.                |
| Varad                              | Avage leht **Kõik varad**, kus saate vaadata valitud funktsionaalse asukohaga seotud varade loendit.                      |
| Nõuded                            | Avage leht **Aktiivsed taotlused**, kus saate vaadata valitud funktsionaalse asukohaga seotud taotluste loendit.               |
| Töötellimused                         | Avage leht **Aktiivsed töötellimused**, kus saate vaadata valitud funktsionaalse asukohaga seotud töötellimuste loendit.         |
| Tõrge                              | Avage leht **Vara tõrked**, kus saate vaadata valitud funktsionaalse asukohaga seotud tõrke registreeringute loendit. |
| Funktsionaalse asukoha värskendamine    | Valitud funktsionaalse asukoha etapi värskendamine                                                                                        |
| Elutsükli oleku logi                 | Saate vaadata logi, mis näitab valitud funktsionaalse asukoha etappe.                                                                        |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]