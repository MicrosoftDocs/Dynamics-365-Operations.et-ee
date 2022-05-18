---
title: Finantsdimensioonid
description: Selles teemas kirjeldatakse mitmesuguseid finantsdimensioonide tüüpe ja nende seadistamist.
author: aprilolson
ms.date: 03/07/2022
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 1360139a06909c1df922570f6e577d1d310b1c48
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722320"
---
# <a name="financial-dimensions"></a>Finantsdimensioonid

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse mitmesuguseid finantsdimensioonide tüüpe ja nende seadistamist.

Kasutage lehte **Finantsdimensioonid**, et luua finantsdimensioonid, mida saab kasutada kontosegmentidena kontoplaanide puhul. Finantsdimensioone on kaht tüüpi: kohandatud dimensioonid ja üksuse tagatud dimensioonid. Kohandatud dimensioone kasutavad juriidilised isikud ühiselt ning väärtusi sisestavad ja haldavad kasutajad. Üksuse tagatud dimensioonide puhul määratletakse väärtused mujal süsteemis, nt üksustes Kliendid või Kauplused. Mõnda üksuse tagatud dimensiooni kasutavad juriidilised isikud ühiselt, samas kui mõni on ettevõttekohane.

Kui olete finantsdimensioonid loonud, kasutage igale finantsdimensioonile täiendavate atribuutide lisamiseks lehte **Finantsdimensiooni väärtused**.

Finantsdimensioone saab kasutada juriidiliste isikute kajastamiseks. Te ei pea dynamics 365 Finances juriidilisi isikuid looma. Finantsdimensioonid pole aga mõeldud juriidiliste isikute tegevus- või ärivajaduste rahuldamiseks. Rakenduse Rahandus sisekäibe funktsioon on mõeldud käsitlema ainult iga kandega loodud raamatupidamiskirjeid.

 Finantsdimensioonide juriidilised isikud häälestamiseks hinnata äriprotsessist järgmistes määratlemiseks, kui teie organisatsioon töö see seadistus:

- Varud
- Müügi ja ostu finantsdimensioonide ja juriidilised isikud
- Käibemaksuaruandluse koodi genereerimine
- Tegevuse aruandlus

Siin on mõned neist piirangutest.

- Ainult juriidiliste isikutega, finantsdimensioonide, saate käibemaksu funktsiooni.
- Mõned aruanded ei sisalda finantsdimensioone. Seega võib finantsdimensioonide alusel aruande koostamiseks olla vaja aruandeid muuta.

## <a name="custom-dimensions"></a>Kohandatud dimensioonid

Kasutaja määratletud finantsdimensiooni loomiseks valige väljal **Kasuta väärtusi allikast** suvand **Kohandatud dimensioon**.

