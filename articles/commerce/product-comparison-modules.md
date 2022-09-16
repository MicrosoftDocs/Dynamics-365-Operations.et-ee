---
title: Tootevõrdluse moodulid
description: See artikkel kirjeldab tootevõrdluse mooduleid ja nende juurutamist, nii et kliendid saavad teha tootevõrdlusi Microsoft Dynamics 365 Commerce e-kaubanduse veebisaitidel.
author: ashishmsft
ms.date: 08/09/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 6fd851ce6b32d0772c3fe23c4d7bd4dae2616fdc
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474122"
---
# <a name="product-comparison-modules"></a>Tootevõrdluse moodulid

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab tootevõrdluse mooduleid ja nende juurutamist, nii et kliendid saavad teha tootevõrdlusi Microsoft Dynamics 365 Commerce e-kaubanduse veebisaitidel.

> [!NOTE]
> Tootevõrdluse ja tootevõrdluse nupumoodulid on saadaval versiooni Dynamics 365 Commerce 10.0.29 väljalaskest. Neid saab kasutada nii ettevõtete-tarbe- (B2C) kui ka ettevõtete-ettevõtete (B2B) veebisaitidel.

Tootevõrdluse funktsioonid lasevad ostjatel võrrelda toote üksikasju tootevõrdluse lehel, et aidata neil teha paremate ostuotsuste tegemist. Seda funktsiooni konfigureeritakse Commerce’i saidikonstruktoris, kasutades tootevõrdluse moodulit. Tooteloendi lehtedel (PLP), nt kategooria tulemused, otsingutulemused ja tootekogumite lehed, saate konfigureerida tootevõrdluse nupu, mis võimaldab ostjal lisada tooteid võrdlussalve. See funktsioon on konfigureeritud saidikonstruktoris, kasutades toote võrdluse nupumoodulit, mis töötab kiirvaate [moodulina](quick-view-module.md).

Kui saidi kasutajad lisavad võrdluseks tooteid, valides need tootepaanil, ilmub lehe allosas võrdlussalv. Võrdlussalv näitab tooteid, mida ostja praegu võrdleb, koos lühikeste toodete eelvaatega. Saidi kasutajad saavad toote üksikasjalehtedelt (PDP-dega) tooteid lisada ja nad saavad tooteesimestega võrdlemiseks lisada kindlaid tootevariantide.

Pärast seda, kui kliendid on võrdlussalve mõned tooted **liinud**, saavad nad valida suvandi Võrdle, et suunata toote võrdluslehele. Tootevõrdluse lehel kuvatakse iga valitud toote toote üksikasjad, et kliendid saaksid võrrelda pilte, hindu, tootedimensioone (suurus, stiil ja värv), koondhinnangute teavet ja muid tooteatribuute.

Järgmine näide näitab tootevõrdluse nupu näiteid, võrdluse nupust eemaldamist, võrdlussalve ja toote võrdluslehte.

![Tootevõrdluse ülevaade, kuvades võrdlustoote nupu, võrdluse nupust eemaldamise, võrdluse salvepaneeli ja toote võrdluslehe.](./media/Product-Comparison-Overview.png)

> [!NOTE]
> - Toote võrdluse lehel võrreldakse toote atribuutide vaikekomplekti ja kõiki atribuute, mida saab antud toote PDP-s näha.
> - Atribuute, nt tarneviisi, vaba kaubavaru ja mõõtühikuid, ei saa toote võrdluslehel kuvada.
> - Kliendid saavad lisada erinevate kategooriate tooteid võrdluse salve, eeldusel, et tooted on samast kataloogist.
> - Tootevõrdluse funktsioonid on praegu piiratud toodete võrdlemisega üksikus kataloogis. Saidi kasutajad ei saa teha kataloogiülesi võrdlusi.
> - Veenduge, et renderdamismooduli **kliendi atribuut on** tühjendatud kõigi toote võrdlusmoodulite puhul.
> - Peaksite tagama, et lehetasandi vahemälustus on keelatud kõigil lehtedel, kus kasutatakse toote võrdlusmoodulit. Need leheküljed sisaldavad PDP-sid, PLP-sid ja toote võrdluslehti. Lisateavet vt konfigureerimislehe [vahemälust](e-commerce-extensibility/page-caching.md).

Järgmine illustratsioon näitab toote võrdluse lehe näidet.

![Toote võrdluse leht](./media/Product-Comparison-Page.png)

## <a name="add-the-product-comparison-module-to-a-new-product-comparison-page"></a>Lisa toote võrdlusmoodul uuele toote võrdluslehele

