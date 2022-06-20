---
title: Värskenda ärapanemiseks jälgimist
description: See artikkel kirjeldab, kuidas seadistada ja käivitada ajastatud perioodilise ülesande uuenduste jälgimist.
author: Weijiesa
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: b36fe5a9828ea018881f08b8af27d77cdf0babc1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882601"
---
# <a name="update-tracking-for-put-away"></a>Värskenda ärapanemiseks jälgimist

[!include [banner](../includes/banner.md)]

*Ajastatud perioodilise ülesande värskendusejälgimine* on mõeldud käitama igatunnise korduva partiina. See näitab, millised reisid on saanud kõik laokanded ja millistel reisidel pole tegeliku lõppkuupäeva väärtust. Seejärel seadistab see tegeliku lõppkuupäeva vajaduse järgi praegusele kuupäevale.

*Konteineri tegevused* luuakse iga *saatmiskonteineri* iga töölähetuse *relgi* jaoks. Need väärtused määratleb reisi loomisel valitud reisimall. Iga konteineri tegevuste kirje puhul saab väärtusi seada väljadele **Alguskuupäev**, **Eeldatav lõppkuupäev** ja **Tegelik lõppkuupäev**. Neid välju saab uuendada, kui on saadud kinnitus, et eesliide on alustatud või lõpetatud.

Tavaliselt pakub kinnitatud kuupäevadega seotud teavet kolmas osapool, nt ekspediiter, sest neid tegevusi hallatakse väljaspool rakendust Microsoft Dynamics 365 Supply Chain Management. Kolmandalt osapoolelt saadud teave ei ole siiski vajalik nende kaupade saabumise jälgimiseks reisikiilt lattu (märgitud kaupade panemisjäljega). Seetõttu saab jälgimist määratleda rakenduse Dynamics 365 Supply Chain Management teabe põhjal.

*Ajastatud perioodilise ülesande uuenduste jälgimise* seadistamiseks ja käitamiseks järgige järgmisi samme.

1. Minge **Väljaminev kulu \>Perioodilised ülesanded \>Ajastatud värskenduse jälgimine**.
1. Seadke dialoogiaknas **Ajastatud uuenduste jälgimine** jaotises **Parameetrid** järgmised väljad:

    - **Jalg** – valige kordumatu ID-nimi/number reisi selle osa jaoks, mille jälgimist soovite uuendada. Valitud väärtus peab tähistama reisi saabumise laos.
    - **Tegevus** - valige tegevus, mis valiti valitud jala jooksul. Need väärtused määratakse jälgimiskontrollikeskuses iga reisimalli rea kohta.

1. Värskendusse kaasatavate kirjete piiramiseks valige kiirklahvil **Kaasatavad kirjed** nupp **Filtreeri**. Kuvatakse standardne päringudialoogiaken, kus saate määrata valikukriteeriumid, sortimiskriteeriumid ja ühendamised. Väljad töötavad samamoodi nagu muudel päringutüüpidel Supply Chain Management puhul. Siinsed väljad on kirjutuskaitstud ja kuvavad teie päringuga seotud väärtused.
1. Häälestage kiirkaardil **Käivita taustal** vastavalt vajadusele partii ja plaanimise valikud, nagu võite teha teiste rakenduse Supply Chain Management tüüpi töödes.
1. Valige **OK** oma sätete rakendamiseks ning uuendamise käivitamiseks või plaanimiseks.
