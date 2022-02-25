---
title: B2B-äripartnerite haldamine kliendi hierarhiaid kasutades
description: See teema kirjeldab, kuidas kasutada kliendi Microsoft Dynamics 365 Commerce hierarhiaid äripartnerite haldamiseks ettevõtete ja ettevõtete (B2B) e-kaubanduse veebisaitidel.
author: josaw1
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d6e594cbb824a8b823912118e99b819585adc45e
ms.sourcegitcommit: 8bcb9c13eccb14e61c39ca6578d135b64090fad2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2022
ms.locfileid: "8313842"
---
# <a name="manage-b2b-business-partners-using-customer-hierarchies"></a>B2B-äripartnerite haldamine kliendi hierarhiaid kasutades

[!include [banner](../../includes/banner.md)]

See teema kirjeldab, kuidas kasutada kliendi Microsoft Dynamics 365 Commerce hierarhiaid äripartnerite haldamiseks ettevõtete ja ettevõtete (B2B) e-kaubanduse veebisaitidel.

Commerce headquartersis kasutatakse kliendi *hierarhia* üksust äripartneri organisatsioonide esindamiseks, mis kasutavad teie B2B e-äri saiti. Enne kui saate alustada kliendi hierarhiate kasutamist äripartnerite haldamiseks, peate lubama Commerce Headquartersis B2B e-äri võimalused ja seejärel määratlema kliendi hierarhia numbriseeria.

## <a name="enable-the-b2b-e-commerce-feature-in-commerce-headquarters"></a>Commerce Headquartersis B2B e-commerce'i funktsiooni lubamine

B2B e-kaubanduse **võimaluste kasutamiseks peate esmalt lubama B2B eCommerce-võimaluste** kasutamise funktsiooni Commerce headquartersis.

1. Avage **Tööruumid \> Funktsioonihaldus**.
1. Kasutage vahekaardil **Kõik** filtriboksi, et otsida moodulit **Retail ja Commerce**.
1. Leidke B2B **eCommerce'i** võimaluste kasutamise lubamisfunktsioon, **valige** see ja valige siis parempoolses allnurgas suvand Luba kohe.

## <a name="define-a-number-sequence-for-the-customer-hierarchy"></a>Kliendihierarhia numbriseeria määratlemine

Numbriseeriaid kasutatakse loetavate ainuidentifikaatorite loomiseks koondandmete ja kannete kirjete jaoks, mis nõuavad identifikaatoreid. Peate määratlema numbriseeria, mida kasutatakse kliendi hierarhia ID loomiseks. Numbriseeriate kohta leiate lisateavet teemast [Numbriseeriate ülevaade](/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview).

Commerce Headquartersis kliendi hierarhia numbriseeria määratlemiseks järgige neid samme.

1. Minge rakenduse **Retail ja Commerce \> Headquarters häälestuse \> numbriseeriate \> numbriseeriatele**.
1. Looge uus numbriseeria või valige olemasolev numbriseeria selle uuesti kasutamiseks.
1. Valige suvandid **Jaemüük ja kaubandus \> Headquartersi häälestus \> Parameetrid \> Commerce’i ühiskasutuses parameetrid**.
1. **Lisage vahekaardil Numbriseeriad** numbriseeria, mille lõite või valisite varem kliendi **hierarhia ID viitele**.

![Kliendi hierarhia ID viitele lisatud numbriseeria.](../media/NumberSequenceCustHierarchy.png)

## <a name="how-the-approval-process-works"></a>Kinnitusprotsessi töö

Kui äripartner taotleb B2B e-kaubanduse saidiga liitumist, salvestab süsteem taotluse potentsiaalse *kliendina*. Rakenduse Commerce headquarters persona,nt jaemüügitoimingute juht saab kinnitada või tagasi lükata partneri taotlusi. Lisateavet äripartneri taotluste ja potentsiaalse kliendi kinnituste haldamise kohta [vt B2B e-äri veebisaidi jaotisest Äripartneri kasutajate haldamine](manage-b2b-users.md).

Kui potentsiaalne klient kinnitatakse, loob süsteem kaks uut kliendikirjet:

