---
title: Kollektsioonide halduse võtmekontseptsioonid
description: Selles teemas määratletakse kollektsioonide halduse võtmekontseptsioone.
author: JodiChristiansen
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f1e6932740c33ae418ac633623680eda6af7a592
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858520"
---
# <a name="collections-management-key-concepts"></a>Kollektsioonide halduse võtmekontseptsioonid

[!include [banner](../includes/banner.md)]

Enne sissenõuete seadistamise alustamist või nendega töötamist peaksite teadma järgmisi põhimõtteid.

- Kliendi aegumise hetktõmmised sisaldavad aegunud saldoteavet teatud ajahetkel.
- Sissenõuete kliendikaustad aitavad teil oma tööd korraldada.
- Inkassaatoritel võivad olla oma kliendikaustad.
- Loendilehtedel korraldatakse sissenõuete kliendid, tegevused ja juhtumid.
- Kogu kliendi sissenõuete teave on ühel lehel ja saate tegevusi sellelt lehelt teha.
- Intresside ja tasude puhul saab loobumise, ennistamise või tühistamise teha ühe etapina.
- Mahakandmiskanded saab luua ühe etapina.
- Ebapiisavate vahendite (NSF) maksed saab töödelda ühe etapina.

See artikkel kirjeldab iga mõiste.

## <a name="customer-aging-snapshots"></a>Kliendi aegumise hetktõmmised 

Aegumise hetktõmmis sisaldab kliendi arvutatud aegunud saldosid kindlal ajahetkel. See teave kuvatakse loendilehel **Aegunud saldod** ja lehel **Sissenõuded**. Enne kui saate kollektsioonide loendi lehtede (**Aegunud saldod**, **Sissenõudetegevused** ja **Sissenõuete juhtumid**) andmeid vaadata, tuleb luua aegumise hetketõmmis.

Iga kliendi puhul sisaldab aegumise hetktõmmis aegumise hetktõmmise päist ja üksikasjalikke kirjeid, mis vastavad igale aegumisperioodile aegumisperioodi definitsioonis.

Aegumise hetktõmmise päis sisaldab tasumisele kuuluvat kogusummat, krediidilimiiti, saatelehe summat, müügitellimuse summat, vaidlustatud kannete arvu ja kliendikonto vaidlustatud kannete kogusummat. Kõik kliendi kanded kaasatakse nende summade arvutusse. Tasumisele kuuluv kogusumma, krediidilimiit, saatelehe summa ja müügitellimuse summa kuvatakse lehe **Krediiditeave** kiirinfos lehel **Sissenõuded**.

Aegumise hetktõmmise üksikasjalik kirje luuakse iga aegumisperioodi kohta aegumisperioodi definitsioonis. Iga üksikasjade kirje sisaldab aegumisperioodi ID-d ja aegumisperioodi jäävate kuupäevadega kannete kogusummat. Kanded määratakse aegumisperioodile, näiteks 30 päeva üle tähtaja. Kuupäev on seotud kuupäeva **Aegumise kuupäev** väärtusega, mille määratlete aegumise hetketõmmist luues. See teave kuvatakse loendilehel **Aegunud saldod** ja lehe **Sissenõuded** kiirinfos **Aegunud saldod**.

## <a name="collections-customer-pools"></a> Sissenõuete kliendikaustad 

Kliendikaustad on päringud, mis määratlevad kliendi kirjete grupi. Saate kasutada neid grupeeritud kirjeid, et vaadata teavet kaasatud kliendikontode kohta ja hallata nende sissenõudmiste ja aegumiste protsesse. Kliendikaustadega saate filtreerida teavet sissenõuete loendilehtedel. Nendega saate ka filtreerida kliendikontosid, mis kaasatakse aegumise hetktõmmiste loomisel.

## <a name="collections-agents"></a>Inkassaatorid

Vaikimisi saavad kasutajad vaadata sissenõuete loendilehtedel kogu klienditeavet. Inkassaatorikirjete abil saate määrata kliendikaustad, mis on saadaval sissenõuete loendilehtedel ja lehel **Sissenõuded** oleva teabe filtreerimiseks.