Saate luua sihtotstarbelise tootevõrdluse lehe, lisades toote võrdluse mooduli lehe kehale. Lisaks sellele, et lubada klientidel võrrelda erinevate toodete toote üksikasju, saate konfigureerida tootevõrdluse mooduli, et anda klientidele võimalus oma ostud pärast toodete võrdlemist kiiresti lõpule viia. Toote võrdlusmoodul sisaldab ka **tühja** võrdluspesa, kuhu saate lisada sisublokki mooduli, mis kirjeldab tühja olekut (nt kui teie toote võrdlus on tühi").

Toote võrdlusmooduli lisamiseks uuele toote võrdluslehele järgige neid samme.

1. Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.
1. Dialoogiboksis Uue **lehe loomine lehe** nime **all** sisestage sobiv lehe nimi (nt **Toote võrdlus**) ja seejärel valige **Edasi**.
1. Valige **jaotises Vali mall** sobiv mall (nt vaikekategooriate lehel kasutatav mall) ja seejärel klõpsake nuppu **Edasi**.
1. Valige **valiku Vali paigutus** all lehekülje paigutus (nt Paindlik **paigutus**) ja seejärel klõpsake nuppu **Edasi**.
1. Vaadake **jaotises Ülevaade ja lõpetamine** üle lehe konfiguratsioon. Kui peate lehekülje teavet redigeerima, valige suvand **Tagasi**. Kui lehekülje teave on õige, valige Loo **leht**.
1. Põhipesas valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige konteinerimoodul **ja** seejärel valige **OK**.
1. Valige konteineri pesast kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Valige** moodulid valige toote võrdluse **moodul** ja seejärel valige **OK**.
1. Valige kiirvaate nupupesast kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige toote kiirvaate **moodul** ja seejärel valige **OK**.
1. Konfigureerige parempoolsel atribuutide paanil toote kiirvaate **mooduli** atribuudid.
1. Valige tühjal **võrdluspesal** kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige sisublokti **moodul** ja seejärel valige **OK**.
1. Konfigureerige parempoolsel atribuutide paanil sisubloki **mooduli** atribuudid. 
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.
1. Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

Järgmine näide näitab tühja võrdluslehe näidet saidiloojas.

![Tootevõrdluse moodul](./media/Product-comparison-module.png)

## <a name="add-a-product-comparison-button-to-product-tiles-on-search-and-category-results-pages"></a>Toote võrdluse nupu lisamine toote paanidele otsingu- ja kategooriatulemuste lehtedel

Toote võrdluse nupp võimaldab kasutajatel toodete sirvimisel loendilehel toote kiiresti võrdlussalve lisada. Nad saavad loendilehelt lisada võrdlussalve ühe või mitu toodet ilma PDP-sse minekuta.

Toote võrdluse nuppu toetavad tootekogum, otsingutulemused ja PDP ostuboksi moodulid.

Toote võrdluse nupu lisamiseks toote paanidele otsingu ja kategooria tulemuste lehtedel järgige neid samme.

1. Minge saidikonstruktori **lehekülgedele** ja avage kategooria lehekülg, millele soovite tootevõrdluse nupu lisada.
1. Põhipesas valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige otsingutulemuste **moodul** ja seejärel valige **OK**.
1. Otsingutulemuste **mooduli tootevõrdluse** nupu **pesas** valige ellips (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Valige** moodulid valige toote võrdluse **nupu moodul** ja seejärel valige **OK**.
1. Atribuutide paanil paremal konfigureerige toote võrdluse **nupu mooduli** atribuudid.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.
1. Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="specify-the-maximum-number-of-products-to-show-in-the-comparison-tray"></a>Määrake toodete maksimaalne arv, mida võrdlussalves kuvada.

Saate määrata võrdlussalves näidatatavate toodete maksimaalse arvu, kui kasutate saidikonstruktori **\> saidisätete** laiendusi. Saate konfigureerida eraldi maksimaalsed piirid töölaua- ja mobiili-/tahvelarvutivaadetele. Kui maksimumpiiri pole määratletud, siis piirangut vaikimisi ei jõustata.

> [!NOTE]
> Optimaalse sirvimiskogemuse **tagamiseks on soovitatav seadistada toodete maksimaalne arv võrdlussalves 2-ks** **mobiili vaateporti puhul ja 4** töölaua vaateporti, et vähendada nõutud horisontaalse kerimise kogust.

Toodete maksimaalse arvu määramiseks võrdlussalves järgige neid samme.

1. Minge saidikonstruktoris saidisätete **laiendustele \>**.
1. Toodete puhul **võrdluspiirangus –** töölaua seadmete atribuut, sisestage toodete maksimaalne arv, mida tuleb töölaua vaateportide võrdlussalves kuvada.
1. Toodete puhul **võrdluslimiidis – mobiili- ja tahvelarvutiseadmete** atribuut, sisestage toodete maksimaalne arv, mida tuleb mobiilseadmete ja tahvelarvutite vaateportide võrdlussalves kuvada.
1. Käsuribal valige salvestamine **ja avaldamine**.

![Saidi sätted võrdlussalve toodete piiramiseks.](./media/Site-settings-to-limit-products-in-comparison-tray.png)
