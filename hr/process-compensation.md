---
title: "Tasu töötlemine"
description: "Tasu töötlemise abil saate arvutada omakapitali kohanduste, teenetel põhineva palgatõusu sihtväärtuste ja tulemuste põhjal töötajate uusi põhipalga summasid."
author: kherr
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 6e30357b0bca8745b69bff19a55828b180c3b829
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017


---

# <a name="process-compensation"></a>Tasu töötlemine
Tasu töötlemise abil saate arvutada omakapitali kohanduste, teenetel põhineva palgatõusu sihtväärtuste ja tulemuste põhjal töötajate uusi põhipalga summasid. Selle ajaveebipostitus hõlmab põhipalga plaanide töötlemise peamist tasu töötlemise voogu, tulemusi arvestamata.

## <a name="plan-the-new-compensation-amounts-and-budgets"></a>Uute tasusummade ja eelarvete plaanimine
Töötajatele teenetel põhineva palgatõusu andmiseks peate seadistama igale osakonnale fikseeritud tõusu eelarve: Tasuhaldus > Lingid > Teenetel põhineva palgatõusu sihtmärgid. (Teine võimalus on avada see osakonna kaudu: Organisatsioon > Osakonnad.) Siin saate täiendavalt määrata, kas teatud ametiühingu või asukoha töötajad peaksid saama teistsuguse kasvuprotsendi. Väljad **Eelarve** ja **Valuuta** on informatiivsed ja neid saab kasutada eelarve jaoks valuutasumma märkimiseks.

## <a name="set-up-the-compensation-process"></a>Tasuprotsessi seadistamine
Protsessisündmus võimaldab määrata tasu töötlemise jaoks parameetrid. See hõlmab kuupäevaperioodi, mida tasusummade määramiseks hinnata,  ja kuupäeva, millal uued tasusummad jõustuma peaksid.

Soovi korral võite lisada põhipalga proportsionaalse töölevõtmise kuupäeva, kui mõnes põhipalgaplaanis kasutatakse protsendi palkamisreeglit. Nende plaanide puhul saab inimene, kes palgati pärast tsükli alguskuupäeva ja enne põhipalga proportsionaalset palkamise kuupäeva, 100% oma arvutatud teenetel põhinevast tasust või üldisest palgatõusust. Inimene, kes palgati pärast põhipalga proportsionaalset palkamise kuupäeva ja enne tsükli lõppkuupäeva, saab osa oma arvutatud palgatõusust selle põhjal, mitu päeva ta tsükli päevade koguarvust töötas. Näiteks kui tsükkel kestab 1. jaanuarist 31. detsembrini ja meil on põhipalga proportsionaalne palkamiskuupäev 1. aprill, saab töötaja, kes palgati märtsis, terve arvutatud palgatõusu, samas kui 1. juulil palgatud töötaja saab ligikaudu poole arvutatud palgatõusust.

Protsessisündmuse **Ajahetk** kuupäeva kasutatakse ainult teatud ergutussüsteemi plaanide töötlemiseks ja neid see ajaveebipostitus ei hõlma. **Ülevaatamise tähtaeg** on kõigi soovituste esitamise tähtaeg, et uued tasusummad saaks töötaja kirjesse laadida. Ülevaatamise kuupäev on ainult informatiivne.

Kui protsessisündmuse parameetrid on salvestatud, võite klõpsata nuppu **Seadistus**, et näidata, millised plaanid tuleks sellesse protsessitsüklisse lisada ja milliseid põhipalga toiminguid iga plaani puhul teha.

Klõpsake ülemisel vahekaardil nuppu **Lisa** tasuplaani lisamiseks protsessisündmusele. Veergusid **Kasuta muud finantsvõimendust**, **Finantsvõimenduse tegur** ja **Finantsvõimenduse kirjeldus** kasutatakse ainult ergutussüsteemi plaanide jaoks ja neid selles teemas ei käsitleta.

Salvestage kirje ja klõpsake siis alumisel vahekaardil nuppu **Lisa** põhipalga toimingute lisamiseks valitud plaani puhul. Kasutage valikut Luba soovitus, kui soovite, et saaksite sisestada muu summa peale tegevuse arvutatud kasvusumma. Kui soovite, et tegevus arvutataks eelmise tegevuse tulemuse põhjal, et siduda mitu tasutegevust, siis märkige valik Kasuta eelmist tulemust. Põhipalga tegevused on tasuloogika tegevused, millele saate anda kirjeldavad nimed. Taseme ja palgaastmiku plaanide puhul saate lisada ainult järgmist tüüpi tasutegevusi.

