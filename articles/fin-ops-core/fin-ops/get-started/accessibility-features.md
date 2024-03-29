---
title: Hõlbustusfunktsioonid
description: See artikkel kirjeldab funktsioone, mis on mõeldud erinevate puuetega kasutajate abistamiseks.
author: jasongre
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 4e6a077cc7848448233ed5f94f9b1ba5b385c3fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284019"
---
# <a name="accessibility-features"></a>Hõlbustusfunktsioonid

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

See artikkel kirjeldab funktsioone, mis on loodud aitamaks kasutajaid, kellel on erinevad puuetega kasutajad seda rakendust kasutama. Näiteks on saadaval funktsioonid inimestele, kes kasutavad nägemist abistavaid tehnoloogiaid, nagu Microsoft Windowsi jutustaja.

## <a name="windows-narrator-and-keyboard-only-access"></a>Windowsi jutustaja ja juurdepääs ainult klaviatuuriga

Igal väljal ja juhtelemendil on silt ning kohaldatavate kiirklahvide kirjeldus. Ekraanilugeja saab lugeda silti ja kirjeldust.

## <a name="shortcuts-for-the-most-frequently-performed-actions"></a>Kõige sagedamini tehtavate tegevuste kiirklahvid

Enamiku kasutajate korral hõlmab süsteemi igapäevane kasutamine rohkelt andmesisestust ja klaviatuuri kasutamist. Kasutuskogemuse parandamiseks võtsime kasutusele kiirklahvid, mis aitavad teil ekraanil ringi liikuda, ning kiirklahvid spetsiaalsete tegevuste jaoks. Lisateavet vt teemast [Kiirklahvid](shortcut-keys.md).

## <a name="navigation-search"></a>Navigeerimisotsing

Kõik lehed, millele pääseb juurde navigeerimispaani menüü kaudu (kõige vasakpoolsem paan), on saadaval ka välja **Otsing** kaudu. Vajutage klahvikombinatsiooni Alt + G, et nihutada fookus väljale **Otsing**. ja seejärel sisestage lehe nimi või kirjeldus.

![Otsinguväljale sisestati „pangakonto”](media/6d08b0be32808221023e2aa92d69fd70.png "Otsinguväljale sisestati „pangakonto”")

Lisateavet vt teemast [Navigeerimisotsing](navigation-search.md).

> [!NOTE]
> Saate liikuda otse ainult ülataseme lehtedele. Sekundaarsed lehed tuginevad nende vastavatel emalehtedel olevale teabele või sisule.

## <a name="action-search-for-keyboard-only-users-or-for-heads-down-data-entry"></a>Tegevuse otsing ainult klaviatuuri kasutavate kasutajate jaoks või veatuvastuseta andmesisestuse jaoks

Igale lehel esitatud tegevusele saab juurdepääsu klaviatuurilt, kasutades tabeldusjärjestust. Teave vahekaartide järjestuse kohta antakse hiljem selles artiklis. Tegevuste käivitamiseks otsesemalt saate kasutada tegevuse otsimise funktsiooni.

### <a name="example"></a>Näide

Soovite käivitada tegevuse **Meiliteatise logi**, mis asub toimingupaani vahekaardil **Müügitellimus** grupis **Meiliteatis**.

![Meiliteatise logitegevus toimingupaanil.](media/f0d78399e7fafcd85ded1cd1e3d34f3c.jpg "„Meiliteatise logitegevus&quot; toimingupaanil")

Üks võimalus on kasutada klaviatuuri. Vajutage klahvikombinatsiooni Ctrl + F6, et nihutada fookus tegevuspaanile ja vajutage seejärel korduvalt tabeldusklahvi (TAB), et liikuda läbi kõigi vahekaartide ja tegevuste, kuni fookus on tegevusel **Meiliteatise logi**.

