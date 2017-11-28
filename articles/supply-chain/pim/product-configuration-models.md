---
title: "Toote konfiguratsioonimudelite ülevaade"
description: "See artikkel määratleb toote konfiguratsioonimudeleid puudutavad tingimused ja mõisted. Toote konfiguratsioonimudelid võimaldavad luua üldise tootestruktuuri, mida saab kasutada üksiku toote paljude variantide konfigureerimiseks."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 4031
ms.assetid: 70b968e8-e550-4731-823d-d713b8910f7b
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 64f0a9a44b97a9980f8d1b76ff158f1ac9cbc114
ms.openlocfilehash: 6b896c28f475a8f827a1db1b6dd684b6ec64e872
ms.contentlocale: et-ee
ms.lasthandoff: 11/14/2017

---

# <a name="product-configuration-models-overview"></a>Toote konfiguratsioonimudelite ülevaade

[!include[banner](../includes/banner.md)]


See artikkel määratleb toote konfiguratsioonimudeleid puudutavad tingimused ja mõisted. Toote konfiguratsioonimudelid võimaldavad luua üldise tootestruktuuri, mida saab kasutada üksiku toote paljude variantide konfigureerimiseks.

Toote konfiguratsioonimudelid on loodud tähistama toote üldstruktuuri. Pärast toote konfiguratsioonimudeli seadistamist saate konfigureerida eristatava toote variandi, millel on kordumatu kooslus ja kordumatu protsess. Toote konfiguratsioonimudelid kasutavad erinevate tootevariantide seoste ja piirangute käsitlemisel nii deklaratiivseid piiranguid kui ka imperatiivseid arvutusi. Üksusi saab konfigureerida müügitellimustele, müügipakkumistele, ostutellimustele ja tootmistellimustele. Järgmine tabel kirjeldab tabeli piirangul põhinevaid tingimusi ja mõisteid.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Komponendid</td>
<td>Komponendid on toote konfiguratsioonimudeli peamised koosteüksused. Komponendid kuvatakse lehe <strong>Piirangupõhise toote konfiguratsioonimudeli üksikasjad</strong> puustruktuuris. Komponendid võivad sisaldada järgmisi elemente.
<ul>
<li>Atribuudid</li>
<li>Piirangud</li>
<li>Arvutamised</li>
<li>Alamkomponendid</li>
<li>Kasutaja nõuded</li>
<li>Koosluseread</li>
<li>Protsessitoimingud</li>
</ul></td>
</tr>
<tr class="even">
<td>Atribuudid</td>
<td>Atribuudid kirjeldavad kõiki toote konfiguratsioonimudeli funktsioone. Atribuutide abil saate määrata funktsioonid, mida saab valida eristatava toote konfigureerimisel. Atribuute kasutatakse piirangutes ja tingimustes. Kui atribuudid on loodud ja lisatud toote konfiguratsioonimudelile, viidatakse seotud atribuudi tüüpidele. Atribuudile saab seada vaikeväärtuse. Vaikeväärtust kasutatakse konfiguratsiooni kasutajaliideses (UI) toote konfiguratsioonimudeli konfigureerimisel. Saate määrata, kas atribuut on kohustuslik, kirjutuskaitstud või peidetud.
<ul>
<li><strong>Kohustuslik</strong> – väärtus tuleb seada atribuudile toote konfigureerimisel.</li>
<li><strong>Kirjutuskaitstud</strong> – atribuudi väärtus kuvatakse konfiguratsiooniseansi ajal, kuid seda ei saa muuta.</li>
<li><strong>Peidetud</strong> – atribuudi väärtus sisaldub piirangutes ja tingimustes, kuid ei kuvata konfiguratsiooniseansi käigus.</li>
</ul>
Samuti saate määrata atribuutide eeltingimuse. Kui tingimus on täidetud, tuleb väärtus sisestada kohustuslikule atribuudile. Tingimused on avaldised, mida tuleb täita atribuutidele, koosluseridadele ja protsessitoimingutele, mis kaasatakse toote konfiguratsioonimudelisse. Iga atribuut, mida on viidatud tingimuses, muutub kohustuslikuks. On soovitatav valida atribuudid kohustuslikuna vahekaardil <strong>Atribuudid</strong>. See muudab lihtsamaks kohustuslike atribuutide tuvastamise. Atribuudiväärtused on oluline osa tingimuste taaskasutamisest. Süsteem kasutab atribuudiväärtuseid määramaks, kas on olemas konfiguratsioon, mis vastab kasutaja tehtud valikutele konfiguratsiooniseansi käigus.</td>
</tr>
<tr class="odd">
<td>Atribuuditüübid</td>
<td>Atribuudi tüübid määravad andmetüübid atribuutidele, mida kasutatakse toote konfiguratsioonimudelis. Kasutatakse järgmisi atribuudi tüüpe.
<ul>
<li><strong>Täisarv</strong> vahemikuga või ilma</li>
<li><strong>Kümnendkoht</strong></li>
<li><strong>Tekst</strong> fikseeritud loendiga või ilma</li>
<li><strong>Kahendmuutuja</strong></li>
</ul>
Kui atribuudi tüüp on <strong>Kahendmuutuja</strong>, vahemikuga <strong>Täisarv</strong> või <strong>Tekst</strong>, on väärtuste kogum kättesaadav, kui toote konfiguratsioonimudel on seadistatud. <strong>Märkus.</strong> Tootekonfiguratsiooni lahendaja tunneb ära ainult järgmised atribuuditüübid: <strong>kahendmuutuja</strong>, fikseeritud loendiga <strong>tekst</strong> ja vahemikuga <strong>täisarv</strong>. Seetõttu saab ainult neid atribuudi tüüpe kasutada avaldise piirangutes ja tingimustes.</td>
</tr>
<tr class="even">
<td>Piirangud</td>
<td>Piirangud kirjeldavad tootemudeli konfiguratsiooni piiranguid. Piiranguid kasutatakse tagamaks, et toote konfigureerimisel valitakse ainult kehtivad väärtused. Piirangud saavad olla avaldise piirangud või tabeli piirangud.
<ul>
<li>Avaldise piiranguid saab kasutada ainult komponentidega, millega need seotud on. Komponendi avaldise piirangud võivad viidata komponentide alamkomponentide atribuutidele. Tootekonfiguratsiooni lahendajat kasutatakse piirangute lahendamiseks ja piirangute kirjutamisel tuleb kasutada lahendaja süntaksit. Lisateavet saate teema lingi kaudu avaldise piirangute ja tabeli piirangute kohta.</li>
<li>Tabeli piirangud tuleb määratleda enne nende rakendamist komponendile toote konfiguratsioonimudelis. Tabeli piirangud võivad olla kas kasutaja või süsteemi määratletud. Kasutaja määratletud tabeli piirang on teatud tüüpi maatriks, mida saab kasutada kombinatsioonide kogumi kirjeldamiseks atribuudiväärtustele, mis on määratletud atribuudi tüübiga. Näiteks kui toodetakse kõlareid, võib kasutaja määratletud tabeli piirangu maatriksil olla veerud kõlari viimistluse ja võre jaoks.</li>
</ul>
<strong>Näide</strong> Kõlareid on saadaval nelja viimistlusega: must, tamm, roosipuu ja valge. Kõlarite esivõre võib olla üks kolmest: must, metall või valge. Must viimistlus on saadaval kõigi võrede puhul, kuid muud viimistlused on piiratud teatud võredega. Järgmises tabelis on näide teabe kohta, mis kuvatakse vahekaardil <strong>Lubatud kombinatsioonid</strong> lehel <strong>Tabeli piirangu redigeerimine</strong>.
<table>
<thead>
<tr class="header">
<th>Kabinetiviimistlus</th>
<th>Esivõre</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Must</td>
<td>Must</td>
</tr>
<tr class="even">
<td>Must</td>
<td>Metall</td>
</tr>
<tr class="odd">
<td>Must</td>
<td>Valge</td>
</tr>
<tr class="even">
<td>Tamm</td>
<td>Must</td>
</tr>
<tr class="odd">
<td>Roosipuu</td>
<td>Valge</td>
</tr>
<tr class="even">
<td>Valge</td>
<td>Must</td>
</tr>
<tr class="odd">
<td>Valge</td>
<td>Valge</td>
</tr>
</tbody>
</table>
Süsteemi määratletud tabeli piirang tähistab tarkvara Finance and Operationsi tabeli atribuudi tüübi ja välja vahelist vastendust. Süsteemi määratud tabeli piirang seob atribuudi tüübi dünaamiliselt väljaga. Link lubab atribuudi toote konfiguratsioonimudelis, et kajastada välja andmeid Finance and Operationsi tabelis.</td>
</tr>
<tr class="odd">
<td>Arvestused</td>
<td>Arvutused kujutavad endast piirangute täiendust. Saate kasutada arvutust aritmeetilistes tehetes tüübiga <strong>Kümnendarv</strong> ja <strong>Täisarv</strong> või loogikatehete puhul, mis hõlmavad fikseeritud loendiga <strong>teksti</strong> ja <strong>kahendmuutuja</strong> tüüpi atribuute. Arvutusel on sihtatribuut, milles on arvutusavaldise tulemus. Arvutusavaldis koostatakse avaldiseredaktori abil.</td>
</tr>
<tr class="even">
<td>Alamkomponendid</td>
<td>Alamkomponendid kajastavad toote konfiguratsioonimudeli puustruktuuri. Saate kasutada alamkomponente toote konfiguratsioonimudeli struktuuri ehitamiseks. Alamkomponendid viitavad olemasolevatele komponentidele. Seega soodustab alamkomponentide kasutamine komponentide taaskasutust mitmes toote konfiguratsioonimudelis. Alamkomponendi lehel <strong>Koosluse rea üksikasjad</strong> saate valida alamkomponendi eristatava väärtuse. Teise võimalusena saate valida atribuudi, millele väärtus on toote konfiguratsioonimudeli seadistamisel valitud. Toote lisamiseks komponendi või alamkomponendina peate lehel<strong> Toote loomine</strong> määrama järgmised andmed.
<ul>
<li>Valige väljalt <strong>Toote tüüp</strong> väärtus <strong>Kaup</strong>.</li>
<li>Valige väljalt <strong>Toote alamtüüp</strong> väärtus <strong>Tooteetalon</strong>.</li>
<li>Valige väljalt <strong>Konfiguratsioonitehnoloogia</strong> väärtus <strong>Piirangupõhine konfiguratsioon</strong>.</li>
</ul>
Saate vaadata, kas väljastatud toodet saab kasutada komponendi või alamkomponendina vahekaardil <strong>Üldine</strong> lehel <strong>Väljastatud toote üksikasjad</strong>. Kui valik <strong>Piirangupõhine konfiguratsioon</strong> on väljal <strong>Konfiguratsioonitehnoloogia</strong> valitud, saab toodet kasutada komponendi või alamkomponendina. Alamkomponente saab peita nii, et neid ei kuvata kasutajale konfiguratsiooniseansi ajal. Atribuudid, alamkomponendid ja kasutajanõuded, mis on seotud alamkomponentidega, on ka peidetud.</td>
</tr>
<tr class="odd">
<td>Kasutaja nõuded</td>
<td>Kasutajanõuded tähistavad abstraktsiooni kasutajanõuete ning spetsiifiliste kompontide ja atribuutide vahel. Kasutajanõuet ei saa kaubaga vastendada. Näiteks klient soovib osta kodukinosüsteemi. Müügiesindaja võib küsida ruumi suuruse kohta, kuhu klient plaanib süsteemi paigaldada, et määrata, kui palju vatte on vaja. Selle näite puhul võib ruumi suurus olla kasutajanõue, mis aitab määrata sobivat atribuudi väärtust konkreetsele komponendile. Kasutajanõudeid saab peita nii, et neid ei kuvata kasutajale konfiguratsiooniseansi ajal. Atribuudid, alamkomponendid ja kasutajanõuded, mis on seotud kasutajanõuetega, on ka peidetud. Saate kirjutada tingimuse, et kontrollida, kas kasutajanõue võib olla peidetud. Peate kirjutama tingimuse, kasutades optimeerimise modelleerimiskeele (OML) süntaksit.</td>
</tr>
<tr class="even">
<td>Koosluseread</td>
<td>Koosluseread tähistavad komponentide üksikuid materjale toote konfiguratsioonimudelis. Lehel <strong>Koosluse rea üksikasjad</strong> on kõik üksused valimiseks valmis. Tingimuse saab lisada kooslusereale nii, et koosluseread, mis on valitud eristatava toote variandi jaoks, võivad varieeruda vastavalt kasutaja tehtud valikule toote konfiguratsioonimudeli seadistamisel. Tingimused on avaldised, mida tuleb täita atribuutidele, koosluseridadele ja protsessitoimingutele, mis kaasatakse toote konfiguratsioonimudelisse. Lehel <strong>Koosluse rea üksikasjad</strong> saate valida eraldi väärtuse. Teise võimalusena saate vastendada atribuudi, millele väärtus on toote konfiguratsioonimudeli seadistamisel valitud.</td>
</tr>
<tr class="odd">
<td>Protsessitoimingud</td>
<td>Lehel <strong>Protsessitoimingu üksikasjad</strong> saate valida eraldi väärtuse. Teise võimalusena saate vastendada atribuudi, millele väärtus on toote konfiguratsioonimudeli seadistamisel valitud. Tingimused kirjutatakse nagu avaldise piiranguid. Tingimused on avaldised, mida tuleb täita atribuutidele, koosluseridadele ja protsessitoimingutele, mis kaasatakse toote konfiguratsioonimudelisse.</td>
</tr>
</tbody>
</table>






