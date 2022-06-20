---
title: Asukohakorralduse häälestus ostutellimuse kõrvalepaneku jaoks
description: See artikkel selgitab, kuidas seadistada lihtasukoha direktiivi.
author: Weijiesa
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d973d1cdb530a031ca8a5caf621f9bebced4842
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873488"
---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>Asukohakorralduse häälestus ostutellimuse kõrvalepaneku jaoks

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas seadistada lihtasukoha direktiivi. Toodud näites luuakse asukohakorraldus, mille abil määratletakse, kuhu panna ostutellimuse jaoks vastu võetud kaubad. Saate kasutada selles ülesandejuhendis demoettevõtte USMF andmeid. Eeltingimused: peate looma likvideerimiskoodi. Kasutame selles protseduuris likvideerimiskoodi Ümbersildistamine. Kui loote asukohakorralduse oma andmete põhjal, peate seadistama oma lao ja kaupade jaoks täiendava laohalduse. See protseduur on mõeldud laohaldurile.

1. Avage navigeerimispaanil **Moodulid > Laohaldus > Seadistus > Asukohadirektiivid**.
2. Valige väljal **Töökäsu tüüp** suvand **Ostutellimused**.

## <a name="create-a-location-directive-header"></a>Asukohakorralduse päise loomine
1. Valige suvand **Uus**.
2. Sisestage arv väljale **Järjekorranumber**. See on asukohakorralduse töötlemise järjestus valitud töötüübi puhul. Vajaduse korral saate järjestust ka muuta.  
3. Sisestage väärtus väljale **Nimi**. See on selle korralduse ainuidentifikaator.  
4. Väljal **Töö tüüp** valige **Paigal**. Valige tehtava töö tüüp. Töökäsu tüübi ostutellimusega direktiivi korral on **Paigal** ainuke toetatud väärtus.  
5. Sisestage väärtus väljale **Sait**.
6. Sisestage väärtus väljale **Ladu**. Jätke väli Korraldusekood tühjaks.  Korraldusekoode kasutatakse töötellimuse rea, mille tüüp on Pane, linkimiseks kindla korraldusega. Ostutellimuste puhul lahendatakse viimase töötellimuse rea, mille tüüp on Pane, asukoht enne töömalli määratlemist. Seetõttu ei saa töömalli viimast rida ühendada kindla korraldusega.   
7. Sisestage väärtus väljale **Likvideerimiskood**. Likvideerimiskood piirab asukohakorralduse kasutamist, nii et asukohakorraldust kasutatakse ainult siis, kui laotöötaja sisestab selle kindla väärtuse mobiilse seadme abil kauba registreerimisel.  
8. Valige käsk **Salvesta**.

## <a name="edit-the-query-for-directive"></a>Korralduse päringu redigeerimine
1. Valige **Päringu redigeerimine**. Selle korralduse kasutamine on juba piiratud teie määratud laos registreeritud kaupade ja teie määratud likvideerimiskoodiga. Saate päringu abil lisada ka muid piiranguid.  
2. Valige nupp **OK**.

## <a name="add-directive-lines"></a>Korralduseridade lisamine
1. Valige suvand **Uus**. See on asukohakorralduse ridade töötlemise järjestus valitud töötüübi puhul. Vajaduse korral saate järjestust ka muuta.  
2. Sisestage arv väljale **Alates kogusest**. See on väikseim kogus, mille puhul see korralduserida kehtib.  
3. Sisestage arv väljale **Kuni koguseni**.
4. Sisestage väärtus väljale **Ühik**. Väljade Alates kogusest ja Kuni koguseni väärtuse ühik. Kui jätate selle välja tühjaks, kasutatakse kauba varudeühikut.  
5. Valige suvand väljal **Asukoha kogus**.
    - Puudub või litsentsiplaadi kogus: igale litsentsiplaadile registreeritud kogus.  
    - Ühikuna määratud kogus: kogu registreeritud kogus.  
    - Järelejäänud kogus: ostutellimuse realt veel registreeritav kogus.  
    - Oodatav kogus: kogu ostutellimuse real määratud kogus.  
6. Valige või tühistage valik märkeruudus **Piira ühiku järgi**. Kui valite selle suvandi ja määrate üksuse lehel **Piira ühiku järgi**, saab asukohta panna ainult selle mõõtühikuga üksuseid. Näiteks kui mõõtühikuks on kaubaalused, saab määratud asukohta maha panna ainult kaubaalustel kaupu.  
7. Valige või tühistage valik märkeruudus **Luba poolitamine**. See võimaldab korraldusel jaotada koguse mitme asukoha vahel.  
8. Valige käsk **Salvesta**.

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>Korralduserea piiramine kindla ühikuga
1. Valige **Piira ühiku järgi**. See nupp on saadaval ainult siis, kui vajutate nuppu **Salvesta** pärast märkeruudu **Piira ühiku järgi** valimist.  
2. Sisestage väärtus väljale **Ühik**.
3. Sulgege leht.

## <a name="add-a-location-directive-action-line"></a>Asukohakorralduse tegevuserea lisamine
1. Valige suvand **Uus**. See on asukohakorralduse tegevuseridade töötlemise järjestus valitud töötüübi puhul. Vajaduse korral saate järjestust ka muuta.  
2. Sisestage väärtus väljale **Nimi**. See on selle korraldustegevuse ainuidentifikaator.  
3. Valige suvand väljal **Fikseeritud asukoha kasutamine**.
    - Fikseeritud ja fikseerimata asukohad: kehtivad kõik fikseerimata asukohad ja ka toote oma fikseeritud asukoht päringus määratud vahemikus.  
    - Ainult toote fikseeritud asukoht: kehtivad toote fikseeritud asukohad ja kõik tootevariandid kasutavad sama fikseeritud asukohtade kogumit.  
    - Ainult tootevariantide fikseeritud asukoht: kehtivad ainult igale tootevariandile määratud fikseeritud asukohad.  
4. Valige sobiv variant väljal **Strateegia**. Ostutellimus tüübiga töökäsud toetavad järgmisi strateegiaid. 
    - Puudub: üksus asetatakse esimesse leitud asukohta.  
    - Konsolideeri: kaup pannakse asukohta, kus on sarnased kaubad juba olemas.  
    - Tühi asukoht sissetuleva tööta: kaup pannakse esimesse leitud tühja asukohta. Asukohta käsitletakse tühjana, kui sellel ei ole füüsilist laoseisu ja eeldatavat sissetulevat tööd.  
5. Valige käsk **Salvesta**.

## <a name="edit-the-query-for-directive-action-line"></a>Korralduse tegevuserea päringu redigeerimine
1. Valige **Päringu redigeerimine**.
2. Valige **Lisa**.
3. Väljale **Väli** sisestage `location profile ID`. Selles näites piirame võimalikke asukohti asukohaprofiili ID abil.  
4. Sisestage väärtus väljale **Kriteerium**.
5. Valige nupp **OK**. Saate jätkata korralduseridade ja korraldusetegevuste lisamist, kuni olete katnud kõik oma lao võimalikud stsenaariumid.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]