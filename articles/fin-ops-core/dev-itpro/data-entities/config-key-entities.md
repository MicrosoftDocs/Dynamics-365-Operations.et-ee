---
title: Konfiguratsioonivõtmed ja andmeüksused
description: Selles teemas kirjeldatakse konfiguratsioonivõtmete ja andmeüksuste vahelist seost.
author: Sunil-Garg
ms.date: 05/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.custom: 25341
ms.assetid: 8e214c95-616b-4ee1-b5a4-fa5ce5147f2c
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: bdb90f8d629a026a84f8c65e7e95b589169a3e4d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752332"
---
# <a name="configuration-keys-and-data-entities"></a>Konfiguratsioonivõtmed ja andmeüksused

[!include [banner](../includes/banner.md)]

Enne andmete importimiseks või eksportimiseks andmeüksuste kasutamist soovitame teil määratleda konfiguratsioonivõtmete mõju andmeteüksustele, mida plaanite kasutada.

Lisateabe saamiseks konfiguratsioonivõtmete kohta lugege teemat [Litsentsikoodide ja konfiguratsioonivõtmete aruanne](../sysadmin/license-codes-configuration-keys-report.md).

### <a name="configuration-key-assignments"></a>Konfiguratsioonivõtmete määramine
Konfiguratsioonivõtmeid saab määrata ühele või kõigile järgmistele artefaktidele.

- Andmeüksused
- Andmeallikatena kasutatavad tabelid
- Tabeli väljad
- Andmeüksuse väljad

Järgmises tabelis antakse ülevaade, kuidas objektile aluseks olevate eri artefaktide konfiguratsioonivõtme väärtused muudavad objekti eeldatavat käitumist.

| Andmeüksuse konfiguratsioonivõtme säte | Tabeli konfiguratsioonivõtme säte | Tabeli välja konfiguratsioonivõtme säte | Andmeüksuse välja konfiguratsioonivõtme säte | Eeldatav käitumine |
|-----------------------------------------|------------------------------------|------------------------------------------|----------------------------------------|------------------|
| Keelatud                                | Pole hinnatud                      | Pole hinnatud                            | Pole hinnatud                          | Kui andmeüksuse konfiguratsioonivõti on keelatud, siis andmeüksus ei toimi. Pole vahet, kas aluseks olevate tabelite ja väljade konfiguratsioonivõtmed on lubatud või keelatud. |
| Lubatud                                 | Keelatud                           | Pole hinnatud                            | Pole hinnatud                          | Kui andmeüksuse konfiguratsioonivõti on lubatud, kontrollib andmehaldusraamistik iga aluseks oleva tabeli konfiguratsioonivõtit. Kui tabeli konfiguratsioonivõti on keelatud, ei saa seda tabelit andmeüksuses kasutada. Kui tabeli konfiguratsioonivõti on keelatud, ei hinnata tabeli ja andmeüksuse konfiguratsioonivõtme sätteid. Kui üksuse esmase tabeli konfiguratsioonivõti on keelatud, toimib süsteem nii, nagu üksuse konfiguratsioonivõti oleks keelatud. |
| Lubatud                                 | Lubatud                            | Keelatud                                 | Pole hinnatud                          | Kui andmeüksuse konfiguratsioonivõti ja aluseks olevate tabelite konfiguratsioonivõtmed on lubatud, kontrollib andmehaldusraamistik tabelite väljade konfiguratsioonivõtit. Kui välja konfiguratsioonivõti on keelatud, ei ole see väli andmeüksuses kasutamiseks saadaval isegi juhul, kui vastava andmeüksuse välja konfiguratsioonivõti on lubatud. |
| Lubatud                                 | Lubatud                            | Lubatud                                  | Keelatud                               | Kui konfiguratsioonivõti on lubatud kõigil muudel tasanditel, aga üksuse välja konfiguratsioonivõti ei ole lubatud, ei saa välja andmeüksuses kasutada. |

> [!NOTE]
> Kui üksusel andmeallikana teine üksus, rakendatakse ülal olevat semantikat rekursiivselt.

### <a name="entity-list-refresh"></a>Üksuste loendi värskendamine
Üksuse loendi värskendamisel loob andmehaldusraamistik konfiguratsioonivõtme metaandmed käitusajal kasutamiseks. Metaandmed luuakse ülalkirjeldatud loogikat kasutades. Soovitame enne andmehaldusraamistikus tööde ja üksuste kasutamist tungivalt oodata üksuste loendi värskendamise lõpetamiseni. Kui te ei oota, ei pruugi konfiguratsioonivõtme metaandmed olla ajakohastatud, mis võib põhjustada ootamatuid tulemusi. Üksuste loendi värskendamisel kuvatakse üksuste loendi lehel järgmine teade.

