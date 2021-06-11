---
title: Tootedimensiooni väärtuste konfigureerimine näidistena kuvamiseks
description: Selles teemas kirjeldatakse, kuidas konfigureerida tootedimensiooni väärtusi Microsoft Dynamics 365 Commerce peakorteris.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.20 update
ms.openlocfilehash: 08564ce7af7412f2501b917b3496942004402611
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117218"
---
# <a name="configure-product-dimension-values-to-appear-as-swatches"></a>Tootedimensiooni väärtuste konfigureerimine näidistena kuvamiseks

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Selles teemas kirjeldatakse, kuidas konfigureerida tootedimensiooni väärtusi Microsoft Dynamics 365 Commerce peakorteris. Lisateavet toote omanike kohta leiate jaotisest [Toote omanikud](../../supply-chain/pim/product-dimensions.md).

Dynamics 365 Commerce toetab suurust, stiili ja värvimõõtmeid tootevariantide eristamiseks. Tootedimensioonidel on sõbralikud nimed, mis kuvatakse toote üksikasjade lehtedel (PDP-d), et valida tootevariante. Nende sõbralike nimede hulka kuuluvad näiteks "Väike", "Keskmine" ja "Suur" suuruste jaoks ning "Must" ja "Pruun" värvide jaoks. Kui aga toode toetab paljusid variatsioone, võib tootevariantide sirvimine olla keeruline, sest iga variandi pildi vaatamiseks on vaja mitut valikut. Seetõttu võib olla klientide jaoks tootevariantide sirvimine ja valimine aeglane ja tüütu.

Kui dimensioone näidatakse PDP-de näidetena, saavad kliendid toote variatsioonidest visuaalse eelvaate. Nad saavad hõlpsasti sirvida mitmesuguseid värve, mustreid ja tekstuure ning kiiresti vaadata erinevaid tootevariatsioonide kombinatsioone.

Kuvamõõtmed näidete funktsioonina võimaldavad rakendusel Commerce kasutada kuueteistkümnendik (hex) koode ja pilte näidete dimensioonide kuvamiseks. Lisaks saab sarnaseid dimensioone, nagu näiteks värvid, tooteloendi lehtedel rühmitada. Näiteks, klient otsib siniseid tooteid. Kui erinevad sinise dimensiooni väärtused on rühmitatud, kuvatakse otsingutulemite loendilehel tooted, millel on erinevad sinised toonid. Dimensioonide rühmitamine parandab oluliselt toote täiustamise kogemust ja aitab klientidel leida rohkem tooteid ühe tooteotsingu päringu kaudu.

> [!NOTE]
> Ekraani mõõtmed näidete funktsioonina on saadaval alates Dynamics 365 Commerce versiooni 10.0.20 väljalaskest alates.

Järgmisel joonisel on toodud näide, kus värvid kuvatakse kaubandusliku PDP-s näidistena.

![Toote üksikasjade lehel näidistena kuvatud värvide näide](../dev-itpro/media/swatch_pdp.png)

Järgmine joonis näitab näidet, kus värvid kuvatakse kaubanduslike otsingutulemuste loendi lehel näidistena.

![Näide värvidest, mis kuvatakse otsingutulemuste loendi lehel näidistena](../dev-itpro/media/swatch_searchresults.PNG)

## <a name="enable-the-display-dimensions-as-swatches-feature-in-commerce-headquarters"></a>Lubage Commerce'i peakorteris displeimõõdud näidistena

Kuvadimensioonide lubamiseks näidis-funktsioonina Commerce peakorteris, minge **Tööruumide \> funktsioonide haldusse** ja lülitage sisse funktsioon **Luba tootedimensiooniväärtuste** lisa. Kui see funktsioonilipp on lubatud, lisatakse Commerce peakorteri vastavatesse tabelitesse iga dimensiooni jaoks kolm uut välja: **Hekskood**, **URL** (piltide jaoks) ja **Piiritlusgrupp**.

## <a name="configure-dimension-values-in-commerce-headquarters"></a>Dimensiooniväärtuste konfigureerimine Commerce peakorteris

Ekraanimõõtmeid kellade funktsioonina toetatakse suuruse, stiili ja värvidimensioonide puhul. Rakenduses Commerce Headquarters saab määrata sobivate dimensioonide hekskoodi ja pildi URL-i väärtused. Kui dimensiooni jaoks pole vaikimisi hex-koodi ja pildi URL-i väärtusi esitatud, näitab süsteem dimensiooni sõbraliku nime teksti.

Konfiguratsiooni saab teha ühel järgmistest tasemetest:

