---
title: Allahindluste näitamine kassas
description: Selle teema all selgitatakse, kuidas Microsoft Dynamics 365 Commerce aitab müügipartneritel õppida tundma kampaaniaid ja seda, kuidas neid saab kasutada ristmüümis- ja edasimüümisliikumisteks.
author: ShalabhjainMSFT
ms.date: 07/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Commerce
ms.author: asharchw
ms.search.validFrom: 2020-02-28
ms.dyn365.ops.version: Application update 10.0.10
ms.openlocfilehash: 9e3fa5030cb684c01153d255ca2bd34d9be7dc9945f0c7ec26985cf74540b73d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731663"
---
# <a name="show-discounts-in-pos"></a>Näita allahindlusi kassas

[!include [banner](includes/banner.md)]

Kampaaniad mängivad olulist rolli nende klientide motiveerimisel, kes teevad ostuotsuseid. Näiteks võivad pühad anda jaemüüjatele suurima müükide arvu, sest kogu jaemüügiturg on üle ujutatud ahvatlevate kampaaniate ja allahindlustega. Kui kaupluse kaastöötajad teavad ja mõistavad olemasolevaid kampaaniaid, saavad nad neid kampaaniaid kasutades teha hõlpsalt kaupade rist- ja edasimüüki. Selle teema all selgitatakse, kuidas Microsoft Dynamics 365 Commerce aitab müügipartneritel õppida tundma kampaaniaid ja seda, kuidas neid saab kasutada ristmüümis- ja edasimüümisliikumisteks.

## <a name="learn-about-store-discounts"></a>Lisateave kaupluse allahindluste kohta

Kaubandus sisaldab operatsiooni, mida nimetatakse "Kuva kõik allahindlused". Selle operatsiooniga kuvatakse kõik kaupluses praegu kehtivad allahindlused. Operatsiooni "Kuva kõik allahindlused" saab vastendada nupuga kassas (POS) ja selle nupu saab lisada lehele **Tervitus** või lehele **Kanne** . Järgneval pildil kuvatakse näidet avatud lehest **Kõik allahindlused** .

![Leht Kõik allahindlused.](./media/View_all_discounts.png "Leht Kõik allahindlused")

Allahindluste kuvamiseks otsib süsteem kõiki allahindlusi, mis vastavad ühele või mitmele järgmistest tingimustest:

- Allahindluse rühm ühtib kaupluse hinnarühmaga.
- Allahindlusrühm on vastendatud kuuluvuse- või püsikliendiprogrammiga.
- Allahindlusrühm on vastendatud kauplusega seotud kataloogiga.

Lehel **Kõik allahindlused** kuvatakse ainult mõned kupongil põhinevad allahindlused, sest jaemüüjad loovad tavaliselt tuhandeid kuponge ja vastavaid allahindlusi kordumatutele klientidele ning see lehekülg ei ole ette nähtud kliendiomaste allahindluste näitamiseks. Kupongil põhinevad allahindlused kuvatakse ainult siis, kui suvand **Rakenda ilma kupongikoodita** on iga kupongi päises sisse lülitatud. Sel juhul saab kassiir kupongi rakendada kupongikoodi või vöötkoodi sisestamata või skannimata.

Kui suvand **Rakenda ilma kupongikoodita** on sisse lülitatud, muutuvad võimalikuks erinevad stsenaariumid. Näiteks võivad kassiirid pakkuda klientidele lisaallahindlusi kliendi rahuloluks või toote defektide tõttu. Prinditud kupongikoode või vöötkoode ei tule kassiiridele jagada. Selle asemel saavad kassiirid valida nupu **Rakenda kupong** . Kupong rakendatakse seejärel kandele automaatselt. Kui kupongi päisele on olemas mitu kupongi, valib süsteem kandel automaatselt esimese aktiivse kupongi.

Lehel **Kõik allahindlused** saavad müügiesindajad otsida allahindlusi ka märksõnade alusel. Märksõnaotsing otsib väljadelt, kus on allahindluse nimi ja allahindluse kirjeldus. Müügiesindajad saavad allahindlusi ka filtreerida, lähtudes sellest, kas allahindlus nõuab kupongikoodi.

## <a name="cross-sell-and-upsell-by-using-discounts"></a>Ristmüük ja edasimüük kasutades allahindlusi

