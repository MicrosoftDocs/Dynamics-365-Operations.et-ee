---
title: Kuluhalduse konfigureerimine
description: "Selles artiklis kirjeldatakse kaalutlusi ja otsuseid, mille peate protsessi plaanimise käigus tegema, enne kui Microsoft Dynamics AX-is kuluhaldust konfigureerite. Kuluhalduse alal saate salvestada teavet makseviiside, reisitellimuste, kuluaruannete, poliitikate jm kohta."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 447ba56a279a29392b00119730c3594fa4ea80f6
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="configure-expense-management"></a>Kuluhalduse konfigureerimine

[!include[banner](../includes/banner.md)]


Selles artiklis kirjeldatakse kaalutlusi ja otsuseid, mille peate protsessi plaanimise käigus tegema, enne kui Microsoft Dynamics AX-is kuluhaldust konfigureerite. Kuluhalduse alal saate salvestada teavet makseviiside, reisitellimuste, kuluaruannete, poliitikate jm kohta. 

Kuna paljud otsused, mida kuluhalduse konfiguratsiooni plaanimisel langetate, põhinevad organisatsiooni hierarhial ja finantsstruktuuril, tuleb juhinduda nende valdkondade plaanimisdokumentidest.

## <a name="intercompany-expenses"></a>Kontsernisisesed kulud
Kui lubate ettevõttesisesed kulud, lubate juriidilistele isikutel ja töötajatel kanda kulusid teise teie organisatsiooni kuuluva juriidilise isiku nimel ja koguda temalt makseid. Näiteks täidab juriidilise isiku A töötaja projekti juriidilisele isikule B. Kui ettevõttesisesed kulud on lubatud, võib töötaja siis esitada juriidilisele isikule B ajatabeli ja saada temalt tasu. Kui teie organisatsioonis pole mitut juriidilist isikut, pole vaja ettevõttesiseseid kulusid lubada. **Otsus:** kas soovite lubada ettevõttesisesed kulud?

## <a name="financial-management"></a>Finantshaldus
Kuluhaldus on tihedalt seotud organisatsiooni finantshaldusega. Suur osa kuluhalduse konfiguratsioonist põhineb otsustel, mille olete oma organisatsiooni finantside kohta langetanud. Järgmised jaotised kirjeldavad erinevaid valdkondi, kus on vajalik plaanimine ja otsustamine organisatsiooni rahaliste otsuste ja juhtkonna juhiste põhjal.

### <a name="per-diems"></a>Päevarahad

Peate määratlema töötajate päevarahad, mida teie organisatsioon maksab. Kuna päevarahasid kasutatakse tavaliselt selliste kulude katmiseks nagu toitlustus, majutus ja muud ettenägematud kulud, saate koostada ettevõtte makstavate päevarahade reeglid. Päevaraha määrade aluseks võib olla aastaaeg, reisisiht või mõlemad. Päevaraha reegli määratlemisel saate valida päevaraha määrast mingi protsendi kinnipidamise, kui töötaja saab tasuta eineid või teenuseid. Saate määratleda ka päevaraha määrade järgud, määrates minimaalse ja maksimaalse tundide arvu, millele päevaraha määr töötaja reisi ajal rakendatakse. **Otsused.**

-   Esimese ja viimase päeva vaikepäevaraha reeglid:
    -   Milline on minimaalne tundide arv, mida töötaja saab ühes päevas taotleda ja siiski päevaraha saada?
    -   Kas esimese ja viimase päeva puhul vähendatakse toitlustusele kuluvat summat? Kui nii, siis milline on vähendamise protsent?
    -   Kas esimese ja viimase päeva puhul vähendatakse hotellile kuluvat summat? Kui nii, siis milline on vähendamise protsent?
    -   Kas esimese ja viimase päeva puhul vähendatakse muude kulude summat? Kui nii, siis milline on vähendamise protsent?
-   Päevaraha vaikereeglid:
    -   Kas päevaraha vähendatakse protsentuaalselt iga toidukorra kohta, kui näiteks tasuta toitlustust pakutakse? Kui nii, siis milline on iga toidukorra vähendamise protsent?
    -   Kas toitlustamisega seotud vähendamine arvutatakse päeva, reisi või päevase toidukordade arvu alusel?
    -   Kas päevaraha summad tuleks ümardada tavaliselt või ülespoole?
    -   Kas päevarahade arvutused põhinevad 24-tunnisel perioodil või kalendripäeval?
-   Päevaraha reeglid asukoha alusel:
    -   Kas päevaraha määrad erinevad asukohtade põhjal ja milliseid asukohti arvestatakse?
    -   Kui päevaraha määr erineb asukoha põhjal, siis milline protsendimäär eraldatakse iga asukoha puhul:
        -   toitlustusele
        -   hotellile
        -   muudele kuludele

### <a name="expense-management-journals-and-accounts"></a>Kuluhalduse töölehed ja kontod

Kuluhaldus nõuab, et kasutaksite mitut töölehte ja kontot. Peate näiteks otsustama, kas avansimaksete ja krediitkaardivaidluste jaoks kasutatakse sama kontot. **Otsused.**

-   Millistele pearaamatukontodele kinnitatud kuluaruanded sisestatakse?
-   Millist kontot kasutatakse avansimaksete puhul?
-   Kas avansimaksed tuleks kohe sisestada?

