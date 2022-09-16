---
title: Varudest teadlikud tootekirjed
description: See artikkel kirjeldab, kuidas organisatsioonid saavad konfigureerida tooteloendi lehekülgi Microsoft Dynamics 365 Commerce oma e-äri veebisaidil, nii et nad on varudest kursis.
author: boycez
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-23
ms.openlocfilehash: 2a65dedf2da62fcd92169077d75a0f3b7832a86d
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473729"
---
# <a name="inventory-aware-product-listing"></a>Varudest teadlikud tootekirjed

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas organisatsioonid saavad konfigureerida tooteloendi lehekülgi Microsoft Dynamics 365 Commerce oma e-äri veebisaidil, nii et nad on varudest kursis. Tooteloendi leheküljed sisaldavad kategooria alapealdlehti ja otsingutulemuste lehekülgi.

Ostjad eeldavad üldiselt toote tuvastamist kogu e-äri veebisaidil, et olla kursis laovarudega, nii et nad saavad otsustada, mida teha, kui toode on laost otsas. Ärimooduli [teegi](starter-kit-overview.md) kategooriat ja otsingutulemuste mooduleid saab konfigureerida nii, et need sisaldaks laoandmeid. Sel viisil saavad nad pakkuda järgmisi kogemused:

- Kuvab kaubavaru taseme sildid koos toodetega.
- Laost väljas toodete peitmine tooteloendist
- Laost väljas toodete liigutamine tooteloendi lehtede alla
- Toetab laopõhise toote filtreerimist.

Nende kogemuste lubamiseks peate esmalt lubama täiustatud **e-commerce’i tootetuvastuse varude teadmise funktsiooniks** Commerce Headquartersis.

> [!NOTE]
> Äriversioonis 10.0.29 **ja uuemates versioonides on täiustatud e-kaubanduse** tootetuvastus varudest teadmise funktsioon vaikimisi lubatud.

## <a name="set-up-product-attribute-for-inventory-availability"></a>Saate häälestada toote atribuuti varude saadavuse jaoks.

Teadmise tooteloendis kasutatakse toote atribuutide raamistikku. Eeltingimusena tuleb varude saadaoleku andmete hõivamiseks luua sihtotstarbeline tooteatribuut.

Toote atribuudi häälestamiseks varude saadavuse jaoks Commerce Headquartersis järgige neid samme.

1. Minge jaemüügi ja **kaubanduse IT-toodete \>\> ja varude \> asusta tooteatribuudid varude tasemega**.
1. Sisestage **·** **dialoogiboksi** Asusta toote atribuudid varude taseme dialoogiboksi väljale Toote atribuut ja tüübi nimi sihtotstarbeline tooteatribuudi jaoks kohandatud nimi, mis luuakse varude andmete hõivamiseks.
1. Väljal Varude **saadavus valige koguse** tüüp, mis peaks varude taseme arvutuse aluseks olema. Füüsiliselt **saadav või** **Kokku saadaval**.
1. Seadke valiku **Pakktöötlus** väärtuseks **Jah**.
1. Valige nupp **OK**.

> [!NOTE]
> E-äri veebisaidi lehtedel varude taseme järjepidevaks arvutamiseks veenduge, **·** **et valite sama kogusetüübi nii varude saadavuses, mis põhinevad väljal Asusta tooteatribuudid varude taseme tööga** **ja Laotase, mis põhineb** Ärisaidi looja sättel.

Pärast sihtotstarbelise toote atribuudi loomist on järgmiseks sammuks võrgukanali atribuudi konfigureerimine.

Atribuudi konfigureerimiseks võrgukanali jaoks Commerce Headquartersis järgige neid samme.

1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kanali kategooriad ja toote atribuudid**.
1. Valige võrgukanal, et lubada varude teadmise tooteloendi kogemus.
1. Valige ja avage seostatud atribuudigrupp ning lisage seejärel uus toote atribuut.
1. Minge jaemüügi **ja rakenduse Commerce \> Retail ja Commerce IT jaotusgraafikusse \>** ja käitage **1150-töö** (**kataloog**). Soovitame teil planeerida see töö pakett-tööna, **mis töötab sama sagedusega kui laotaseme töö asusta tooteatribuudid**.

> [!NOTE]
> Äriversioonis 10.0.26 ja varasemas versioonis peate pärast varude saadavuse tooteatribuudi lisamine atribuudigruppi valima ka atribuudi metaandmete seadmine ja seejärel lülitama sisse atribuudi Kuva **kanalil,** **Tootav,** **·** **Saab täpsem olla ja teid saab** uue toote atribuudi jaoks päringusse teha.**·**

## <a name="configure-the-display-behavior-for-out-of-stock-products-on-product-listing-pages"></a>Laost väljas toodete kuvamiskäitumise konfigureerimine tooteloendilehtedel

Pärast kõigi eelnevate konfiguratsioonietappide lõpule viimist on kategooria ja otsingutulemuste lehtedel täpsustustel laopõhise filtri valik. Iga lehel kuvatava tootepaani kohta kuvatakse kaubavarude taseme silt.

Kategooria ja otsingu tulemusteleht kuvab tooteid koondtasemel, mitte tootevariandi tasemel. Laovaru tase, mis kuvatakse koos iga tootega, on koondatud kaubavaru tase, mille määrab kõigi tootevariantide laotase. Variandi laovarude tase arvutatakse commerce headquartersi võrgukanali vaikelaos oleva selle variandi vaba kaubavaru põhjal. Põhitoote laovarude tasemel on kaks võimalikku väärtust, mis tähistavad laoseis ja laost väljas olekut. Põhitoode loetakse laost otsas, kui kõik selle variandid on laost otsas. Vastasel juhul kaalutakse toodet laos. Väärtuse silt tuuakse laotaseme [definitsioonist](inventory-buffers-levels.md). Kui ühtegi kaubavaru taset pole määratletud, on vaikesildid (inglise keeles) saadaval **ja** **laost väljas**.

Saate konfigureerida Commerce’i **saidikonstruktoris** tooteloendi lehtede sätte Varude sätted, et kontrollida, kuidas kategooria ja otsingutulemuste leht kuvab laoseistud tooteid. Lisateavet vt teemast [Varude sätete rakendamine](inventory-settings.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
