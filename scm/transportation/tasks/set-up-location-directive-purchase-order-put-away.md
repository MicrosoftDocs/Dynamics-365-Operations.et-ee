--- 
title: "Asukohakorralduse seadistamine ostutellimuse kõrvalepaneku jaoks"
description: "See protseduur näitab, kuidas seadistada lihtsat asukohakorraldust."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 4c2456fffd9a010728154749b35c58db13f142bb
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>Asukohakorralduse seadistamine ostutellimuse kõrvalepaneku jaoks

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas seadistada lihtsat asukohakorraldust. Toodud näites luuakse asukohakorraldus, mille abil määratletakse, kuhu panna ostutellimuse jaoks vastu võetud kaubad. Saate kasutada selles ülesandejuhendis demoettevõtte USMF andmeid. Eeltingimused: peate looma likvideerimiskoodi. Kasutame selles protseduuris likvideerimiskoodi Ümbersildistamine. Kui loote asukohakorralduse oma andmete põhjal, peate seadistama oma lao ja kaupade jaoks täiendava laohalduse.  See protseduur on mõeldud laohaldurile.

1. Avage Laohaldus > Seadistus > Asukohakorraldused.
2. Valige väljal Töötellimuse tüüp suvand Ostutellimus.

## <a name="create-a-location-directive-header"></a>Asukohakorralduse päise loomine
1. Klõpsake valikut Uus.
2. Sisestage number väljale Seerianumber.
    * See on asukohakorralduse töötlemise järjestus valitud töötüübi puhul. Vajaduse korral saate järjestust ka muuta.  
3. Sisestage väärtus väljale Nimi.
    * See on selle korralduse ainuidentifikaator.  
4. Valige väljal Töö tüüp suvand Pane.
    * Valige tehtava töö tüüp. Korralduse puhul, mille töötellimuse tüüp on Ostutellimus, on ainus toetatud väärtus Pane.  
5. Sisestage väärtus väljale Koht.
6. Sisestage väärtus väljale Ladu.
    * Jätke väli Korraldusekood tühjaks.  Korraldusekoode kasutatakse töötellimuse rea, mille tüüp on Pane, linkimiseks kindla korraldusega. Ostutellimuste puhul lahendatakse viimase töötellimuse rea, mille tüüp on Pane, asukoht enne töömalli määratlemist. Seetõttu ei saa töömalli viimast rida ühendada kindla korraldusega.   
7. Sisestage väärtus väljale Likvideerimiskood.
    * Likvideerimiskood piirab asukohakorralduse kasutamist, nii et asukohakorraldust kasutatakse ainult siis, kui laotöötaja sisestab selle kindla väärtuse mobiilse seadme abil kauba registreerimisel.  
8. Klõpsake nuppu Salvesta.

## <a name="edit-the-query-for-directive"></a>Korralduse päringu redigeerimine
1. Klõpsake suvandit Redigeeri päringut.
    * Selle korralduse kasutamine on juba piiratud teie määratud laos registreeritud kaupade ja teie määratud likvideerimiskoodiga. Saate päringu abil lisada ka muid piiranguid.  
2. Klõpsake nuppu OK.

## <a name="add-directive-lines"></a>Korralduseridade lisamine
1. Klõpsake valikut Uus.
    * See on asukohakorralduse ridade töötlemise järjestus valitud töötüübi puhul. Vajaduse korral saate järjestust ka muuta.  
2. Sisestage number väljale Alates kogusest.
    * See on väikseim kogus, mille puhul see korralduserida kehtib.  
3. Sisestage number väljale Kuni koguseni.
4. Sisestage väärtus väljale Ühik.
    * Väljade Alates kogusest ja Kuni koguseni väärtuse ühik. Kui jätate selle välja tühjaks, kasutatakse kauba varudeühikut.  
5. Valige suvand väljal Koguse asukoha leidmine.
    * Puudub või Litsentsiplaadi kogus: igale litsentsiplaadile registreeritud kogus. Ühikuna määratud kogus: kogu registreeritud kogus. Järelejäänud kogus: ostutellimuse realt veel registreeritav kogus. Oodatav kogus: kogu ostutellimuse real määratud kogus.  
6. Märkige või tühjendage ruut Piira ühiku alusel.
    * Kui valite selle suvandi ja määrate lehel Piiramine ühiku alusel soovitud ühiku, saab asukohta panna ainult selle mõõtühikuga kaubad. Näiteks kui mõõtühikuks on kaubaalused, saab määratud asukohta maha panna ainult kaubaalustel kaupu.  
7. Märkige või tühjenadge ruut Luba tükeldamine.
    * See võimaldab korraldusel jaotada koguse mitme asukoha vahel.  
8. Klõpsake nuppu Salvesta.

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>Korralduserea piiramine kindla ühikuga
1. Klõpsake suvandit Piira ühiku alusel.
    * See nupp on saadaval ainult siis, kui vajutate pärast ruudu Piira ühiku alusel valimist nuppu Salvesta.  
2. Sisestage väärtus väljale Ühik.
3. Sulgege leht.

## <a name="add-a-location-directive-action-line"></a>Asukohakorralduse tegevuserea lisamine
1. Klõpsake valikut Uus.
    * See on asukohakorralduse tegevuseridade töötlemise järjestus valitud töötüübi puhul. Vajaduse korral saate järjestust ka muuta.  
2. Sisestage väärtus väljale Nimi.
    * See on selle korraldustegevuse ainuidentifikaator.  
3. Valige suvand väljal Fikseeritud asukoha kasutus.
    * Fikseeritud ja fikseerimata asukohad: kehtivad kõik fikseerimata asukohad ja ka toote oma fikseeritud asukoht päringus määratud vahemikus.  Ainult toote fikseeritud asukoht: kehtivad toote fikseeritud asukohad ja kõik tootevariandid kasutavad sama fikseeritud asukohtade kogumit. Ainult tootevariantide fikseeritud asukoht: kehtivad ainult igale tootevariandile määratud fikseeritud asukohad.  
4. Valige suvand väljal Strateegia.
    * Töötellimused, mille tüüp on Ostutellimused, toetavad järgmisi strateegiaid. Puudub: kaup pannakse esimesse leitud asukohta. Konsolideeri: kaup pannakse asukohta, kus on sarnased kaubad juba olemas. Tühi asukoht sissetuleva tööta: kaup pannakse esimesse leitud tühja asukohta. Asukohta käsitletakse tühjana, kui sellel ei ole füüsilist laoseisu ja eeldatavat sissetulevat tööd.  
5. Klõpsake nuppu Salvesta.

## <a name="edit-the-query-for-directive-action-line"></a>Korralduse tegevuserea päringu redigeerimine
1. Klõpsake suvandit Redigeeri päringut.
2. Klõpsake vahekaarti Lisa.
3. Sisestage väljale Väli tekst „asukohaprofiili ID”.
    * Selles näites piirame võimalikke asukohti asukohaprofiili ID abil.  
4. Sisestage väärtus väljale Kriteeriumid.
5. Klõpsake nuppu OK.
    * Saate jätkata korralduseridade ja korraldusetegevuste lisamist, kuni olete katnud kõik oma lao võimalikud stsenaariumid.  