Multiallahindlus, nt koguseallahindlused, segu- ja sobitusallahindlused ning läveallahindlused, on suurepärane viis klientide motiveerimiseks ostma rohkem tooteid, et saada suuremaid allahindlusi. Seetõttu aitavad need suurendada ka kliendi ostukorvi ja jaemüüja tulu. Neid allahindlusi saab avaldada e-kaubanduse veebisaitidel, sotsiaalmeediumis ja kauplusebänneritel.

Kuid isegi kui kasutatakse kõiki neid avalikustamismeetodeid, võivad kliendid jääda kampaaniate kasutamise võimalustest ilma. Kui soovite, et müügiesindajad teaksid, milliseid kampaaniaid on võimalik rakendada valitud real või isegi kogu ostukorvi ulatuses, võivad jaemüüjad lisada toimingunupu **„Kuva saadaolevad allahindlused“** lehe **Tehing** mis tahes nupuruudustikule. Pärast seda saab müügiesindaja valida kanderea ja seejärel valida selle nupu, et kuvada kõik valitud reale saadaolevad allahindlused. Müügiesindaja saab valida ka muu vahekaardi, et näidata allahindlusi, mis kehtivad kogu kandele. On oluline märkida, et funktsioon **Kuva saadaolevad allahindlused** ei näita allahindlusi, mis on juba müügireale rakendatud, kuna allahindluse teave on juba müügireal kuvatud. Selle stsenaariumi eesmärk on näidata ainult allahindlusi, mida pole veel rakendatud. Erandiks on allahindlused, mida rakendatakse kupongi põhjal, mis on märgitud kui „Rakenda ilma kupongikoodita”. See teeb rakendatud kupongi eemaldamise müügiesindajate jaoks lihtsaks.

Lehel **Kõik allahindlused** kuvatakse ainult need allahindlused, mis ei konkureeri ühegi rakendatud allahindlusega. Selline käitumine aitab tagada, et kui müügiesindaja teavitab klienti allahindlusest ja klient võtab vajalikud meetmed (nt klient ostab veel ühe üksuse, et saada 10 protsenti allahindlust), rakendatakse allahindlus kandele. Kupongil põhinevad allahindlused kuvatakse ainult siis, kui suvand **Rakenda ilma kupongikoodita** on sisse lülitatud.

Lihtsa stsenaariumi korral, kus kõik allahindlused on sama prioriteediga, on koosallahindluse režiim **Seotud** ja koosallahindluse korrigeerimise juhtelement on seatud **Parim hind ja seotus prioriteedi piires, mitte kunagi prioriteetide seotus**, lehel **Kõik allahindlused** kuvatakse toote kõik olemasolevad allahindlused, sest kõik allahindlused on seotud ja omavahel ei konkureeri.

Järgmised pildid näitavad loogikat, mis määrab, millised allahindlused kuvatakse täpsemates stsenaariumites, nagu stsenaariumis, mille puhul allahindluse kaasrežiim on **Parim hind** või **Eksklusiivne**, ja kasutatakse kahte või enamat prioriteeti. Sellistes stsenaariumites on näidatud allahindlused lisaks mõjutatud lähtudes sellest, kas allahindluse kaastoime kontroll on seatud **Parimale hinnale ja seosele prioriteedi piires, mitte kunagi prioriteetide seosele** või **Parimale hinnale ainult prioriteedi piires, alati prioriteedi seosele**.

Järgmisel pildil on kujutatud loogikat, mida kasutatakse juhul, kui allahindluse konkureerimiskontroll on seatud **Parimale hinnale ja seosele prioriteedi piires, mitte kunagi seosele üle prioriteetide**.

![Loogika Parima hinna ja seose prioriteedi piires, mitte kunagi seos üle prioriteetide.](./media/Model_1.png "Loogika Parim hind ja seos prioriteedi piires, mitte kunagi seos üle prioriteetide").

Järgmisel pildil on kujutatud loogikat, mida kasutatakse juhul, kui allahindluse konkureerimiskontroll on seatud **Parimale hinnale ainult prioriteedi piires, alati seos üle prioriteedi**.

![Loogika Parim hind ainult prioriteedi piires, alati seos üle prioriteedi.](./media/Model_2.png "Loogika Parim hind ainult prioriteedi piires, alati seos üle prioriteedi").


[!INCLUDE[footer-include](../includes/footer-banner.md)]