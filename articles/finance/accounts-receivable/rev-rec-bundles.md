---
title: Tulu tuvastamise kogumid
description: Selles teemas kirjeldatakse müügireskontro tulu tuvastamise võimekuse kogumifunktsiooni. Kogum sisaldab emakaupa ja mitut koostiskaupa.
author: kweekley
ms.date: 01/04/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 9afc7786de16cb1cada982f43beb956e062777a4
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347778"
---
# <a name="revenue-recognition-bundles"></a>Tulu tuvastamise kogumid

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse müügireskontro tulu tuvastamise võimekuse kogumifunktsiooni. Kogum sisaldab emakaupa ja mitut koostiskaupa. Emakaup sisestatakse müügitellimusele, et tellimuse kirje oleks tõhusam. Kuid seejärel jaotatakse see koostiskaupadeks. Sisedokumentides, nt saatelehel, loetletakse koostiskaubad. Kuid välisdokumentides näidatakse ainult emakaup.

> [!NOTE]
> Microsoft Dynamics 365 Commerce'i kanalid, nt veeb, kassa (POS) ja kõnekeskused, ei toeta tulu tuvastamist (sh kogumifunktsiooni). See hõlmab Dynamics 365 Supply Chain Managementi ja Dynamics 365 Salesi lahendust Potentsiaalne klient sularahaks. Tulu tuvastamiseks konfigureeritud kaupu ei tohiks lisada tellimustele või kannetele, mis on loodud Commerce'i kanalites või lahenduses Potentsiaalne klient sularahaks.

Kogumite häälestamiseks peate sisestama tulu tuvastamise konfiguratsioonivõtmed. Kuid saate kogumeid kasutada ka juhul, kui tulu tuvastamine pole häälestatud. Sarnaselt saate kasutada ka tulu tuvastamist, kui kogumid pole häälestatud. Kui tulu tuvastamine on häälestatud, määratlevad koostiskaubad tulu hinna ja tulu graafiku, mida kasutatakse müügitellimuse arveldamisel tulu tuvastamiseks või viitvõlaks.

Kogumite häälestamisel kasutatakse koosluse (BOM) funktsiooni. Lisateavet kogumi kauba häälestamise kohta vt teemast [Tulu tuvastamise häälestus](revenue-recognition-setup.md). Kui emakaup on märgitud kogumina, koheldakse seda teisiti kui teisi koosluse kaupu. Erinevused on järgmised.

- Kogumid tuleb jaotada müügitellimuse kinnituse kaudu, valides müügitellimuse lehe toimingupaani vahekaardil **Müük** valiku **Müügitellimuste kinnitamine**. Kogumi kaupade jaotamiseks ei tohi kunagi valida kiirkaardil **Müügitellimuse read** menüüs **Müügitellimuse rida** jaotises **Jaota** valikut **Koosluse rida**. Vastasel juhul käsitletakse kaupa kooslusena, mitte kogumina.
- Kogumi kaupa sisaldav müügitellimus tuleb enne saatelehe või arve loomist kinnitada.
- Kui kogum jaotatakse müügitellimuse kinnituse kaudu, siis emakaup tühistatakse ning selle ühiku hind ja allahindlused eraldatakse kogumi koostiskaupadele.
- Koostiskaupade summa peab alati võrduma emakauba hinnaga. Seetõttu kehtivad koostiskaupade väljade uuendamisele ja muutmisele piirangud. Näiteks ei saa ühiku hinda käsitsi muuta. Seda ei saa muuta ka kaudselt, jõustades uue hinnaleppe. Uue hinnaleppe takistamiseks ei saa koostiskaupadel muuta varude dimensioone.
- Välissuunalise dokumendi (nt müügitellimuse kinnituse või arve) printimisel prinditakse emakaup, mitte koostiskaubad.

## <a name="bundles-on-sales-orders"></a>Kogumid müügitellimustel

USMF-i demoettevõtel on järgmine kogumihäälestus. Arvestage, et kõik tulu tuvastamise häälestused, nt tulugraafikute häälestus, on sellesse stsenaariumisse hõlmatud kaupadelt eemaldatud.

**Emakaup:** sülearvutikogum

- **Koostiskaup:** kaup 1000, kogus 1
- **Koostiskaup:** kaup S0021, kogus 1
- **Koostiskaup:** kaup Tugi, kogus 1

Koostiskaupade *baasmüügihind* on koostisosade häälestamise oluline osa. Baasmüügihind määratletakse kauba kiirkaardil **Müük**. Seda kasutatakse eraldamistegurina emakauba ühiku hinna eraldamisel koostiskaupadele. Kaubandusleppe müügihindu ei kasutata kunagi selleks otstarbeks.

Koostiskaupadele on määratletud järgmised baasmüügihinnad:

- **1000:** 1900.00 $
- **S0021:** 150.00 $
- **Tugi:** 500.00 $

Sisestatakse kliendi US-004 Cave Wholesales müügitellimus. Ainus sisestatud rida on sülearvuti kogumi kauba jaoks. Emarea ühiku vaikehinna saab võtta mitmest kohast, nt kaubandusleppest või baasmüügihinnast. Selles näites sisestati kauba hinnana käsitsi 2300 $.

