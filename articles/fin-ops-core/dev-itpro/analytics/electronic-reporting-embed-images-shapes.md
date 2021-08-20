---
title: Manustatud pildid ja kujutised ER-iga loodud dokumentides
description: See teema kirjeldab, kuidas kasutada elektroonilise aruandluse tööriista äridokumentide loomiseks, milles on manustatud pilte ja kujusid.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 550ecca31af48e624e292b342d909abd6eb3e87af122f736eb388524b42f1e05
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730631"
---
# <a name="embed-images-and-shapes-in-documents-that-you-generate-by-using-er"></a>Manustatud pildid ja kujutised ER-iga loodud dokumentides

[!include [banner](../includes/banner.md)]

Saate kasutada elektroonilise aruandluse (ER) tööriista aruannete kujundamiseks, mida saate käitada vajalike elektrooniliste dokumentide loomiseks. Saate kasutada Microsoft Excel või Microsoft Word dokumente aruande paigutuse määramiseks. ER-i toimingute koostaja võimaldab teil manustada aruandele mallina Exceli või Wordi dokumendi. Järgmised lisatud mallis olevad nimega elemendid on seostatud ER aruande vormingukomponendi elementidega. Aruande vorminguelemendid on seotud andmeallikatega. Need elemendid määratlevad andmed, mis sisestatakse loodud dokumentidesse käitamise ajal.

See uus funktsioon ületab vormingutes dokumentide loomise olemasolevaid ER-i Microsoft Office võimalusi. Lisateabe saamiseks mängige järgmisi ülesannete juhendeid. Need ülesannete juhendid leiate äriprotsesside 7.5.4.3 IT-teenuse/lahenduse komponentide (10677) hankimisest/arendamisest.

- Elektrooniline aruandlus OPENXML-vormingus aruannete loomiseks konfiguratsiooni koostamine
- ER kujunduse konfiguratsioon aruannete loomiseks Microsoft WORD vormingus

## <a name="embed-an-image-in-an-excel-document"></a>Manusta pilt Exceli dokumenti

### <a name="embed-an-image-in-an-excel-worksheet"></a>Manusta pilt Exceli töölehele

Kõigepealt peate Exceli dokumendis pildi jaoks kohatäitja lisama. Avage Exceli töövihik ja lisage pilt pildi kohatäitena pildile, mille hiljem lisate. Seejärel kasutage ER-i tööriista uue ER-vormingu konfiguratsiooni lisamiseks, et kaasata teie kujundatav aruanne. Manustage Exceli töövihik aruande vormingu mallina ja seejärel importige töövihiku sisu ER-vormingusse. Vormingu definitsioon luuakse automaatselt. Lisatud pildi kohatäide kaasatakse ER-vormingu definitsiooni **lahter** elemendina.

> [!NOTE]
> Vormingu definitsiooni saate importimise asemel käsitsi määrata. Kui salvestate oma muudatused, kinnitatakse vorming.

