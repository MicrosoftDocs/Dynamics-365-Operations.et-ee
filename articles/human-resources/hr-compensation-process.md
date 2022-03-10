---
title: Tasu töötlemine
description: Tasu töötlemise abil saate arvutada omakapitali kohanduste, teenetel põhineva palgatõusu sihtväärtuste ja tulemuste põhjal töötajate uusi põhipalga summasid.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 7c72f866886f320d8a7fa22d6ccfa7e43284b5bf
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071716"
---
# <a name="process-compensation"></a>Tasu töötlemine


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tasu töötlemise abil saate arvutada omakapitali kohanduste, teenetel põhineva palgatõusu sihtväärtuste ja tulemuste põhjal töötajate uusi põhipalga summasid. See teema käsitleb tasude töötlemise põhivoogu põhipalga plaanide puhul ilma töötaja tulemusi arvesse võtmata.

## <a name="plan-the-new-compensation-amounts-and-budgets"></a>Uute tasusummade ja eelarvete plaanimine
Töötajatele teenetel põhineva palgatõusu andmiseks peate seadistama igale osakonnale fikseeritud tõusu eelarve: **Tasuhaldus** > **Lingid** > **Teenetel põhineva palgatõusu sihtmärgid**. (Teine võimalus on avada see leht osakonna kaudu: **Organisatsioon** > **Osakonnad**.) Siin saate täiendavalt määrata, kas teatud ametiühingu või asukoha töötajad peaksid saama teistsuguse kasvuprotsendi. Väljad **Eelarve** ja **Valuuta** on informatiivsed ja neid saab kasutada eelarve jaoks valuutasumma märkimiseks.

## <a name="set-up-the-compensation-process"></a>Tasuprotsessi seadistamine
**Kompensatsiooni protsesside** lehel saate määrata kompensatsiooni töötlemise parameetrid. See hõlmab kuupäevaperioodi hüvitussummade kindlaksmääramiseks ja kuupäeva, millest uued hüvitussummad peavad jõustuma.

Soovi korral võite lisada **Põhipalga proportsionaalse töölevõtmise kuupäeva**, kui mõnes põhipalgaplaanis kasutatakse protsendi palkamisreeglit. Nende plaanide puhul saab inimene, kes palgati pärast **Tsükli alguskuupäeva** ja enne **Põhipalga proportsionaalset palkamise kuupäeva**, 100% oma arvutatud teenetel põhinevast tasust või üldisest palgatõusust. Inimene, kes palgati pärast **Põhipalga proportsionaalset palkamise kuupäeva** ja enne **Tsükli lõppkuupäeva**, saab osa oma arvutatud palgatõusust selle põhjal, mitu päeva ta tsükli päevade koguarvust töötas. Näiteks kui tsükkel kestab 1. jaanuarist 31. detsembrini ja põhipalga proportsionaalne palkamiskuupäev on 1. aprill, saab töötaja, kes palgati märtsis, terve arvutatud palgatõusu, samas kui 1. juulil palgatud töötaja saab ligikaudu poole arvutatud palgatõusust.

Protsessisündmuse **Ajahetk** kuupäeva kasutatakse ainult teatud ergutussüsteemi plaanide töötlemiseks ja neid siin ei käsitleta. **Ülevaatamise tähtaeg** on kõigi soovituste esitamise tähtaeg, et uued tasusummad saaks töötaja kirjesse laadida. Ülevaatamise kuupäev on ainult informatiivne.

Kui protsessisündmuse parameetrid on salvestatud, võite klõpsata nuppu **Seadistus**, et valida, millised plaanid tuleks sellesse protsessitsüklisse lisada ja milliseid põhipalga toiminguid iga plaani puhul teha.

Klõpsake vahekaardil **Plaanid** nuppu **Lisa** tasuplaani lisamiseks protsessisündmusele. Veergusid **Kasuta muud finantsvõimendust**, **Finantsvõimenduse tegur** ja **Finantsvõimenduse kirjeldus** kasutatakse ainult ergutussüsteemi plaanide jaoks ja neid selles teemas ei käsitleta.

Salvestage kirje ja klõpsake siis vahekaardil **Tegevused** nuppu **Lisa** põhipalga toimingute lisamiseks valitud plaani puhul. Kasutage valikut **Luba soovitus**, et sisestada muu summa peale tegevuse jaoks arvutatud kasvusumma. Kui soovite arvutada eelmise tegevuse tulemusel põhineva tegevuse mitme hüvitustegevuse linkimiseks, märkige valik **Kasuta eelmist tulemuse** varianti. Põhitasu tegevused on kompensatsiooniloogika tüübid, millele saate anda kirjeldavaid nimed. Sest **Hinne** ja **Bänd** plaanid, saate lisada ainult järgmist tüüpi fikseeritud hüvitistoiminguid:

| Põhipalga tegevuse tüüp | Funktsioon                  |
|-------------------------------|-------------------------------------------------------------------------|
| Omakapital                        | Omakapitali tegevused võrdlevad töötaja palgamäära tsükli lõpu seisuga madalaima võrdluspunktiga töötaja ametikohal näidatud taseme puhul. Kui töötaja palgamäär on minimaalsest võrdluspunktist madalam, arvutatakse vajalik kasv töötaja viimiseks vahemiku miinimumpunkti.                                                                                |
| teene                         | Teenetel põhinevad tegevused arvutavad kasvu töötaja palgamäära põhjal tsükli lõppkuupäeva seisuga ja töötaja osakonna, ametiühingu ning asukoha fikseeritud palgatõusu eelarves antud kasvuprotsendi alusel.                                                                                                                                                                                         |
| Üldine                       | Üldised toimingud arvutavad palgatõusu protsendi põhjal või annavad töötajatele fikseeritud summa. See määratakse vahekaardil **Üldine** olevate suvandi **Põhipalk** sätete alusel.                                                                                                                                                                                                                        |
| Edutamine                     | Kampaaniategevused annavad teile nimelise koha, kus saate preemiatõusu. Märkige valik **Luba soovitamine**, et sisestada soovitus töötajatele, kes saavad kampaaniaid.  Ilma soovitatud palgatõusuta töötajate põhipalga kirjetesse ei lisata tegevust **Edutamine**.                                                                       |
| Mõni teine taseme muutus            | Eelnevas näites on tegevusel **Põhipalk** tüübiga **Muu taseme muutus** nimi **Ametialandus**. See loob 0 (nullmuutusega) juurdekasvu, et saaksite sisestada soovitusliku summa töötaja palgamäära korrigeerimiseks. (Valige **Luba soovitus**.) Ilma soovituseta töötajate puhul ei lisata seda tegevust nende põhipalga kirjetele. |

Astmeplaani saab lisada ainult neid tegevusi **Põhipalk**, mille tüüp on Aste.

| Põhipalga tegevuse tüüp | Funktsioon                |
|--------------------------------|------------------------------|
| Etapp                           | Märkige vahekaardil **Üldine**, kas see astmetegevus peaks viima töötajad edasi 0 astme, 1 astme või kahe astme võrra.                                                                                  |
|                                | **0 astet** – töötaja saab selle astme palgamäära, millel ta praeg on.                                                                                                                      |
|                                | **1 aste** – süsteem kontrollib, kas töötaja on juba oma taseme viimases võrdluspunktis.                                                                                             |
|                                | **2 sammu** - Töötaja liigub praegusel tasemel kaks sammu edasi. Töötaja võib liikuda ainult ühe või null sammu, kui ta jõuab oma taseme viimase võrdluspunktini. |

## <a name="run-the-compensation-process"></a>Tasuprotsessi käitamine
Pärast protsessisündmuse seadistamist vajalike kuupäevaväljade, plaanide ja tegevustega klõpsake lehel **Protsessisündmus** valikut **Käivita protsess**, see avab **Käivitage kompensatsiooniprotsessi sündmused** dialoogi. Klõpsake valikul **Töötlemise tulemuste näitamine**, et näha, kuidas iga töötaja puhul tasusummad arvutati. Nupu **OK** klõpsamisel käivitatakse tasuprotsess kõigi töötajate kohta, kes on tsükli lõppkuupäeva seisuga valitud tasuplaanides.

## <a name="view-the-process-results"></a>Protsessi tulemuste kuvamine
Protsessi tulemuste kuvamiseks avage leht **Protsessi tulemused**. Iga kord, kui protsessisündmus käivitatakse, luuakse uus tasusündmus. See lubab teha proovitsükleid, korrigeerida ja käivitada tasusündmuse mitu korda, et näha, kuidas mitmesugused muudatused töötaja tasu mõjutavad.

Lehel **Protsessi tulemused** on teave protsessi tsükli kohta, sh tsükli toimumise aeg, kasutaja, kes protsessi käivitas, ja kas protsessi käitamisel ilmnes tõrkeid. Võite märkida ka valiku **Lukustatud** nupu **Laadi tasu** keelamiseks ja vältida nii tasusündmuste laadimist töötaja kirjetesse. Nupu **Töötajate tulemused** klõpsamisel kuvatakse tsüklis sisalduvate töötajate loend.

Suvandis **Töötaja tulemused** on näidatud teave protsessi enda kohta, samuti kõik protsessis tehtud tasutegevused. Jaotis **Põhipalk** sisaldab kirjet iga tegevuse kohta, mis on tasuplaani protsessisündmusse kaasatud. Veergudes **Praegune juhend** ja **Soovitus** on kuvatud lisateave jaotises **Põhipalk** valitud tegevuse kohta. Kui tegevuse puhul on märgitud valik **Luba soovitused**, siis saab **Soovituste** välju redigeerida. See võmialdab töötaja summasid käsitsi korrigeerida. Pange tähele, et kui märkisite protsessisündmuses tegevuse puhul valiku **Kasuta eelmist tulemust**, peate sõltuvate tegevuste summasid käsitsi värskendama.

Kui töötaja tasusummad on üle vaadatud ja soovitud väärtused korrigeeritud, võite muuta väärtust **Olek** real **Töötaja sündmus** selleks et näidata, kas sündmus on kinnitatud või seda tuleks eirata. Soovi korral võite töötaja soovituses tehtud muudatused kustutada, klõpsates nuppu **Arvuta ümber**. Sellisel juhul märgitakse olemasolev töötaja sündmus olekuga Eira ja luuakse uus ümberarvutatud väärtustega töötaja sündmus.

## <a name="loading-approved-compensation-changes"></a>Kinnitatud tasumuudatuste laadimine
Kui vähemalt ühe töötaja olek on muutunud olekuks **Kinnitatud**, saab need laadida töötaja põhipalga kirjetesse. Seda saab teha, valides ühekaupa kõik töötaja sündmused ja klõpsates lehel **Töötaja tulemused** nuppu **Laadi töötaja tasu** või klõpsates nuppu **Laadi tasu** lehel **Protsessi tulemused** kõigi kinnitatud töötaja sündmuste korraga laadimiseks.

Kui klõpsata nuppu **OK** dialoogis **Laadi tasu**, lisatakse nullist erinevad tasutegevuse read lehele **Töötaja põhipalk**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
