---
title: Kanaliülese ühiskasutuse lubamine ja kasutamine
description: See artikkel kirjeldab, kuidas lubada ja kasutada saidikonstruktori kanaliülese Microsoft Dynamics 365 Commerce ühiskasutuse funktsiooni.
author: josaw1
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: c05da17327e61d6f61883ab97a403bf2cf8a68f1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270069"
---
# <a name="enable-and-use-cross-channel-sharing"></a>Kanaliülese ühiskasutuse lubamine ja kasutamine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas lubada ja kasutada saidikonstruktori kanaliülese Microsoft Dynamics 365 Commerce ühiskasutuse funktsiooni.

Kanaliülene ühiskasutus laseb jaemüüjatel taaskasutada ja jagada sisu saidi mitme kanali vahel. See võimalus on kasulik, kui saidi kanalitel on ühilduv baaskeel või kui neil on palju ühiseid sisuüksusi.

Kanaliülene ühiskasutus toimib vaikekanali lubamise kaudu, millest otsitakse saadaolevat sisu, kui taotletud sisu kanalipõhist versiooni ei leita. Kanalite vahel jagamiseks mõeldud sisu luuakse vaikekanalis. Seda sisu saab lokaliseerida mis tahes lokaadi jaoks, mida kasutatakse mis tahes saidikanalis.

## <a name="when-to-use-cross-channel-sharing"></a>Millal kanaliülest ühiskasutust kasutada?

Kanaliülene ühiskasutus on kasulik, kui ühe saidi mitu kanalit saavad sisu jagada. Näiteks saab jaemüüja, kellel on mitu kaubamärki ja kauplust, mis on toodud ühele saidile, jagada osa sisust mõne või kõigi kauplustega. See jagatud sisu võib hõlmata tingimuste, maksetingimuste, saatmisviiside ja korduma kippuvate küsimuste (KKK) lehti.

Kanaliülene ühiskasutus toetab ka fragmente. Seetõttu on võimalik luua kanalipõhiseid fragmente sisaldav sisuleht kanaliülese sisuna. Sel juhul, kuigi enamikku sisust jagatakse kanalite vahel, renderdatakse kanalipõhised fragmendid kanaliülesel lehel ainult siis, kui neid päritakse asjaomase poe kanalist.

Saidid, millel on ainult üks kanal, või saidid, millel on mitu kanalit, mis ei saa sisu jagada, ei saa kanaliülesest ühiskasutusest kasu.

## <a name="enable-cross-channel-sharing"></a>Kanaliülese ühiskasutuse lubamine

Kanaliülene ühiskasutus lubatakse saiditasemel. See toiming on ühesuunaline. Teisisõnu ei saa pärast kanaliülese ühiskasutuse lubamist seda enam keelata.

Et lubada kanaliülene ühiskasutus Commerce'i saidiehitajas, toimige järgmiselt.