Kuid saate tegevuse käivitada ka otsesemalt. Vajutage lehel mistahes kohas klahvikombinatsiooni Ctrl + ülakoma ('), et kuvada tegevuste otsinguväli.

![Tegevuste otsinguväli.](media/80f7e8c5ac412fdf2c8a12f7728f135a.jpg "Tegevuste otsinguväli")

Sisestage otsinguväljale sõnad, mis kirjeldavad tegevust. Tegevus on tehtud teile kättesaadavaks ja te saate seda otse käitada. Näiteks, kui sisestate sõnad **meil**, **teatis** või **logi**, saate kohe hüpata meiliteatise logi funktsiooni juurde.

![Otsinguväljale sisestati „meil”](media/image4.png "Otsinguväljale sisestati „meil”")

![Otsinguväljale sisestati „teatis”](media/image5.png "Otsinguväljale sisestati „teatis”")

![Otsinguväljale sisestati „logi”](media/image6.png "Otsinguväljale sisestati „logi”")

Kui olete lõpetanud, võite uuesti vajutada klahvikombinatsiooni Ctrl + ülakoma, et naasta fookus väljale, millega töötasite enne tegevuse otsingu käivitamist.

Lisateavet vt teemast [Tegevuse otsing](action-search.md).

## <a name="tab-sequence"></a>Tabeldusjärjestus

Süsteemi tavapärasel igapäeval kasutamisel ei ole tavapäraste ülesannete täitmiseks kõiki välju vaja. Seetõttu on tabeldusjärjestus vaikimisi „optimeeritud”. Tabelduskohad on määratud ainult väljadele, mis on vajalikud tüüpiliste stsenaariumide jaoks.

Siiski võib juhtuda, et mõned väljad, mida kasutate tihti teatud ülesannete täitmiseks, ei ole vaikimisi tabeldusjärjestusse lisatud. Sellisel juhul, kui kasutate Windowsi jutustajat, saate nendele väljadele juurdepääsu saamiseks ja nende sisu kontrollimiseks kasutada Windowsi jutustaja klaviatuuri tegevusi. Teise võimalusena saate lehel **Suvandid** lülitada sisse suvandi **Täiustatud tabeldusjärjestus**. See suvand lisab kõik redigeeritavad ja kirjutuskaitstud väljad tabeldusjärjestusse. Seejärel saate kasutada lehe isikupärastamist, et luua kohandatud tabeldusjärjestus ja jätta välja väljad, mida ei ole tabeldusjärjestusse vaja. Lisateavet isikupärastamise kohta vt teemast [Kasutuskogemuse isikupärastamine](personalize-user-experience.md).

![Suvand "Täiustatud tabeldusjärjestus"](media/8c0f12bbb3f26032997ef0ba95d89b6a.png "Suvand „Täiustatud tabeldusjärjestus&quot;")

## <a name="form-patterns"></a>Vormi mustrid

Ligikaudu 90 protsenti rakenduses olevatest lehtedest põhinevad väikestel mustrikomplektidel. Neid mustreid nimetatakse *vormimustriteks*. Iga vormimustrit kasutatakse lehel kõige sagedamini tehtavate toimingute esitamiseks. Vormimuster teeb kasutamise selgemaks ja arusaadavamaks, sest sageli kasutatavad tegevused ja andmed esitatakse erinevatel lehtedel alati samas kohas. Kuna vormimustreid on vähe, saavad kasutajad süsteemi hõlpsalt tundma õppida, olenemata selles olevate lehekülgede arvust, ja saavad seda pärast vormimustrite äratundmist enesekindlalt kasutada.

Lisateave vormimustrite kohta vt teemast [Vormi laadid ja mustrid](../../dev-itpro/user-interface/form-styles-patterns.md).

## <a name="responsive-layout"></a>Reageeriv paigutus

Toode on loodud töötama erinevates seadmetes ja vormiteguritel, alates väikestest ekraanidest ja lõpetades kõige suurema eraldusvõimega suurte ekraanidega. Meie reageeriva paigutuse mootor võimaldab kasutajatel suurendada kuni 200 protsendini (või mõnel juhul rohkem kui 200 protsenti).

Nutitelefonid ja muud väikesed ekraanid, juhtelemendid ja vormi kavandid kohanduvad, et tagada põhiliste andmete soosimine. Need tundlikud käitumised võivad hõlmata ka veergude arvu vähendamist gruppides ja vahekaartides ühte veergu, elementide peitmist ja tegevuse paani ahendamist.

## <a name="guidance-to-help-developers-and-customers-incorporate-accessible-thinking-in-their-customizations"></a>Juhendid, mis aitavad arendajatel ja klientidel oma kohandamistesse kaasata hõlbustavat mõtteviisi

Lisateabe saamiseks parimate tavade kohta, mida Microsoft kasutab hõlbustatuse lihtsustamiseks, vt teemat [Vormide, toodete ja juhtelementide hõlbustatus](../../dev-itpro/user-interface/enable-accessibility.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
