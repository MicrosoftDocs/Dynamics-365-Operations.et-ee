---
title: Pakkumiste loomine, kinnitamine ja allkirjastamine
description: Selles teemas kirjeldatakse kuidas luua, kinnitada ja allkirjastada kandidaadile tehtavat pakkumist kasutades rakendust Dynamics 365 for Talent.
author: josaw
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-10-19
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: be66d9f95551066bb8bc25445c652d4fa59066d4
ms.openlocfilehash: f189df052ef299a2cca1d92065a7a4d377d25399
ms.contentlocale: et-ee
ms.lasthandoff: 12/07/2018

---

# <a name="creating-approving-and-signing-offers"></a>Pakkumiste loomine, kinnitamine ja allkirjastamine

[!include[banner](../includes/banner.md)]

Paljudel juhtudel peab kandidaadile pakkumise paketi koostamine olema väga kiire protsess.
Attracti administraatori seadistatud mallide abil saate vähendada pakkumiste loojate aega ja vaeva kandidaadile pakkumiste koostamisel ja saatmisel.

## <a name="create-an-offer"></a>Pakkumise loomine

Kui pakkumise haldamise rakendus on sisse lülitatud, saavad kõik personalijuhi või värbaja rolli omavad kasutajad kandidaadile pakkumise paketi koostada. Pakkumise koostamiseks toimige järgmiselt.

1.  Liikuge töö ja selle kandidaadi avalduse juurde, kellele pakkumist loote.

1.  Avage **Pakkumise etapp** ja klõpsake **Koosta pakkumine** peal.

    Teid suunatakse pakkumise rakendusse, kus näete kandidaati olekuga **Uus**. Näete ka teisi pakkumisi, mille osaline olete, kas siis looja või kinnitajana.

1.  Klõpsake **Koosta pakkumine**. 
    
    Kuvatakse erinevate administraatori poolt saadavaks tehtud pakkumise pakettide valik.

1.  Pakkumise koostamise alustamiseks valige pakett ja klõpsake **Valmis**.

    Laetakse pakkumise paketi mall, kuhu on sisestatud vastava töö ja kandidaadi üksikasjad.

1.  Kõik teised pakkumise paketi osaks olevad pakkumise andmete kohatäited on sihtlehel näha. Saate kogu paketi väärtused sisestada sellel lehel.

    Sihtlehel näete ka kõiki pakkumise dokumendi malle, mis on pakkumise paketi osaks.

1.  Olenevalt sellest, kuidas mall administraatori poolt seadistatud on, võib teil nüüd olla võimalik pakkumise sisu redigeerida.

1.  Kui teil on vaja mittevajalikeks märgitud dokumente eemaldada, saate seda teha.

1. Kui kõik pakkumise andmete kohatäiteid on täidetud, klõpsake pakkumise mustandi salvestamiseks **Salvestada**.

>[!NOTE]
> Pärast mustandi salvestamist saate pakkumise mustandversiooni kustutada või valida vajadusel uue paketi malli.


## <a name="approve-an-offer"></a>Pakkumise kinnitamine

Enamik pakkumisi peavad läbima kinnitusprotsessi veendumaks, et pakkumine vastab vajalikele standarditele. Kui pakkumine ei vasta standarditele, näiteks kui pakkumise looja ei järgi pakkumise andmete reegleid ja muudab pakkumise väärtusi, volitatakse kinnitusprotsess. Pakkumise kinnitamisele saatmiseks toimige järgmiselt.

1.  Kui pakkumine on mustandi olekus, lisage **Kinnitaja paneel** kaudu kinnitajad. 
    >[!NOTE]
    > Personalijuhid lisatakse vaikimisi kinnitajateks. Pakkumise kinnitajaks võite valida ükskõik millise kasutaja oma organisatsioonist.

1.  Vajadusel määrake kinnitajad järjestikuste kinnitamise meetodil või paralleelse kinnitamise meetodil. See valik on saadaval ainult siis, kui see oli sellisena administraatori poolt seadistatud.
    >[!NOTE]
    > Järjestikuste kinnitusprotsessi puhul saate soovi korral muuta kinnitajate järjekorda.

1.  Kui olete kinnitamise järjekorra määramisega valmis, saate muuta kinnitusmeili sisu ja seejärel saata kinnitajatele teatise. Klõpsake **Saada kinnitajatele**.
    >[!NOTE]
    > Kui pakkumine on mittestandardne, tuleb teil esitada põhjendus.

1.  Kui pakkumise looja soovib kinnitaja vahele jätta, saavad nad lisada märkuse ja liikuda edasi järgmise kinnitaja juurde.

Kinnitajad saavad meili palvega pakkumine kinnitada. Nad saavad meilis olevale lingile klõpsates pakkumise avada, terve pakkumise paketi läbi vaadata ja selle kas kinnitada või pakkumise loojale tagasi saata. Kui pakkumise kinnitajad pakkumise paketi tagasi lükkavad ja muutmisele saadavad, peavad nad lisama märkuse. 

Juhul, kui enne kinnitaja reageerimist on pakkumisest loodud uus versioon, ei saa kinnitaja pakkumist kinnitada ega tagasi lükata.

## <a name="offer-versioning"></a>Pakkumise versioonid 

