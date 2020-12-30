---
title: Klientide krediidilimiidid
description: See artikkel annab ülevaate krediidilimiitide toimimisest rakenduses Dynamics 365 Supply Chain Management.
author: omulvad
manager: tfehr
ms.date: 09/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e98203f03f10b3a7c530cb91211df2af025710dc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426354"
---
# <a name="credit-limits-for-customers"></a>Klientide krediidilimiidid

[!include [banner](../includes/banner.md)]

Krediidilimiitide määramine võimaldab määrata klientidele antava krediidi maksimumsumma. Kui krediidilimiit on määratud, kontrollitakse seda automaatselt, kui kasutaja püüab dokumenti värskendada. Krediidilimiidi ületamisel kuvatakse kasutajale teade. See artikkel annab ülevaate sellest, kuidas krediidilimiidid toimivad, ja vastab järgmistele küsimustele.

-   Milliste dokumentide ja protsesside krediidilimiite saan kontrollida?

-   Kus saan konfigureerida seda, kuidas kliendi järelejäänud krediidisummat arvutatakse?

-   Kus on teave kliendi järelejäänud kasutatava krediidi kohta?

-   Kus saan määrata, kas kliendile krediidi andmiseks on vajalik ID ja milline krediidilimiidi summa nõuab ID-d?

-   Kus saan määrata, kas krediidilimiidi ületamisel tuleks kuvada hoiatus või tõrge?

-   Kuidas saan konkreetsele kliendile krediidilimiidi määrata?

-   Kuidas saan müügitellimuste puhul käsitsi krediidilimiite kontrollida?

**Milliste dokumentide ja protsesside krediidilimiite saan kontrollida?**

Vormi **Müügireskontro parameetrid** abil saab määrata, milliste dokumentide puhul tuleks krediidilimiiti kontrollida. Sellel vormil muudatuste tegemiseks peate olema süsteemiadministraatori (- SYSADMIN-) turberolli liige. Krediidilimiite saab kontrollida järgmiste dokumentide ja protsesside puhul.

-   Müügitellimuste arved, kui arveid sisestate

-   Müügitellimuste saatelehed, kui saatelehti värskendate

-   Müügitellimused, kui lisate ridu vormil **Müügitellimus**

-   Müügitellimused, kui neid teenuse kaudu koostatakse

-   Vabas vormis arved, kui arveid sisestate

Krediidilimiiti kontrollitakse automaatselt, kui on määratud üks järgmistest valikutest.

-   Vormil **Müügireskontro parameetrid** on väljale **Krediidilimiidi tüüp** määratud muu väärtus kui **Pole**. Krediidilimiiti kontrollitakse kõigi klientide puhul.

-   Vormil **Müügireskontro parameetrid** on välja **Krediidilimiidi tüüp** väärtuseks määratud **Pole**, kuid kliendile on valitud **Kohustuslik krediidilimiit** vormil **Kliendid**. Krediidilimiiti kontrollitakse ainult konkreetsete klientide puhul.

Krediidilimiidi kontrollimiseks järgmiste dokumentide puhul tuleb määrata lisasätted.

|    Dokument                                     |    Lisasäte                                                                                                             |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|    Vabas vormis arve                         |    Tehke vormi Müügireskontro parameetrid alal Krediidireiting valik Krediidilimiidi kontrollimine vabas vormis arvel.     |
|    Müügitellimus (käsitsi sisestatud)            |    Tehke vormi Müügireskontro parameetrid alal Krediidireiting valik Krediidilimiidi kontrollimine müügitellimusel.           |
|    Müügitellimus (elektrooniliselt vastuvõetud)     |    Tehke vormi Müügireskontro parameetrid alal AIF valik Krediidilimiidi kontrollimine müügitellimusel.                     |

**Kus saan konfigureerida seda, kuidas kliendi järelejäänud krediidisummat arvutatakse?**

Saate konfigureerida Dynamics 365 arvutama kliendi järelejäänud krediidisummat ühel järgmistest viisidest.