- **Dimensioon** – avage Commerce headquarters dimensiooni leht, otsides **värvi**, **Suurust** või **Laadi**. Igal leheküljel on ruudustikus dimensiooniväärtused. Saate hallata kuvamisjärjestuse, hex-koodi ja pildi URL-i väärtusi. Järgnev illustratsioon näitab lehe **Värvid** näidet.

    ![Näide dimensiooni konfiguratsioonist lehel Värvid](../dev-itpro/media/swatch_Color.PNG)

- **Dimensioonigrupp** – rakenduses Dynamics 365 Commerce saate dimensioonigruppide loomiseks kasutada atribuuti **Piiritlusgrupp**. Kui dimensioonigrupid on määratletud, avage sobiv leht, otsides **Värvigruppi**, **Suurusgruppi** või **Laadigruppi**. Igal lehel saate hallata heks-koodi, pildi URL-i ja piiritlusrühma väärtusi. Järgnev illustratsioon näitab lehe **Värvide grupp** näidet.

    ![Näide dimensiooni konfiguratsioonist lehel Värvide grupp](../dev-itpro/media/swatch_colorGroup.PNG)

- **Tootedimensioon (toote loomise ajal)** – uue toote loomisel saate dimensiooniväärtuste sisestamiseks kasutada lehte **Toote dimensioonid**. Olemasolevate toodete puhul võivad väljad **Heks-kood**, **URL** (piltide jaoks) ja **Piiritlusgrupp** olla juba seatud. Saate selle välja väärtust siiski muuta. Järgnev illustratsioon näitab konfiguratsiooni näidet **Toote dimensioonid** lehel.

    ![Näide dimensiooni konfiguratsioonist lehel Tooete dimensioonid lehel](../dev-itpro/media/swatch_product_dimensions.PNG)

> [!NOTE]
> Hex-koodi ja pildi URL-i konfiguratsioonide haldamise protsess järgib sama mustrit, mida kasutatakse dimensioonide kuvamisjärjestuse haldamiseks.

## <a name="configure-dimension-values-by-using-hex-codes"></a>Dimensiooniväärtuste konfigureerimine heks-koodide abil

Enamiku värvidimensioonide puhul tuleks Commerce Headquarters dimensioonilehtedel esitada heks-koodi värviväärtus. Näiteks peaks musta värvi hekskoodi väärtus olema **#00000**. Kui Commerce renderdab saidilehte, tähistab heks-koodi värviline näidis.

Järgmisel joonisel on kujutatud näide, kus värvidimensioonid on konfigureeritud heks-koodi väärtuste abil.

![Näide dimensiooni konfiguratsioonist, mis kasutab heks-koodi](../dev-itpro/media/swatch_color_hexcode.png)

## <a name="configure-dimension-values-by-using-image-urls"></a>Dimensiooniväärtuste konfigureerimine URLi pildi abil

Mõned värvimõõtmed esindavad mustreid, mitte täpseid värve. Näiteks võib värvidimensiooni kirjeldada kui "leopardi." Sellistel juhtudel saate värvimõõtmeid tõhusamalt esindada, kasutades kellade heks-koodide asemel avaldatud pilte.

Peate iga pildi Üles laadima Commerce site koostajasse ja selle avaldama. Seejärel sisestage avaldatud pildi pildi URL Commerce Headquarters vastavatele dimensioonilehtedele. Kui dimensioon on valitud kuvamiseks näiisena, kuid heksa-kood pole määratletud, teeb Commerce lehe renderdamisel pildi otsingu. Kui pildi otsing nurjub, näitab Commerce dimensiooni sõbraliku nime teksti.

Järgmisel illustratsioonil on näide, kus pildi URL-e kasutatakse konfiguratsiooniks **Värvid** lehel.

![Näide dimensiooni konfiguratsioonist, mis kasutab pildi URLi](../dev-itpro/media/swatch_color_urls.PNG)

Meediumimalli abil saate määratleda pildi URL-e nii nagu toote- ja kategooriapiltide puhul. Piltide üleslaadimisel saidikoosturisse peavad failinimede konventsioonid ja failiteed olema järjepidevad.

Järgmisel illustratsioonil on näide, kus meedia malli konfigureerimiseks kasutatakse pildi URL-e.

![Meediumimalli konfigureerimise näide](../dev-itpro/media/swatch_media_template.PNG)

## <a name="configure-dimension-values-by-using-both-hex-codes-and-image-urls"></a>Konfigureerige dimensiooniväärtused nii heks-koodide kui ka pildi URL-ide abil

Enamiku värvidimensioonide puhul saate konfigureerida nii heks-koode kui ka pildi URL-e. Kaubanduse renderdamise varuloogika otsib värvimalli kuvamiseks automaatselt kas heksakoodi või pildi URL-i. Kasutades värvidimensioonide konfigureerimiseks nii heksakoode kui ka pildi URL-e, aitate lihtsustada pildihaldust, kui värvide arv on suur.