[![Sülearvuti kogumi kaup müügitellimusel.](./media/bundle-01.png)](./media/bundle-01.png)

Kuna müügitellimus sisaldab kogumit, tuleb see kinnitada. Kinnitusdialoog näitab kogumi koostiskaupu.

[![Müügitellimuse kinnitamise dialoogiboks, mis näitab koostiskaupu.](./media/bundle-02.png)](./media/bundle-02.png)

Kuid prinditud kinnitusaruanne näitab ainult kogumi emakaupa, sest see aruanne on kliendile väljapoole suunatud dokument.

[![Kinnitusaruanne, mis näitab ainult emakaupa.](./media/bundle-03.png)](./media/bundle-03.png)

Pärast müügitellimuse kinnitamist näidatakse müügitellimusel endiselt emakaupa, kuid selle olekuks on nüüd **Tühistatud**. Lisaks jälgitakse netosummat väljal **Kogumi netosumma**. See summa on vajalik arve printimiseks, sest arvel näidatakse emakaupa, mitte koostiskaupu.

Koostiskaupade summa peab võrduma emakauba **Kogumi netosumma** väärtusega, kuna see väärtus on summa, mis esitatakse kliendile prinditud arvel. Arve pearaamatusse sisestatud summadele vastavuse tagamiseks on koostiskaupade muutmisvõimalused piiratud. Näiteks ei saa muuta kohta ja ladu, kuna need muudatused võivad kaubandusleppe alusel käivitada hinnamuutuse.

Emakauba real olev ühikuhind eraldatakse koostisosadele järgmiselt.

**Koostisosade baasmüügihinnad kokku:** 1900 $ + 500 $ + 150 $ = 2550 $

- **Koostisosa 1:** 2300 $ × (1900 ÷ 2550) = 1713.73 $
- **Koostisosa 2:** 2300 $ × (500 ÷ 2550) = 450.98 $
- **Koostisosa 3:** 2300 $ × (150 ÷ 2550) = 135.29 $

Koostisosade summa peab võrduma summaga 2300 $ ja nii see ongi (1713.73 $ + 450.98 $ + 135.29 $ = 2300 $).

Kui muuta on vaja kõiki koostiskaupu, saab emakauba eemaldada. Sel juhul eemaldatakse ka koostiskaubad. Emakauba saab seejärel uuesti lisada ning nõutavad muudatused saab teha enne müügitellimuse kinnitamist.

[![Kogumi kaup, mis sisaldab koostiskaupade muudatusi.](./media/bundle-04.png)](./media/bundle-04.png)

Kui müügitellimus on komplekteeritud ja pakitud, sisaldavad dokumendid ainult kogumi koostisosi. Saateleht ja arve peavad sisaldama kogu kogumit. Vastasel juhul ei saa neid sisestada. Võtame näiteks dialoogiboksi, mis näitab kolme koostiskaupa. Kui proovite ühte neist kustutada, kuvatakse tõrketeade sõnumiga, et kõik kogumis olevad tooted tuleb enne nende arveldamist lähetada.

Kogum tuleb lähetada ja arveldada täiskogumina. Kui te näiteks muudate kauba 1000 koguseks 4, kuid jätate muude koostiskaupade koguseks 5, ei saa saatelehte ja arvet sisestada.

Osalist summat saab lähetada ja arveldada ainult siis, kui vähendatakse kogumi kõigi koostisosade koguseid. Näiteks sisestatakse müügitellimusele sülearvuti kogumi kauba kogus 5. Kui müügitellimus on kinnitatud, näidatakse müügitellimusel kolme koostiskaupa ja iga kauba kogus on 5. Lähetamisel ja arveldamisel määratakse iga koostisosa koguseks vaikimisi 5. Kuid te saate kõigi kolme koostiskauba kogused vähendada väärtusele 3. Sel juhul lähetatakse ja arveldatakse kolm täiskogumit. Ülejäänud kaks kogumi kaupa (kõigi kolme koostiskauba koguseks 2) saab lähetada ja arveldada hiljem.

Viimaseks etapiks on müügitellimuse arveldamine. Arveldamisel kuvatakse arve dialoogiboksis koostiskaubad.

[![Arve dialoogiboks, mis näitab koostiskaupu.](./media/bundle-06.png)](./media/bundle-06.png)

Kuid prinditud arvel näidatakse ainult emakaup.
 
[![Prinditud arve, mis näitab ainult emakaupa.](./media/bundle-07.png)](./media/bundle-07.png)

Pärast sisestamist loodud arvete tööleht ei sisalda kogumi emakaupa, kuna selle kauba olek on **Tühistatud**.

[![Arvete tööleht, mis ei sisalda emakaupa.](./media/bundle-08.png)](./media/bundle-08.png)

On oluline, et arvete tööleht ei sisaldaks kogumi emakaupa, sest kõik pärast arve sisestamist tehtavad protsessid põhinevad sellel arvete töölehel. Näiteks kui loote toimingupaani vahekaardil **Müük** kreeditarve, sisaldab loodav kreeditarve koostiskaupu, kuid mitte emakaupa.

[![Kreeditarve, mis näitab koostiskaupu, kuid mitte emakaupa.](./media/bundle-09.png)](./media/bundle-09.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]