1. Avage **Saidi sätted \> Funktsioonid**.
1. Seadke funktsiooni **Kanaliülene** suvandi väärtuseks **Sees**.

    ![Commerce'i saidiehitajas sisselülitatud kanaliülene suvand.](./media/enabling-cross-channel-sharing.png)

Pärast seda, kui lubate kanaliülese ühiskasutuse, kuvatakse kanaliülene teave jaotises **Kanalid**, mis asub jaotises **Saidi sätted \> Funktsioonid**, nagu järgmisel illustratsioonil näha.

![Kanalite teave, mis on nähtav pärast kanaliülese ühiskasutuse lubamist.](./media/channels-cross-channel.png)

Pärast seda, kui lubate kanaliülese ühiskasutuse, sisaldab Commerce'i saidiehitaja ülemises parempoolses nurgas olev väli **Kanal** suvandit **Kanaliülene e-pood**, mille abil saate hallata kanaliülest sisu, nagu on näidatud järgmisel illustratsioonil.

![Kanaliülese e-poe suvand väljal „Kanalid” pärast kanaliülese ühiskasutuse lubamist.](./media/cross-channel-dropdown.png)

## <a name="create-and-use-cross-channel-content"></a>Kanaliülese sisu loomine ja kasutamine

Kanaliülest sisu saate luua ja kasutada mitmel viisil. Näiteks saate luua kanaliüleseid fragmente, kanaliüleseid lehti, mis kasutavad kanaliülest ja kanalispetsiifilist sisu, ning alistada fragmentide kanalispetsiifiliste versioonide kaudu kanaliüleseid fragmente.

### <a name="create-a-cross-channel-fragment"></a>Kanaliülese fragmendi loomine

Et luua kanaliülene fragment Commerce'i saidiehitajas, toimige järgmiselt.

1. Avage **Fragmendid** ja valige uue fragmendi loomiseks **Uus**.
1. Valige dialoogiboksis **Uus fragment** moodul **Reklaambänner** ja seejärel sisestage jaotises **Fragmendi nimi** sellele nimi (nt **Kanaliülene bänner**). Seejärel valige **OK**.
1. Tehke mooduli **Reklaambänner** atribuudipaanil valikud **Lisa teade** ja **Teade**.
1. Sisestage dialoogiboksis **Teade** väljale **Tekst** väärtus **Kanaliülene** ja valige **OK**. 
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

Seda kanaliülest fragmenti saab kasutada kanaliülestel või kanalispetsiifilistel lehtedel, mis on loodud mis tahes saidikanalis.

### <a name="create-a-cross-channel-page-that-uses-cross-channel-content"></a>Kanaliülese lehe loomine, mis kasutab kanaliülest sisu

Kanaliüleseid lehti saab kasutada teie saidi mis tahes kanalis. Seetõttu saate luua jagatud sisulehe üks kord ja värskendada seda hiljem ühes kohas. Näiteks on võimalik jagada kanaliülest lehte **Tingimused**, mille URL on `/toc`, kõikide saidil olevate kanalite vahel. Kui saidikanalite baas-URL-id on `www.fabrikam.com/brand1` ja `www.fabrikam.com/brand2`, siis on sama kanaliülene jagatud leht **Tingimused** saadaval mõlema saidikanali URL-idel vastavalt `www.fabrikam.com/brand1/toc` ja `www.fabrikam.com/brand2/toc`. Kui lehte **Tingimused** tuleb hiljem värskendada, peate värskendama ainult üht jagatud lehte.

Commerce'i saidiehitajas kanaliülese lehe loomiseks, mis kasutab kanaliülest sisu, toimige järgmiselt.

1. Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.
1. Valige dialoogiboksis **Malli valimine** mõni mall, näiteks **Turundus**.
1. Sisestage väljale **Lehe nimi** lehele nimi (näiteks **Kanaliülene leht**).
1. Sisestage väljale **Lehe URL** lehele URL (nt **examplepage**) ja seejärel valige **OK**.
1. Valige uue lehe jaotises **Peamine** kolmikpunkt (**...**) ja seejärel valige **Lisa fragment**.
1. Valige dialoogiboksis **Fragmendi lisamine** varem loodud kanaliülene fragment, millel on reklaambänner, ja seejärel valige **OK**.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**. Peaksite nägema reklaambännerit, millel on kiri „Kanaliülene”.
1. Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

### <a name="create-a-channel-specific-page-that-uses-cross-channel-content"></a>Kanalispetsiifilise lehe loomine, mis kasutab kanaliülest sisu

Kui kasutate kanaliülest sisu kanalispetsiifilisel lehtedel, saate luua jagatud sisufragmendi ühe korra ja seejärel kasutada seda kanalispetsiifilistel lehtedel. See „ühekordne allikas” on kasulik jagatud sisu jaoks, nagu tingimused, maksetingimused või kontaktteave.

Commerce'i saidiehitajas kanalispetsiifilise lehe loomiseks, mis kasutab kanaliülest sisu, toimige järgmiselt.

1. Avage kindlas kanalis, näiteks kanalis **Fabrikami laiendatud e-pood**, jaotis **Lehed** ja valige **Uus**, et luua uus leht.
1. Valige dialoogiboksis **Malli valimine** mõni mall, näiteks **Turundus**.
1. Sisestage väljale **Lehe nimi** lehele nimi (näiteks **Kanalispetsiifiline leht**).
1. Sisestage väljale **Lehe URL** lehele URL (nt **channelspecificpage**) ja seejärel valige **OK**.
1. Valige uue lehe jaotises **Peamine** kolmikpunkt (**...**) ja seejärel valige **Lisa fragment**.
1. Valige dialoogiboksis **Fragmendi lisamine** jaotises **Kanal** suvand **Kanaliülene e-pood**. Varem loodud kanaliülene fragment peaks loendis olema. Valige see ning seejärel **OK**.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**. Peaksite nägema reklaambännerit, millel on kiri „Kanaliülene”.
1. Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

### <a name="create-a-channel-specific-version-of-a-cross-channel-page"></a>Kanaliülese lehe kanalispetsiifilise versiooni loomine

Kanaliülene ühiskasutus toetab kanaliülese sisu alistamist. Näiteks jagavad kõik saidikanalid peale ühe sama kindlat sisu. See üks saidikanal vajab erinevat sisu. Selleks, et rakendada selle puhul erinevat sisu, peate alistama kanaliülese sisu kanalispetsiifilise sisuga, luues kanaliülesest lehest kanalispetsiifilise versiooni.

Commerce'i saidiehitajas kanaliülese lehe kanalispetsiifilise versiooni loomiseks toimige järgmiselt.

1. Valige ülemises parempoolses väljas **Kanal** suvand **Kanaliülene e-pood**.
1. Avage varem loodud kanaliülene leht.
1. Valige ülemises parempoolses väljas **Kanal** see kanal, millel peaks olema kindel sisu. Leheredaktor kuvab teate, mis palub teil luua uus lehevariant.
1. Valige **Loo lehevariant**.
1. Valige lehevariandi pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.
1. Valige dialoogiboksis **Mooduli lisamine** moodul **Reklaambänner** ja klõpsake seejärel **OK**.
1. Tehke mooduli **Reklaambänner** atribuudipaanil valikud **Lisa teade** ja **Teade**.
1. Sisestage dialoogiboksis **Teade** väljale **Tekst** väärtus **Kanalispetsiifiline** ja valige **OK**.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**. Peaksite nägema reklaambännerit, millel on kiri „Kanalispetsiifiline”.
1. Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

Kui te kasutate nüüd kanali baas-URL-i ja avate selle saidi kanaliülese lehe URL-i, näete kanaliülese sisu asemel kanalispetsiifilist sisu.

## <a name="additional-resources"></a>Lisaressursid

[Sisu lisamise viisid](add-manage-content.md)

[Lehemudeli sõnastik](page-elements-overview.md)

[Dokumendi olekud ja töötsükkel](document-states-overview.md)

[Avaldamisrühmadega töötamine](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