Samuti saate määrata kontomaski, et piirata dimensiooniväärtuste puhul sisestatava teabe hulka ja tüüpi. Saate sisestada märke, mis jäävad samaks igale dimensiooniväärtusele, näiteks tähti või sidekriipsu (-). Saate sisestada ka trelle (\#) ning ja-märke (&) kohatäidetena tähemärkide jaoks, mis muutuvad iga kord, kui luuakse dimensiooniväärtus. Kasutage numbrimärki (\#) kohatäitena numbrile ning ja-märki (&) kohatäitena tähele. Vormingumaski väli on saadaval ainult siis kui valite väljal **Kasuta välja väärtusi** suvandi **Kohandatud dimensioon**.

**Näide**

Dimensiooniväärtuse piiramiseks tähtede CC ja kolme arvuga saate vormingumaskina sisestada **CC-\#\#\#**.

## <a name="entity-backed-dimensions"></a>Üksuse tagatud dimensioonid

Üksuse tagatud finantsdimensiooni loomiseks valige väljalt **Kasuta väärtusi** allikast süsteemi määratletud üksus, millele finantsdimensioon tugineb. Finantsdimensiooni väärtused luuakse siis sellest üksusest. Näiteks projektide dimensiooniväärtuste loomiseks valige **Projektid**. Siis luuakse igale projektinimele dimensiooniväärtus. Lehel **Finantsdimensiooni väärtused** on näha üksuse väärtused. Kui need väärtused on ettevõttepõhised, kuvatakse lehel ka ettevõte.

## <a name="activating-dimensions"></a>Dimensioonide aktiveerimine

Finantsdimensiooni aktiveerimisel uuendatakse tabelit, nii et see sisaldab finantsdimensiooni nime. Kustutatud dimensioonid eemaldatakse. Võite sisestada dimensiooniväärtused enne finantsdimensiooni aktiveerimist. Kuid finantsdimensiooni ei saa enne aktiveerimist tarbida. Näiteks ei saa te lisada finantsdimensiooni kontostruktuurile, enne kui finantsdimensioon on aktiveeritud. Kui valite käsu **Aktiveeri**, siis värskendatakse kõiki dimensioone ja kuvatakse nende oleku muutused.

## <a name="translations"></a>Tõlked

Lehele **Teksti tõlge** võite sisestada valitud finantsdimensiooni teksti mitmesugustes keeltes. Lehele **Põhikonto** võite sisestada põhikonto teksti mitmesugustes keeltes. 

## <a name="legal-entity-overrides"></a>Juriidilise isiku alistamised

Kõik dimensioonid ei sobi kõigile juriidilistele isikutele. Lisaks võivad mõningad dimensioonid olla asjakohased ainult konkreetse perioodi jooksul. Sel juhul saab kasutada jaotist **Juriidilise isiku tühistamised** tuvastamiseks, milliste ettevõtete dimensioon tuleks peatada, kes on omanik ja mis ajaperioodil on dimensioon aktiivne.

## <a name="deleting-financial-dimensions"></a>Finantsdimensioonide kustutamine

Andmete viiteterviklikkuse säilitamiseks saab finantsdimensioone harva kustutada. Kui püüate finantsdimensiooni kustutada, hinnatakse järgmisi kriteeriume.

- Kas finantsdimensiooni on kasutatud mõnes sisestatud või sisestamata kandes või mõnes dimensiooniväärtuste kombinatsiooni tüübis?
- Kas finantsdimensiooni on kasutatud mõnes aktiivses kontostruktuuris, täpsema reegli struktuuris või finantsdimensioonide kogumis?
- Kas finantsdimensioon kuulub mõnesse finantsdimensiooni integreerimise vaikevormingusse?
- Kas finantsdimensioon on seadistatud vaikedimensiooniks?
- Kas finantsdimensioon on finantsaruandluse seadistusest valimata? 

Kui mõni neist kriteeriumidest on täidetud, ei saa finantsdimensiooni kustutada.

> [!NOTE]
> Alates finantsversioonist 10.0.27 ei valita finantsdimensioone enam automaatselt finantsaruandluse seadistamiseks nende loomisel. 

## <a name="default-dimension-values"></a>Vaikedimensiooni väärtused

Uutes dimensioonides saate kasutada vaikeväärtustena väärtusi põhikirjetest, nt klient ja hankija. Uute dimensioonide loomisel sisestatakse põhikirje ID nende põhikirjete dimensiooniväärtustesse. Näiteks uue kliendi sisestamisel sisestatakse kliendi dimensiooni kliendi ID. Müügitellimuste, arvete või muude dokumentide, mis nõuavad kliendi ID-d, loomisel kasutatakse olemasolevaid vaikeväärtuste reegleid ja dokumendile lisatakse kliendi ID.

Seda funktsiooni juhib dimensioonis olev säte. Selle sätte nimi on **Kopeeri väärtused sellesse dimensiooni igal uuel loodaval üksusel DimensionName**, kus **DimensionName** on dimensiooni nimi. Vaikimisi on see funktsioon välja lülitatud. Saate selle siiski igal ajal sisse lülitada.

Kui dimensiooni kohta on kirje juba olemas, värskendatakse selle funktsiooni sisselülitamisel põhikirjeid. Olemasolevaid dokumente ja kandeid siiski ei värskendata.

Malli kasutamisel koondkirje loomiseks veenduge, et koonddimensiooni vaikeväärtus oleks tühi. Näiteks kui loote kliente malli põhjal, veenduge, et kliendi dimensioon mallis on tühi. Kliendi dimensiooni väärtus tuuakse vaikimisi uue kliendi koodist uue kliendi loomisel.  

## <a name="derived-dimensions"></a>Tuletatud dimensioonid

Saate konfigureerida dimensiooni nii, et teiste dimensioonide teave sisestatakse automaatselt, kui sisestate dokumenti selle dimensiooni. Näiteks kui sisestate kulukeskuse 10, saab osakonna dimensiooni sisestada automaatselt väärtuse **20**.

Tuletatud väärtused saate seadistada dimensioonide lehel.

1. Valige dimensioon ja seejärel suvand **Tuletatud dimensioonid**.

    Lehel **Tuletatud dimensioonid** on ruudustik. Valitud dimensiooni segment on ruudustiku esimene veerg.

2. Lisage segmendid, mis tuleb tuletada. Iga segment kuvatakse veeruna.

Sisestage dimensioonide kombinatsioonid, mis tuleb esimeses veerus olevast dimensioonist tuletada. Näiteks kui soovite kasutada kulukeskust dimensioonina, millest tuletatakse osakond ja asukoht, sisestage kulukeskus 10, osakond 20 ja asukoht 30. Seejärel, kui sisestate põhikirjesse või kandelehele kulukeskuse 10, sisestatakse vaikimisi osakond 20 ja asukoht 30.

### <a name="overriding-existing-values-with-derived-dimensions"></a>Olmeasolevate väärtuste asendamine tuletatud dimensioonidega
 
Tuletatud dimensiooni protsess ei tühista vaikimisi tuletatud dimensioonide olemasolevaid väärtusi. Näiteks kui sisestate kulukeskuse 10 ja ühtki muud dimensiooni pole sisestatud, sisestatakse vaikimisi osakond 20 ja asukoht 30. Kulukeskuse muutmisel aga juba määratud väärtusi ei muudeta. Seetõttu saate luua põhikirjetele vaikedimensioonid, midia tuletatud dimensioonid ei muuda.

Saate määrata tuletatud dimensioonid olemasolevaid väärtusi asendama, märkides **Asendada olemasolevad dimensiooniväärtused tuletatud väärtustega** märkeruudu **Tuletatud dimensioonide** lehel. Kui see väi on valitud, saate sisestada tuletatud dimensiooni väärtustega dimensiooni ja tuletatud dimensiooni väärtused asendavad mis tahes juba olemasolevad väärtused. Eelmist näidet kasutades, kui sisestate kulukeskuse 10 ja ühtki muud dimensiooni pole sisestatud, sisestatakse vaikimisi osakond 20 ja asukoht 30. Kui aga väärtused olid juba osakond 50 ja asukoht 60, muudetakse nüüd väärtused osakond 20 ja asukoht 30.
 
Selle sätte tuletatud dimensioonid ei asenda automaatselt olemasolevaid dimensioonide vaikeväärtuseid, kui dimensiooni väärtused on vaikeväärtused. Dimensiooni väärtused asendatakse vaid siis, kui sisestate lehele dimensiooniväärtused ja lehel on juba olemas selle dimensiooni tuletatud väärtused.

### <a name="preventing-changes-with-derived-dimensions"></a>Tuletatud dimensioonide muutmise vältimine
 
Kui kasutate tuletatud dimensiooni lisamiseks **Tuletatud dimensioonide lehel** olevat valikut **Lisa segment**, pakutakse **Lisa segment** lehe allosas suvandit, mis võimaldab teil vältida selle dimensiooni muutmist, kui see on lehele tuletatud. Vaikeseade on välja lülitatud, et see ei takistaks tuletatud dimensiooniväärtuste muutmist. Muutke seadistus olekule **Jah**, kui soovite vältida dimensiooni muutmist pärast selle tuletamist. Näiteks kui osakonna dimensiooni väärtus tuletatakse kulukeskuse dimensiooni väärtusest, ei saa osakonna väärtust muuta, kui seade **Muutmise vältimine** väärtus on **Jah**. 
 
Säte ei takista muudatusi, kui dimensiooniväärtus on õige, kuid seda ei ole tuletatud dimensioonide loendis. Kui näiteks osakond 20 tuletatakse kulukeskusest 10 ja te sisestate kulukeskus 10, ei saa tee muuda osakonda 20. Kui aga sisestate kulukeskus 20 ja see ei ole kulukeskuse tuletatud dimensioonide loendis, saate osakonna väärtust muuta. 
 
Igal juhul kontrollitakse konto väärtus ja kõikide dimensioonide väärtused konto struktuuri suhtes pärast seda, kui tuletatud dimensiooni väärtused on rakendatud. Kui kasutate tuletatud dimensioone ja nende valideerimine lehel kasutamisel nurjub, tuleb tuletatud dimensioonide väärtused tuletatud dimensioonide lehel ära muuta, et saaksite neid kannetes kasutada. 
 
Kui muudate dimensioone **Finantsdimensioonide** kiirkaardil, ei saa muuta dimensiooni, millele on määratud muutuste takistamine. Kui sisestate konto ja dimensioonid segmenditud kirje juhtelementi, on dimensioonid muudetavad. Kui aga nihutate esiletõstu segmenditud kirje juhtelemendilt teisele väljale või teete mõne tegevuse, kontrollitakse konto ja dimensioonid tuletatud dimensioonide loendi ja konto struktuuride suhtes, kinnitamaks, et olete sisestanud sobivad väärtused. 

### <a name="derived-dimensions-and-entities"></a>Tuletatud dimensioonid ja üksused

Üksuste abil saate seadistada tuletatud dimensioonide segmendid ja väärtused.

- Tuletatud dimensioonide üksus seadistab juhtdimensioonid ja nende dimensioonide puhul kasutatavad segmendid.
- Tuletatud dimensioonide väärtuste üksus võimaldab teil importida väärtused, mis tuleb iga juhtdimensiooni puhul tuletada.

Kui kasutate andmete importimiseks mõnd üksust ja see üksus impordib dimensioonid, rakendatakse importimisel tuletatud dimensioonireegleid, kui üksus neid dimensioone spetsiaalselt ei tühista.

Lisateavet vt järgmistest teemadest:

- [Finantsdimensioonide määratlemine](tasks/define-financial-dimensions.md)
- [Finantsdimensiooni vaikemallide haldamine](tasks/maintain-financial-dimension-default-templates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