-   Krediidilimiiti võrreldakse kliendi saldoga.

-   Krediidilimiiti võrreldakse kliendi saldo ja saatelehe summadega.

-   Krediidilimiiti võrreldakse kliendi saldo ja kõigi avatud kandetegevustega. See hõlmab saatelehe summasid ja müügitellimuse summasid.

Vormi **Müügireskontro parameetrid** abil saate määrata teabe, millega võrrelda. Sellel vormil muudatuste tegemiseks peate olema süsteemiadministraatori (- SYSADMIN-) turberolli liige. Valige väljalt **Krediidilimiidi tüüp**, kas soovite krediidilimiiti kontrollida ja millist kandeteavet krediidilimiidi kontrollimisel lisada. Valige järgmiste variantide seast:

-   **Pole** – krediidilimiite ei kontrollita. Selle valiku saab konkreetse kliendi puhul alistada, märkides ruudu **Kohustuslik krediidilimiit** vormil **Kliendid**. Kui nii teete, kontrollitakse krediidilimiiti kliendi saldo suhtes.

-   **Saldo** – krediidilimiiti kontrollitakse kliendi saldo suhtes.

-   **Saldo + saateleht või toote sissetulek** – krediidilimiiti kontrollitakse kliendi saldo ja tarnete suhtes.

-   **Saldo + kõik** – krediidilimiiti kontrollitakse kliendi saldo, tarnete ja avatud tellimuste suhtes.

**Kus on teave kliendi järelejäänud kasutatava krediidi kohta?**