- Üks organisatsiooni tüüpi kliendikirje **tähistab** organisatsiooni, mis taotleb äripartneriks muutumist.
- Üks isiku tüüpi kliendikirje **tähistab** taotluse esitanud isikut.

Lisaks luuakse Jaemüügi ja ärikliendi kliendihierarhiates **uus kliendihierarhia \>\> kirje**. Sellel kliendihierarhia kirjel on järgmised atribuudid:

- **Kliendihierarhia ID** – kliendihierarhia kordumatu ID. See ID kasutab Äriportaali ühisparameetrites määratud numbriseeriat.
- **Nimi** - äripartneri organisatsiooni nimi, nagu on määratletud liitumistaotluses. Selle välja sisu on redigeeritav.
- **Eesmärk** - see atribuut on seadistatud eelmääratletud väärtusele **B2B organisatsioon**.
- **Organisatsioon** – äripartneri organisatsiooni kliendi ID.

Saabumistaotluse esitanud isik lisatakse hierarhia **kiirkaardile** **ja administraatori roll** on neile määratud. Kuna administraator lisab äripartneri organisatsioonile B2B-saidil veel kasutajaid, luuakse iga kasutaja jaoks uus kliendikirje. Kliendikirje lisatakse ka äripartneri vastavale kliendihierarhia kirjele ja sellele **on** määratud kasutaja roll.

### <a name="examples"></a>Näited

Isik, kelle nimi on Sam J. esitab Microsofti organisatsiooni nimel sisseseadmistaotluse. Kui taotlus on kinnitatud, luuakse kaks uut kliendikontot: üks **Sam** J-i ja üks **Microsofti organisatsiooni** tüübist.

Nagu järgmise näite näitest näha, luuakse ka uus kliendi hierarhia kirje. Kirjel on organisatsiooniga (**Microsoft)** sama nimi ja **administraatorroll** määratud Sam J-le. Administraator Sam J. lisab sellele hierarhiale kõik teised B2B-saidi **Microsofti kasutajad ja määrab neile** Kasutaja. Selles näites on Sush R. lisatud kasutajana.

![Kliendi hierarhia kirje näide.](../media/CustomerHierarchy2.png)

Määramaks, kas klient on seotud kliendi hierarhiaga, avage kliendikirje. Nagu näha järgmises illustratsioonis, **näitab jaemüügi kiirkaardi jaotise B2B** kliendi hierarhia ID **väli**, kas klient on kliendi hierarhia osa ja B2B **administraatori suvand näitab,** kas klient on **selle** hierarhia administraator.

![Näide jaotisest B2B kliendikirje jaemüügi kiirkaardil, kus klient on seotud hierarhiaga ja määratud administraatorina.](../media/CustomerHierarchyMapping2.png)

Enamasti peaksid hierarhia kõikide kliendikirjete atribuudiväärtused ühtima. Näiteks, kuna kõik äripartneri kasutajad peaksid saama toodetele sarnaseid hindu, peavad nende hinnagrupp ja seotud konfiguratsioonid ühtima. Süsteem ei jõusta siiski seda ühtsust. Seetõttu vastutavad asjakohased Commerce'i peakontori kasutajad selle eest, et atribuudi väärtused ja konfiguratsioonid ühtiksid kõigi antud hierarhia klientidega.

Commerce Headquartersi kasutajad saavad kontrollida atribuudiväärtusi kõigi hierarhia kliendikirjete puhul kõrvuti vaates. Nagu järgmise illustratsiooni näitest näha, saate kasutada suvandit Üldine kiirkaardi Hierarhia ripploendis ja seejärel valida mis tahes osa kliendikirjest, **·** **et** näidata seotud atribuute. Kasutajad saavad atribuudiväärtusi otse selles vaates redigeerida. Kõigi väärtuste kopeerimiseks administraatori kliendikirjest kõigile kasutajatele valige **alistamine** **hierarhia kiirkaardil.**

![Kliendi hierarhiakirje näide, kus kuvatakse alistamisnupp ja ripploendi suvand.](../media/HierarchyDetails2.png)

[!include [footer-include](../../includes/footer-banner.md)]