Järgmisel illustratsioonil on näide, kus mõlemai, nii heksakooe, kui pildi URL-e kasutatakse konfiguratsiooniks **Värvid** lehel.

![Näide dimensiooni konfiguratsioonist, mis kasutab mõlemaid, nii heksakoode, kui pildi URLe](../dev-itpro/media/swatch_color_hexandimage.png)

## <a name="configure-refiner-groups"></a>Piiritlusgruppide konfigureerimine

Kui määratlete dimensiooniväärtuse jaoks heksakoodi või pildi URL-i, saate määrata ka **Piiritlusgrupi** välja väärtuse. See väli määratleb dimensiooni, mida tuleks kasutada sarnaste dimensiooniväärtuste rühmitamiseks piiritluskogemuses.

Näiteks kui teie värvidimensiooni väärtused on "sinine", "siniruuduline", "pesusinine" ja "tumesinine", vastendatakse iga väärtus erineva heksakoodi või pildi URL-iga. Seetõttu kuvatakse iga väärtus sobivate toodete PDP-del tootekaartidel erineva värvina. Kui aga vastendate kõik need värvidimensiooni väärtused **Piiritlusgrupi** väärtusega **Sinine**, loob "siniste" toodete otsing loendilehe otsingutulemused toodete jaoks, mille dimensioonivärviväärtused on "sinine", "sinine ruuduline", "pesusinine" ja "tumesinine".

Järgmise joonise näites on kujutatud Commerce Headquarters atribuutide **Värv** ja **Piiritlusgrupp** seoseid.

![Piiritlusgrupi halduse näide](../dev-itpro/media/swatch_refiner_group.png)

## <a name="manage-images-in-commerce-site-builder"></a>Hallake pilte Commerce site ehitajas

Kui mõne dimensiooniväärtuse puhul kasutatakse pildi URL-e, tuleb vastavad pildid üles laadida Commerce site ehitajasse. Iga pildi asukoht peaks vastama Commerce'i peakorteris pildi jaoks määratletud failinimele ja kaustateele. Pildifailid tuleb üles laadida saidikoosturi vastavatesse kategooriakohtadesse. Näiteks tuleb värvipildid üles laadida **Värv** kategooria kausta. Lisateavet piltide üleslaadimise kohta saidiehitaja meediumiteeki leiate teemast [Piltide üleslaadimine](../dam-upload-images.md).

Järgmisel joonisel on kujutatud näide, kus **Failide üleslaadimine** dialoogiboksi kasutatakse piltide üleslaadimiseks saidikoosturi meediumiteeki. See tõstab esile **Suurus**, **Värv** ja **Laad** valikuks saada olevad kategooriad.

![Pildifailikategooriate näide saidikoosturi meediumiteeki üleslaadimise ajal](../dev-itpro/media/swatch_sitebuilder.png)

## <a name="enable-swatch-display-on-e-commerce-site-pages"></a>Lubage näidiskuvade kuvamine e-commerce site koostajas

Enne kui kellad kuvatakse e-kaubanduse saidi lehtedel, mis nõuavad dimensioonivalimist, näiteks PDP-d ja loendilehed, peate konfigureerima dimensioonisaidi sätted Commerce peakorteris. Lisateavet leiate teemast [Saidisätete rakendamine dimensioonidele](../dimension-settings.md).

Lisaks peaksite lubama otsingutulemite moodulite atribuudi **Kaasa toote atribuudid otsingutulemites**. Kui teie sait kasutab kohandatud kategoorialehti, peaksite värskendama nendel lehtedel kasutatavaid otsingutulemite mooduleid, et lubada atribuut **Kaasa toote atribuudid otsingutulemitesse**. Lisateabe saamiseks vaata [Otsingutulemuste moodul](../search-result-module.md).

## <a name="display-swatches-in-pos-and-other-channels"></a>POS-i ja muude kanalite näidiste kuvamine

Rakendusel Commerce pole praegu erandlikku rakendust, mis toetaks kellade kuvamist müügikohas (POS) ja muudes kanalites. Siiski saate proovivõtte kuvamise funktsiooni rakendada laiendina, mis paneb kanali API-d tagastama heitkoodide renderdamiseks vajalikud heksakoodid ja pildi URL-id.

## <a name="additional-resources"></a>Lisaressursid

[Otsingutulemuste moodul](../search-result-module.md)

[Dimensioonidele saidisätete rakendamine](../dimension-settings.md)

[Tootedimensioonid](../../supply-chain/pim/product-dimensions.md)

[Pildi üleslaadimine](../dam-upload-images.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