Andmed kliendi saldo ja järelejäänud krediidisumma kohta arvutatakse ja salvestatakse aegumise hetktõmmise loomisel ning kuvatakse vormil **Sissenõuded**. Vormil **Sissenõuded** kuvatavad summad ei pruugi sisaldada kõiki kandetegevusi uue aegumise hetktõmmise loomiseni. Lisateavet leiate teemast [Võlanõuded ja krediit moodulis Müügireskontro](https://technet.microsoft.com/library/hh209221.aspx).

Olenevalt valitud dokumentidest arvutatakse müügitellimuste, saatelehtede ja kliendiarvete värskendamisel andmed kliendi saldo ja järelejäänud krediidisumma kohta. Kui töös oleva dokumendi summa põhjustaks krediidilimiidi ületamise, kuvatakse teade.

**Kus saan määrata, kas kliendile krediidi andmiseks on vajalik ID, ja samuti krediidilimiidi, mis nõuab identifitseerimist?**

Vormil **Müügireskontro parameetrid** saate määrata, kas nõuda ID-d ja krediidilimiidi, mis nõuab ID-d.
Sellel vormil muudatuste tegemiseks peate olema süsteemiadministraatori (- SYSADMIN-) turberolli liige.

|    Väli                                    |    Kirjeldus                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Nõua krediidi puhul ID-d     |    Valige ID tüüp, mis tuleb sisestada klientide puhul, kellele teie juriidiline isik krediiti võimaldab. Sellel väljal tehtud valik määrab, millal ja millist tüüpi andmed on vajalikud riikliku IS väljadel vormil Kliendid. Ei – riiklikku ID-d ei nõuta vaatamata kliendi krediidilimiidile.     Jah – riiklikku litsentsinumbrit või muud riiklikku ID-d nõutakse siis, kui kliendi krediidilimiit on suurem või võrdne nulliga.     Minimaalne limiit – riiklikku litsentsi numbrit või muud riiklikku ID-d nõutakse siis, kui kliendi krediidilimiit on suurem või võrdne selle vormi väljale Limiit sisestatava limiidiga.        |
|    Piir                                    |    Sisestage krediidilimiit, millal nõutakse klientidele valitsuse väljastatud litsentsi numbrit või muud ID-d.    Tippige näiteks 2000, mis nõuaks, et tuleks sisestada ID-number (nt juhiloa number) klientide puhul, kelle krediidilimiit on 2000 või suurem.    See väli on saadaval, kui valisite väljalt Nõua krediidi puhul ID-d limiidi Miinimum.                                                                                                                                                                                                                                                                                                                                                                                                                                         |

**Kus saan määrata, kas krediidilimiidi ületamisel tuleks kuvada hoiatus või tõrge?**

Vormil **Müügireskontro parameetrid** saate määrata, kas kuvada krediidilimiidi ületamisel hoiatus või tõrge. See hoiatus või tõrge kuvatakse siis, kui kasutaja sisestab andmeid, või see lisatakse logisse, kui dokumente töötleb elektrooniline teenus. Sellel vormil muudatuste tegemiseks peate olema süsteemiadministraatori (- SYSADMIN-) turberolli liige.

|    Väli                                                               |    Kirjeldus                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Teade krediidilimiidi ületamisel (krediidireitingu alal)     |    Valige, kuidas krediidilimiitide ületamise teated kasutajatele kuvatakse. Tehke üks järgmistest valikutest. Tõrge – kuvatakse tõrketeade. See peatab tavaliselt käimasoleva toimingu ja vastuolu tuleb lahendada enne protsessi jätkamist.     Hoiatus – kuvatakse hoiatusteade, kuid protsessi saab jätkata.                     |
|    Teade krediidilimiidi ületamisel (AIFi alal)               |    Valige, kuidas krediidilimiitide ületamise teateid logis edastatakse. Valige järgmiste hulgast. Tõrge – vormil Erandid kuvatakse tõrketeade ja dokumenti ei töödelda enne, kui tõrge on kõrvaldatud.     Hoiatus – vormil Erandid kuvatakse hoiatusteade, kuid protsessi saab jätkata.        |

**Kuidas saan konkreetsele kliendile krediidilimiidi summa määrata?**

Konkreetsele kliendile määratakse krediidilimiidi summa vormil **Kliendid**. Sellel vormil muudatuste tegemiseks peate olema kohustust Kliendi koondandmete haldamine (CustCustomersMaintain) sisaldava turberolli liige.

1.  Klõpsake valikuid **Müügireskontro** \> **Üldine** \> **Kliendid** \> **Kõik kliendid**. Topeltklõpsake kliendikontot.

2.  Klõpsake tegumiriba vormil **Kliendid** nuppu **Redigeeri**.

3.  Sisestage valuutasumma väljale **Krediidilimiit**. See väärtus peab olema suurem kui null (0) ja seda kasutatakse krediidilimiidi summana.

4.  Kui see on nõutav, sisestage litsentsi number või muu riiklik ID väljale **Riiklik ID**.

> [!NOTE]
> Vormil **Müügireskontro parameetrid** on tavaliselt valitud krediidilimiidi tüüp. Kuid kui krediidilimiidi tüübiks on määratud **Pole**, peate märkima ka ruudu **Kohustuslik krediidilimiit** vormil **Kliendid**, et kontrollida kliendi krediidilimiiti kliendi saldo suhtes. Lisateavet krediidilimiidi tüüpide kohta leiate jaotisest „Milliste dokumentide ja protsesside krediidilimiiti saan kontrollida?” selles teemas. 

**Kuidas saan müügitellimuste puhul käsitsi krediidilimiite kontrollida?**

Mõnikord tuleb kliendi krediidilimiiti käsitsi kontrollida. Näiteks võite enne müügitellimuse sisestamise alustamist kliendi krediidilimiiti käsitsi kontrollida. Krediidilimiite saab kontrollida käsitsi vormil **Müügitellimus**. Sellel vormil muudatuste tegemiseks peate olema kohustust Müügitellimuse haldamine (SalesOrderMaintain) sisaldava turberolli liige.

1.  Klõpsake valikuid **Müük ja turundus** \> **Üldine** \> **Müügitellimused** \> **Kõik müügitellimused**. Topeltklõpsake müügitellimust.

2.  Klõpsake tegumiriba vormi **Müügitellimus** vahekaardil **Halda** valikut **Kontrolli krediidilimiiti**.