Inkassaatorid teevad koostööd klientidega, et makseid kogutaks õigeaegselt. Nad on töötajad, kes on määratud kasutajale lehel **Kasutajate seadistus**.

## <a name="collections-list-pages"></a> Sissenõuete loendilehed 

Järgmiste loendilehtede abil saate sissenõuete teavet korraldada.

- **Aegunud saldod** – loendilehe veergudel kuvatakse kliendisaldod ja aegunud summad aegumisperioodi järgi. See teave salvestatakse aegumise hetktõmmisesse. Aegumisperioodid on määratud kasutatava aegumisperioodi definitsiooniga. Aegumisperioodi definitsioon võetakse kliendikaustast, kui see on kliendikausta päringule määratletud. Kui kliendikaustal ei ole aegumisperioodi definitsiooni, kasutatakse lehel **Müügireskontro parameetrid** määratud aegumisperioodi vaikedefinitsiooni. Kui ühtegi vaikimisi aegumisperioodi definitsiooni ei ole määratud, kasutatakse esimest aegumisperioodi määratlust lehel **Aegumisperioodi määratlused**.
- **Sissenõudmistegevused** – loendilehe veerud, kus kuvatakse sissenõuete tegevustena määratletud tegevused. Need tegevused on loodud lehel **Sissenõuded**. Kasutate tegevusi, et jälgida sissenõuetega seoses tehtavat tööd.
- **Sissenõuete juhtumid** – loendilehe veerud, kus kuvatakse teavet juhtumite kohta, millel on juhtumikategooria juhtumitüübiga **Sissenõuded**.

### <a name="aging-snapshots"></a>Aegumise hetktõmmised

Enne kui saate teavet loendilehtedel Sissenõuded vaadata, tuleb luua aegumise hetktõmmis. Teavet kuvatakse vaid püsiklientidele, kelle jaoks on aegumise hetktõmmis loodud. Loendilehel kuvatavaid kirjeid saab täiendavalt filtreerida järgmiselt.

- Vaikimisi on kasutajatel juurdepääs kõigile klientidele, kel on aegumise hetktõmmis.
- Kliendikaustade olemasolul peab kasutaja olema seadistatud inkasaatorina, et kasutada kaustu sissenõuete loendilehtedel oleva teabe filtreerimiseks. Teave on piiratud klientidega, kes kuuluvad valitud kliendikausta.
- Kui kasutaja on seadistatud inkassaatorina, on sissenõudmiste loendilehel saadaval ainult selle inkassaatori jaoks valitud kaustad. Kui inkassaatori puhul on lehel **Inkassaator** märgitud ruut **Luba inkassaatoril vaadata kõiki kliendikaustu**, on kõik kaustad selle inkassaatori jaoks saadaval.

## <a name="collections-page"></a> Leht Sissenõuded

Lehel **Sissenõuded** saate vaadata ja hallata kliendi sissenõudeteavet, -tegevusi ja -juhtumeid ning nendega tegevusi teha.

Lehe ülemises jaotises kuvatakse valitud kliendi juhtumid, keskmine osa näitab kliendi kandeid ja alumises jaotises kuvatakse kliendi tegevused. Saate luua sissenõudejuhtumid, et jälgida sissenõudeteavet ühe või mitme kande ja tegevuse kohta. Ülemise ja alumise jaotise teavet saab juhtumi alusel filtreerida.

Kiirinfodes kuvatakse valitud kliendi aegunud saldod ja krediidilimiit. See teave salvestatakse aegumise hetktõmmisesse. Vajaduse korral saate aegumise hetktõmmist värskendada.

Toimingupaanil on nupud, mis lasevad vaadata valitud kliendi, juhtumi, kande või tegevusega seotud teavet. Saate teha ka üldisi tegevusi, näiteks muuta kande sissenõuete olekut, saata meile oma meiliteenuse pakkuja integratsiooni kaudu, anda klientidele hüvitisi, töödelda NSF-makseid ja kanda sissenõudmatuid saldosid maha.