Järgmiseks siduge ER-vormingu **lahter** element väljaga vormingu andmeallikast, mis esitab käitusajal pildi andmed binaarvormingus. Kui ER-i andmemudelit kasutatakse vormingu andmeallikana, peab välja andmetüüp olema [konteiner](er-formula-supported-data-types-composite.md#container). Praegu saab ER-andmemudeli välja millel on [konteiner](er-formula-supported-data-types-composite.md#container) andmetüüp siduda mitme tüübi andmellikaga mis tagastavad kujutisi binaarvormingus. Document management framework abil pääsete juurde andmetabeli väljale ja andmetabeli kirjele lisatud failile.

> [!IMPORTANT]
> - Kui soovite täita koostavas dokumendis pildi kohatäitja Exceli malliga, peab ER-vorming sisaldama **LAHTRI** elementi, mis viitab Exceli malli nimelisele pildielemendile. Vastasel juhul ei kuvata aruande väljundis pildi kohatäiteid. Kui **LAHTER** elemendi sidumine käitusajal andmeid ei tagasta, kuvatakse loodud dokumendis mallist pildi kohatäide. Uue dokumendi pildi peitmiseks määratlege **LAHTER** element ja määrake, et **lubav** avaldis tagastaks väärtuse **VÄÄR**.
> - Exceli mallis kasutage kordumatut nime iga elemendi jaoks. Need elemendid on pildid ja lahtrid. Kui kopeerite elemendi nime, on loodud aruande sisu mitmetähenduslik ja segane.

### <a name="embed-images-in-the-header-and-footer-of-an-excel-worksheet"></a>Manusta pildid Exceli töölehe päisesse ja jalusesse

Kasutage Exceli töövihiku dokumenti mallina aruande paigutuse määramiseks. Töövihik võib sisaldada mitmeid töölehti, millest igaüks saab olla kujundatud nii, et sellel on päis ja jalus. Excel toetab iga töölehe päises ja jaluses kuni kolm pilti. Pilti saab joondada vasakule, paremale või keskele.

Finance väljalaskes 10.0.21 saate hallata päise ja jaluse pilte, mille on loonud Exceli malliga ER lahendus.

Kui soovite, et loodud dokumendi päises või jaluses kuvataks vaikepilt, saate ER-malli töölehe päisele või jalusele lisada pildi. Sellele pildile juurdepääsuks ER-vormingus peate lisama vormingu päise või jaluse komponendi alla **Pildi** komponendi [Päisesse](er-fillable-excel.md#header-component) võii [Jalusesse](er-fillable-excel.md#footer-component) vormikomponendis. Konfigureerige **Pildi** komponend joondust vastavalt vajadusele. 

Saate ka **Pildi** komponenti kasutada pildi lisamiseks loodud dokumendi päisesse või jalusesse loodud dokumendi käitusajal, isegi kui mall eisisalda vaikepilti. Meediumisisu määramiseks, mis tuleks panna loodud dokumendi päisesse või jalusesse kas uue pildina või vaikepildi asendusena, peate siduma **Pildi** komponendi andmeallikaga, mille [konteiner](er-formula-supported-data-types-composite.md#container) tüüp tähistab binaarvormingpilti.

Iga **päise** või **jaluse** komponent võib iga toetatud joonduse jaoks hoida ünhte **Pildi** komponenti joonduse jaoks: **Vasak**, **Keskel** ja **Parem**.

**Kõrguse skaala** atribuudi **Pilt** komponent võimaldab teil konfigureeritud sidumist pildi suuruse juhtimiseks:

- Valige **Originaal** algse pildi suuruse säilitamiseks.
- Valige **Suhteline** pildi kõrguse muutmiseks skaala suhtes proportsioonis seda pilti omava päise või jaluse kõrgusega.

    - Sellisel juhul peab pildi kõrgus olema määratletud emapäise või jaluse protsendina.
    - Kui skaleerimisväärtus ületab 100 protsenti, võib pilt kattuda vastava töölehe andmealaga.
    - Kui pildi kõrgust muudetakse skaleerimisel, muudetakse laiust ka pildi algse kuvasuhte säilitamiseks.

- Valige **Absoluutne**, et muuta pildi suurust vastavalt kõrguse ja laiuse väärtustele (pikslites), mis antakse kujundusaja jooksul.

    - Kui määratud kõrgus ületab emapäise või jaluse kõrguse, võib pilt kattuda vastava töölehe andmealaga.

Saate kasutada ka **Lubatud** atribuuti komponendi **Pilt** jaoks, millega saate kontrollida loodud dokumendile asetatud pildi nähtavust.

> [!NOTE]
> Peate kasutama ER-vormingu kujundajat et lisada **Pilt** komponent redigeeritavale ER-vormingule. Te ei saa komponenti lisada, kui kasutate [äridokumendi halduse](er-business-document-management.md) tööruumi äridokumendi malli redigeerimiseks.

Selle funktsiooni kohta lisateabe saamiseks järgige ER-vormingu [kujundamise samme, et luua Aruanne Exceli vormingus koos manustatud piltidega lehekülje päistes või jalustes](er-embed-images-header-footer-excel-reports.md).

## <a name="embed-a-shape-in-an-excel-document"></a>Manusta kuju Exceli dokumenti

Kõigepealt peate Exceli dokumendis kuju jaoks kohatäitja lisama. Avage Exceli töövihik ja valige **kuju**, **tekstiboks** või **WordArt** kohatäitena kuju jaoks. Seejärel kasutage ER-i tööriista uue ER-vormingu konfiguratsiooni lisamiseks, et kaasata teie kujundatav aruanne. Manustage Exceli töövihik aruande vormingu mallina ja seejärel importige töövihiku sisu ER-vormingusse. Vormingu definitsioon luuakse automaatselt. Teie lisatud kuju kohatäide kaasatakse ER-vormingu definitsiooni kui **LAHTER** element, mis viitab nimelisele Exceli kujuelemendile.

> [!NOTE]
> Vormingu definitsiooni saate importimise asemel käsitsi määrata. Kui salvestate oma muudatused, kinnitatakse vorming.

Järgmiseks siduge ER-vormingu **LAHTER** element väljaga vormingu andmeallikast, mis esitab käitusajal pildi andmed binaarvormingus. Neid andmeid saab teisendada tekstistringiks. Kui ER-vormingus **LAHTER** element viitab teksti toetavale Exceli malli kujuelemendile, näidatakse antud sidumist käitusajal antud teksti kujuna loodud dokumendis.

> [!IMPORTANT]
> - Kui soovite kasutada Exceli malli, mis sisaldab uue dokumendi loomiseks kuju kohatäitjat, peab ER-vorming sisaldama **LAHTER** elementi, mis viitab Exceli kujuelemendile. Vastasel juhul ei kuvata aruande väljundis kuju kohatäiteid. Kui nimega Exceli kujuelemendile viitava **LAHTER** elemendi sidumine ei tagasta käitusajal andmeid, kuvatakse loodud dokumendis Exceli mallist kujukohatäite tekst. Uue dokumendi kuju peitmiseks määratlege **LAHTER** element mis viitab Exceli kuju elemendile, on määratud kui **lubav** avaldis, mis tagastaks väärtuse **VÄÄR**.
> - Exceli mallis kasutage kordumatut nime iga elemendi jaoks. Need elemendid on kujud ja lahtrid. Kui kopeerite elemendi nime, on loodud aruande sisu mitmetähenduslik ja segane.

## <a name="embed-an-image-in-a-word-document"></a>Manusta pilt Wordi dokumenti
> [!IMPORTANT]
> Manustatud pilte sisaldavad dokumente saate taaskasutada et luua dokumente ER-vormingus, mis kasutab Exceli malli. Veenduge, et ER-vormingus on nimi määratud **LAHTER** elemendile, mis viitab nimelisele pildielemendile Excelis ja mis on seotud andmeallikaga, mis tagastab käitusajal pildi.

Kõigepealt peate konfigureerima Wordi dokumendi paigutuse. Kasutage **Pildi sisu** juhtelementi manustatud pildi kohatäitja loomiseks. Selle juhtelemendi pääsuks peate esmalt tegema vahekaardi **Arendaja** Word Ribbon`is nähtavaks.

Järgmisena kustutage Exceli mall ER-vormingust ja lisage Wordi mallidokument. Värskendage malli viidet ja salvestage muudatused. Praeguse ER vormingu struktuur salvestatakse Wordi mallina, uue XML-i osana, mille nimeks pannakse **Aruanne**.

Järgmiseks salvestage Wordi mall praeguse ER-vormingu jaoks kohalikku arvutisse. Avage mall ja avage **XML-i vastendamise** paan. Leidke kohandatud XML-osa nimega **Aruanne** ja seejärel osutage ER-i aruande **LAHTRI** elemendile, mis on seotud andmeallikaga, mis tagastab pildi binaarvormingus. Vastendage selle XML-i osa üksus valitud **Pildi sisu** juhtelemendiga ja salvestage oma muudatused.

[![manustage pildid.](./media/embed-images-shapes-01.png)](./media/embed-images-shapes-01.png)

Lõpuks kustutage Wordi mall ER-vormingust ja lisage Wordi dokument, mis sisaldab vastendatud kohandatud XML-i osi. Värskendage malli vorminguviidet ja salvestage sellele ER-vormingule tehtud muudatused.

## <a name="more-information"></a>Lisateave
Et tutvuda selle funktsiooni üksikasjadega, tutvuge ülesandejuhendite komplektiga **ER aruanded MS Office`i vormingutes koos manustatud piltidega**. Need ülesande juhendid näitavad, kuidas saate ettevõtte logo ja volitatud isiku allkirja kujutisi exceli ja Wordi dokumentide ER-tööriista abil loodud maksekontrollides manustada.

Järgmises tabelis loetletakse failid, mis on vajalikud **ER-i aruannete loomiseks MS Office'i vormingutes koos manustatud piltide** ülesandejuhenditega. Laadige alla ja salvestage failid kohalikku arvutisse.

| Kirjeldus                                          | Faili nimi                   |
|------------------------------------------------------|-----------------------------|
| ER-i andmemudeli konfiguratsioon                          | [Model for cheques.xml](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| Elektroonilise aruandluse vormingu konfiguratsioon                              | [Cheques printing format.xml](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| Ettevõtte logo pilt                                   | [Ettevõtte logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| Allkirja pilt                                      | [Allkirja pilt.png](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| Alternatiivne allkirjapilt                          | [Allkirja pilt 2.png](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| Microsoft Word Maksekontrollide printimise mall  | [Tšeki malli Word.docx](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |
| Microsoft Excel Maksekontrollide printimise mall | [Tšeki mall.xlsx](https://download.microsoft.com/download/1/f/6/1f671963-73aa-48d5-ae69-45f21fe7dfb4/Cheque%20template.xlsx)        |

Järgmine graafik annab näite testprintimiseks makse tšekile, mis luuakse Exceli mallist.

[![Makse kontrolltesti väljaprint.](./media/embed-images-shapes-02.png)](./media/embed-images-shapes-02.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