| Põhipalga tegevuse tüüp | Funktsioon                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Omakapital                        | Omakapitali tegevused võrdlevad töötaja palgamäära tsükli lõpu seisuga madalaima võrdluspunktiga töötaja ametikohal näidatud taseme puhul. Kui töötaja palgamäär on minimaalsest võrdluspunktist madalam, arvutatakse vajalik kasv töötaja viimiseks vahemiku miinimumpunkti.                                                                                |
| teene                         | Teenetel põhinevad tegevused arvutavad kasvu töötaja palgamäära põhjal tsükli lõppkuupäeva seisuga ja töötaja osakonna, ametiühingu ning asukoha fikseeritud palgatõusu eelarves antud kasvuprotsendi alusel.                                                                                                                                                                                         |
| Üldine                       | Üldised toimingud arvutavad palgatõusu protsendi põhjal või annavad töötajatele fikseeritud summa. See määratakse vahekaardil Üldine olevate põhipalga sätete alusel.                                                                                                                                                                                                                        |
| Edutamine                     | Edutamistegevused annavad nimelise koha, kus saate palgatõusu anda, seega märkige kindlasti valik **Luba soovitus**, et saaksite lisada edutatavate töötajate soovitusi.  Ilma soovitatud palgatõusuta töötajate põhipalga kirjetesse ei lisata edutamise tegevust.                                                                       |
| Mõni teine taseme muutus            | Eelnevas näites on meie tegevusel Põhipalga tegevus tüübiga Muu taseme muutmine nimi Ametialandus. See loob 0 (nullmuutusega) juurdekasvu, et saaksite sisestada soovitusliku summa töötaja palgamäära korrigeerimiseks. (Märkige kindlasti valik **Luba soovitus**.) Ilma soovituseta töötajate puhul ei lisata seda tegevust nende põhipalga kirjetele. |

Astmeplaani saab lisada ainult neid põhipalga tegevusi, mille tüüp on Aste.

| Põhipalga tegevuse tüüp | Funktsioon                                                                                                                                                                                           |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Etapp                           | Märkige vahekaardil Üldine, kas see astmetegevus peaks viima töötajad edasi 0 astme, 1 astme või kahe astme võrra.                                                                                  |
|                                | **0 astet** – töötaja saab selle astme palgamäära, millel ta praeg on.                                                                                                                      |
|                                | **1 aste** – süsteem kontrollib, kas töötaja on juba oma taseme viimases võrdluspunktis.                                                                                             |
|                                | **2 astet** – süsteem viib töötaja praegusel tasemel kaks astet edasi. Süsteem võib liigutada töötajat ühe või nulli astme võrra, kui töötaja on jõudnud oma taseme viimasesse võrdluspunkti. |

## <a name="run-the-compensation-process"></a>Tasuprotsessi käitamine
Pärast protsessisündmuse seadistamist vajalike kuupäevaväljade, plaanide ja tegevustega võite klõpsata sündmuse töötlemise lehel valikut **Käivita protsess**. Selle tagajärjel avaneb dialoog Käivita tasu protsessisündmused. Selles dialoogis võite klõpsata valikut **Töötlemise tulemuste näitamine**, et näha, kuidas iga töötaja puhul tasusummad arvutati. Nupu **OK** klõpsamisel käivitatakse tasuprotsess kõigi töötajate kohta, kes on tsükli lõppkuupäeva seisuga valitud tasuplaanides.

## <a name="view-the-process-results"></a>Protsessi tulemuste kuvamine
Protsessi tulemuste kuvamiseks avage leht **Protsessi tulemused**. Iga kord, kui protsessisündmus käivitatakse, luuakse uus tasusündmus. Sel viisil saate teha proovitsükleid, korrigeerida ja käivitada tasusündmuse mitu korda, et näha, kuidas mitmesugused muudatused töötaja tasu mõjutavad.

Protsessi tulemuste lehel on teave protsessi tsükli kohta, sh tsükli toimumise aeg, kasutaja, kes protsessi käivitas, ja kas protsessi käitamisel ilmnes tõrkeid. Võite märkida ka valiku **Lukustatud** nupu **Laadi tasu** keelamiseks ja vältige nii tasusündmuste laadimist töötaja kirjetesse. Nupu **Töötajate tulemused** klõpsamisel kuvatakse tsüklis sisalduvate töötajate loend.

Töötaja tulemustes kuvatakse teave protsessi enese ja samuti protsessis tehtavate tasutegevuste kohta. Põhipalga osa sisaldab kirjet iga tasuplaani protsessisündmuses sisalduva tegevuse kohta. Veergudes Praegune juhend ja Soovitus on kuvatud lisateave jaotises Põhipalk valitud tegevuse kohta. Kui tegevusel on märgitud valik Luba soovitused, siis saab soovituse välju redigeerida. See võmialdab töötaja summasid käsitsi korrigeerida. Märkus: kui märkisite protsessisündmuse puhul valiku Kasuta tegevuse puhul eelmist tulemust, peate sõltuvate tegevuste summasid käsitsi uuendama.

Kui töötaja tasusummad on üle vaadatud ja soovitud väärtused korrigeeritud, võite muuta väärtust **Olek** real **Töötaja sündmus** näitamiseks, kas sündmus on kinnitatud või seda tuleks eirata. Soovi korral võite töötaja soovituses tehtud muudatused kustutada, klõpsates nuppu **Arvuta ümber**. Sellisel juhul märgitakse olemasolev töötaja sündmus olekuga Eira ja luuakse uus ümberarvutatud väärtustega töötaja sündmus.

## <a name="loading-approved-compensation-changes"></a>Kinnitatud tasumuudatuste laadimine
Kui vähemalt ühe töötaja olek on muutunud olekuks Kinnitatud, saab need laadida töötaja põhipalga kirjetesse. Seda saab teha, valides ühekaupa kõik töötaja sündmused ja klõpsates töötaja tulemuste lehel nuppu Laadi töötaja tasu või klõpsates nuppu **Laadi tasu** protsessi tulemuste lehel kõigi kinnitatud töötaja sündmuste korraga laadimiseks.

Kui klõpsata nuppu **OK** dialoogis **Laadi tasu**, lisatakse nullist erinevad tasutegevuse read lehele **Töötaja põhipalk**.