## <a name="waiving-reinstating-or-reversing-interest-and-fees"></a>Intressi ja tasude nõudest loobumine, selle ennistamine või tühistamine

Saate loobuda täielike viivisearvete või tasude ja kandeintresside, mis on osa viivisearvest, nõudest, neid ennistada või tühistada. Vahekaardil **Sissenõudmine** lehe **Kõik kliendid** toimingupaanil valige **Viivisearve**, **Kandeintress** või **Tasu**.

Need korrigeerimised mõjutavad ainult viivisearveid ning neis sisalduvat intressi ja tasusid. Teavet selle kohta, kuidas maha maha kirjutada kõik tasud, mis klient võlgneb, [vt selle](#creating-write-off-transactions) artikli jaotist Mahakandmiskannete loomine.

Lisateabe saamiseks vt Vahemikuga viivisekoodi loomine ja Protsessiviivis.

## <a name="creating-write-off-transactions"></a>Mahakandmiskannete loomine

Saate halvad võlad maha kanda, valides suvandi **Mahakandmine** lehel **Sissenõudmised** ja sissenõudmiste loendi lehtedel.

Kliendi kannete mahakandmisel märgitakse kliendi kõik kanded automaatselt tasakaalustamiseks. Mahakantav summa sõltub märgitud kannete netosummast. Mahakandmise kanne luuakse päevaraamatus ja see võib sisaldada kuni kolme tüüpi tööleheridu.

- Esimest tüüpi tööleherida sisaldab kliendi mahakandmiskirjet. Kui märgitud kanded sisaldavad mitut valuutakoodi, dimensiooni ja sisestusreeglite kombinatsiooni, luuakse iga kombinatsiooni kohta eraldi tööleherida.
- Teist tüüpi tööleherida sisaldab pearaamatu mahakandmiskirjet. Kui märgitud kanded sisaldavad mitut valuutakoodi, dimensiooni ja sisestusreeglite kombinatsiooni, luuakse iga kombinatsiooni kohta eraldi tööleherida.
- Kolmandat tüüpi tööleherida sisaldab pearaamatu mahakandmisteavet käibemaksu kohta. See tööleherida luuakse ainult siis, kui lehel **Müügireskontro parameetrid** on märgitud ruut **Eraldi käibemaks**. Kui märgitud kanded sisaldavad mitut tasumisele kuuluva käibemaksu kontod, dimensioonid ja käibemaksukoodide kombinatsioonid, luuakse iga kombinatsiooni kohta eraldi tööleherida. Mahakandmiskanne luuakse kandevaluutas. Lisateabe saamiseks vt Kliendi jaoks mahakandmise töölehe loomine

## <a name="process-nsf-payments"></a>NSF-maksete töötlemine

Saate töödelda NSF-makseid, klõpsates lehel **Sissenõuded** nuppu **NSF-makse**. Selle nupu valimisel tühistatakse makse. Kui kliendile kehtib NSF-tasu, luuakse maksetöölehel tasukanne. Tasu summa põhineb automaatsete tasude seadistusel. Automaatsed tasud, mida kohaldatakse NSF-maksetele, on määratud tasude grupis, mis on valitud seotud pangakonto lehel **Pangakontod**.

## <a name="additional-resources"></a>Lisaressursid

[Kliendi krediidihalduse parameetrite seadistus](./cm-credit-mgmt-setup.md)

[Kliendi krediidihalduse andmete seadistus](./cm-setup-information.md)

[Kliendile krediidihalduse andmete lisamine](./cm-add-credit-mgmt-information-customer.md)

[Kliendi krediidigrupid](./cm-customer-credit-groups.md)

[Kliendi kreeditilimiidi korrigeerimised](./cm-credit-limit-adjustments.md)

[Müügitellimuste krediidi ootelolekud](./cm-sales-order-credit-holds.md)

[Perioodilised kliendi krediidihalduse ülesanded](./cm-periodic-tasks.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