![Üksuste loendi värskendamine](./media/Entity_refresh_list.png)

### <a name="data-entity-list-page"></a>Andmeüksuste loendi leht
Andmeüksuste loendi leht tööruumis Andmehaldus näitab üksuste konfiguratsioonivõtme sätteid. Konfiguratsioonivõtmete mõju mõistmiseks andmeüksustele alustage sellelt lehelt.

See teave kuvatakse üksuse värskendamise ajal loodud metaandmete abil. Konfiguratsioonivõtme veerus kuvatakse andmeüksusega seostatud konfiguratsioonivõtme nimi. Kui see veerg on tühi, tähendab see, on andmeüksusega pole konfiguratsioonivõtit seostatud. Konfiguratsioonivõtme oleku veerus kuvatakse konfiguratsioonivõtme olek. Kui see on märgitud, tähendab see, et võti on lubatud. Kui see on tühi, tähendab see, et võti on keelatud või võtit ei ole seostatud.

![Üksuste loendi leht](./media/Data_entity_list_page.png)

### <a name="target-fields"></a>Sihtväljad
Järgmiseks sammuks andmeteüksusesse süvitsiminek konfiguratsioonivõtmete mõju vaatamiseks tabelitele ja väljadele. Andmeüksuse sihtväljade vorm näitab andmeüksuses seotud tabelite ja väljade konfiguratsioonivõtme ja võtme oleku teavet. Kui andmeüksus ise on oma konfiguratsioonivõtme keelanud, kuvatakse hoiatusteade, et selle üksuse sihtväljade vormi tabelid ja väljad ei ole sõltumata nende konfiguratsioonivõtme olekust üldse saadaval.

![Sihtväljad](./media/Target_fields_1.png)

### <a name="child-entities"></a>Tütarüksused 
Teatud üksustel on andmeallikatena teisi üksuseid või need on liit-andmeüksused; nende üksuste konfiguratsioonivõtme teave kuvatakse alamüksuse vormil. Seda vormi saate kasutada samal viisil nagu ülal kirjeldatud üksusteloendi lehte. Alamüksuse sihtväljad käituvad samuti ülal kirjeldatud viisil.

![Sihtväljad](./media/Target_fields_2.png)

### <a name="using-data-entities"></a>Andmeüksuste kasutamine
Pärast konfiguratsioonivõtmete täieliku mõju mõistmist andmeüksustele, mida soovite kasutada, saate jätkata andmeüksuste kasutamist, lisades neid andmeprojektidele. 

### <a name="run-time-validations-for-configuration-keys"></a>Konfiguratsioonivõtmete käitusaja kontrollid
Üksuste loendi värskendamise ajal loodud konfiguratsioonivõtme metaandmete kasutamisel tehakse käitusaja kontrolle järgmistel kasutusjuhtudel.

- Kui andmeüksus lisatakse tööle
- Kui kasutaja klõpsab üksuste loendil käsku Kontrolli
- Kui kasutaja laadib andmepaketi andmeprojekti
- Kui kasutaja laadib malli andmeprojekti
- Kui olemasolev andmeprojekt on laaditud
- Kui mall on laaditud andmeprojekti
- Enne ekspordi/impordi töö käivitamist (partii, mitte-partii, korduv, OData)
- Kui kasutaja loob vastendamise
- Kui kasutaja vastendab välju vastendamise kasutajaliidesel
- Kui kasutaja lisab ainult imporditavaid välju

### <a name="managing-configuration-key-changes"></a>Konfiguratsioonivõtme muudatuste haldamine
Konfiguratsioonivõtmete värskendamisel üksuse, tabeli või välja tasemel tuleb värskendada andmehaldusraamistiku üksuste loendit. See tagab, et raamistik komplekteerib konfiguratsioonivõtme uusimad sätted. Kuni üksuste loendit värskendatakse, kuvatakse üksuste loendi lehel järgmine hoiatus. Värskendatud konfiguratsioonivõtme muudatused jõustuvad kohe pärast üksuste loendi värskendamist. Soovitame olemasoleva andmeprojektid ja tööd kinnitada, veendumaks et need toimiksid pärast konfiguratsioonivõtmete muudatuste rakendamist õigesti.

![Sihtväljad](./media/Target_fields_3.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]