Kui pakkumine on kinnitatud või redigeerimiseks tagasi saadetud, saate pakkumisest uue versiooni loomiseks valida **Luba redigeerimine**. Pakkumise versiooni uuele versioonile kantakse kõik pakkumise andmete väärtused ja kinnitajate loend üle eelmisest versioonist. 

Kui versioone kinnitajatega kinnitamiseks jagati, saavad kinnitajad liikuda pakkumise erinevate versioonide vahel. Samuti saab kinnitaja või pakkumise looja teatud pakkumise versiooni mustandi kustutada, et minna tagasi eelmisesse olekusse.


## <a name="send-an-offer-to-a-candidate"></a>Kandidaadile pakkumise saatmine 

Kui pakkumine on salvestatud, kinnitatud ja kandidaadile saatmiseks valmis, klõpsake **Saada kandidaadile**.

Enne pakkumise kandidaadile saatmist saate teha mitmeid tegevusi.
-  Saate vaadata kandidaadile saadetava pakkumise paketi osaks olevate dokumentide loendit.

-  Saate määrata pakkumise aegumiskuupäeva. Kandidaatide oodatakse pakkumise kinnitamist või tagasi lükkamist enne aegumiskuupäeva.  Kandidaadile saadetakse meeldetuletus 48 tundi enne pakkumise aegumist.

-  Võib olla soovite pakkumise kinnitamise protsessi lisada lisadokumente. Teil on võimalik lisada nõutava dokumendi tüüp.

- Elektroonilise allkirja valik: kui Adobe Sign on valitud eelistatud elektroonilise allkirjastamise meetodina, peavad pakkumiste loojad ühendama oma Adobe Sign litsentsi. On kaks võimalust. Valige kasutaja **Sätted** jaotises **Pakkumine**, jaotise all **Ühendused** looge ühendus jaotisega **Adobe Sign**. Teise võimalusena palutakse teil luua ühendus ekraaniga Saada pakkumine kandidaadile, kui ei ole juba ühendust kasutaja sätete põhjal loodud. 

> [!NOTE]
> Kasutajatel tuleb Adobe Sign'iga ühenduda vaid ühe korra. Sama kasutajalitsentsi kasutatakse tulevaste pakkumispakettide puhul, mis on välja saadetud sama kasutaja poolt. 

-  Vajadusel saate meilimalli vaadata ja redigeerida.

Kui pakkumine on valmis ja klõpsate **Saada kandidaadile**, saab kandidaat meili, et pakkumine ootab läbi vaatamist.


## <a name="candidates-actions-after-receiving-an-offer"></a>Kandidaadi tegevused pärast pakkumise saamist

Kui kandidaati on teavitatud, te temaga on jagatud pakkumist, saab ta klõpsata meilis olevale lingile ja minna rakenduse armatuurlauale, et pakkumine läbi vaadata. Armatuurlaud näitab kandidaadile kõiki tegevusi, mis tal tuleb veel teostada.

1.  Pakkumise ja kõigi sellega seotud dokumentide vaatamiseks peab kandidaat klõpsama **Vaata pakkumist** peal.

    Kandidaadid saavad pakkumise paketi ka .zip vormingus alla laadida.

1.  Pakkumise vastu võtmiseks peavad kandidaadid klõpsama kõigi pakkumise paketi osaks oleva dokumentide juures valikul **Liigu allkirja juurde**.

1.  Kui kõik dokumendid on eraldi allkirjastatud ja kinnitatud, peab kandidaat vastuvõtmise protsessi kinnitama, klõpsates lehe ülaosas valikule **Võta pakkumine vastu**.

1.  Pakkumise tagasi lükkamiseks peab kandidaat klõpsama lehe ülaservas valikut **Lükka pakkumine tagasi**, valima asjakohase põhjuse, lisama vajadusel kommentaari ja klõpsama **Lükka tagasi**.

1.  Pärast pakkumise vastu võtmist või tagasi lükkamist võib kandidaat jääda pakkumise vaatesse või minna tagasi rakenduse armatuurlauale.

1.  Kui pakkumise vastuvõtmise protsessis oli küsitud muid dokumente, peab kandidaat need dokumendid vajadusel üles laadima ja märgistama need nõutud dokumenditüübiga.

1.  Kui kõik dokumendid on üles laaditud ja pakkumise pakett on allkirjastatud, teavitatakse pakkumise loojat.


## <a name="withdrawing-an-offer"></a>Pakkumise tagasivõtmine

Pakkumise võib kandidaadilt igal ajahetkel erinevatel põhjustel tagasi võtta. 
1.  Võtke pakkumine tagasi klõpsates ellipsnuppu (**...**) ja seejärel klõpsates **Võta pakkumine tagasi**. 

2. Kuvatakse teadet, mis küsib, kas kandidaati on oleku muudatusest teavitatud. Kui kandidaadiga ei ole veel ühendust võetud, on teil võimalik saata kandidaadile meil, teavitades teda täiendavatest tegevustest. 

   Pakkumine ei ole enam kandidaadi poolt ligipääsetav.


## <a name="closing-an-offer"></a>Pakkumise sulgemine 

Kui pakkumine on vastu võetud, tagasi lükatud või tagasi võetud, võite lisatoiminguid teostamata pakkumise sulgeda nii, et sellele pakkumise paketile ei saa enam lisanduvaid muudatusi teha.