### <a name="payment-methods"></a>Makseviisid

Kui lubate töötajatel ettevõtte nimel kulusid tekitada, peate määratlema makseviisid, mida töötajatel on lubatud kasutada. Näiteks võite lubada töötajatel kasutada sularaha või ettevõtte krediitkaarti. Võib lubada töötajatel kasutada ka isiklikku krediitkaarti ja seejärel töötajatele kulud korvata. Iga lubatud makseviisi puhul tuleb teha järgmised otsused. **Otsused:**

-   Millised makseviisid on lubatud?
-   Kellele kuuluvad makseviisi kulud?
-   Kas on olemas vastaskonto tüüp? Kui nii, siis milline see on?
-   Kui on olemas vastaskonto, milline see konto on?
-   Kui makseviis on krediitkaart, kas makseviisi tuleks kasutada ainult imporditud kannetega?

### <a name="expense-categories-and-shared-categories"></a>Kulukategooriad ja jagatud kategooriad

Kui töötajad koostavad kuluaruande, tuleb iga kulu, mille nad seal kajastavad, seostada kulukategooriaga. Kulukategooriad on tuletatud jagatud kategooriatest, mida saab jagada kõigi organisatsiooni juriidiliste isikute vahel. Neid kategooriaid saab jagada ka projektijuhtimise ja raamatupidamise moodulites, olenevalt sellest, kuidas teie organisatsioon on määratletud. Organisatsiooni määratluse ja rakendustöörühma juhtimise alusel saate määrata, kas kuluhalduses kasutatavaid kategooriaid kasutatakse ainult kuludes või neid tuleks projekti ja kulude vahel jagada. Arvestage, et neid kategooriaid saab jagada projekti ja kulu või projekti ja tootmise vahel, kuid mitte kulu ja tootmise vahel. Peate langetama iga kulukategooria kohta järgmised otsused. **Otsused.**

-   Milline on kulukategooria? Näiteks lennukipiletid, hotell või läbisõit.
-   Kas seda kulukategooriat saab kasutada ka moodulis Projektihaldus ja raamatupidamine?
-   Milline on kulutüüp?
-   Milline on kulukategooria vaikemakseviis?
-   Kas selle kategooria kulud tuleb üksikasjalikult loetleda?
-   Milline on kulukategooria peamine vaikekonto?
-   Mis on selle kulukategooria kauba käibemaksu vaikegrupp?
-   Kas selle kulukategooria puhul on lubatud täiendavad makseviisid? Kui nii, siis millised?
-   Kas selles kulukategoorias on alamkategooriaid? Kui nii, siis
    -   kas mõni alamkategooria on maksu korvamisest välja jäetud?
    -   Milline on alamkategooriate kauba käibemaksugrupp?

    Kui seda kulukategooriat kasutatakse ka moodulis Projektihaldus ja raamatupidamine, siis vastake ülejäänud küsimustele. Vastasel korral olete selle osaga lõpetanud.
-   Milliseid kulukontosid järgmiste puhul kasutatakse?
    -   Kulu
    -   Palga eraldamine
    -   Lõpetamata toodang – omahind
    -   Kulu – kaup
    -   Lõpetamata toodang – Omahind – Kaup
    -   Tekkepõhine kahjum
    -   Lõpetamata toodang – Tekkepõhine kahjum
-   Milliseid tulukontosid järgmiste puhul kasutatakse?
    -   Arveldatud tulu
    -   Viittulu – müügihind
    -   Lõpetamata toodang – müügihind
    -   Viittulu – tootmine
    -   Lõpetamata toodang – tootmine
    -   Viittulu – kasum
    -   Lõpetamata toodang – kasum
    -   Viittulu – kordustellimus
    -   Lõpetamata toodang – kordustellimus

 

### <a name="taxes"></a>Maksud

Kuludega seotud maksude puhul tuleb määratleda, mis kuluaruannetes sisaldub või seal lubatud on. **Otsused.**

-   Kas kulusummades sisaldub käibemaks?
-   Kas kulude puhul tuleks maksu korvamine lubada?

Arvestage, et kui otsustasite pearaamatu plaanimise ajal rakendada USA käibemaksu ja kasutada maksureegleid, määrates välja **Rakenda käibemaksu maksustamisreeglid** olekuks Jah, ei saa kuludelt maksu korvamist lubada.

## <a name="policies"></a>Poliitikad
Saate luua kuluaruande poliitikaid, et teie organisatsioon saaks säästa aega ja raha, kui töötajatel organisatsiooni nimel tegutsedes kulud tekivad. Poliitikate abil saab tagada, et töötajad püsivad eelarves, esitavad kõik vajaliku teabe ja kulutavad raha ainult vajalikul viisil. Iga loodava kuluaruande poliitika ja iga kuluaruande kinnitamispoliitika puhul tuleb teha järgmised otsused. **Otsused.**

-   Mis on poliitika nimi?
-   Mille jaoks kulupoliitika mõeldud on?
-   Kui otsustasite eelnevalt lubada ettevõttesiseseid kulusid, siis millistele teie organisatsiooni ettevõtetele poliitika kehtib?
-   Millal poliitika jõustub?
-   Millal poliitika aegub?
-   Mis see poliitikareegel on?
-   Mis on selle poliitikareegli tulemus?





