---
title: Kulutuste haldamise parameetrid
description: "Järgmised parameetrid juhivad käitumist kuluhalduses."
author: KimANelson
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8ca9e80d6d2b87fcdd10ebb9d32bd0a2b2d15614
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="expense-management-parameters"></a>Kulutuste haldamise parameetrid
-----------------------------

Parameetrid juhivad üldist käitumist kuluhalduses.

### <a name="general"></a>Üldine

| **Väli**                                                | **Kirjeldus**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Läbisõidu standardmäär**                             | Sisestage läbisõidukulude korvamismäär. Määr korrutatakse kulusse sisestatud läbisõiduga, et arvutada reisikulude puhul korvatav summa.                       |
|**Isiklike kulude maksja**                             | Saate valida, kes vastutab isiklikeks liigitatud krediitkaardikannete summade tasumise eest.                                                                                                     |
|**Kuva kogu kuluaruanne tagasijälgimises.**               | Valige see suvand, et kuvada kuluaruande puhul kõik kulud, kui vaadatakse kuluaruande sisestamisel loodud kindla kande algdokumendi üksikasju.              |
|**Reisi eelautoriseerimine on kohustuslik.**                 | Valige see suvand, et nõuda reisiplaani esitamist ja kinnitamist, enne kui töötaja saab kuluaruande esitada.                                                                    |
|**Luba jaotuste redigeerimine enne sisestamist.**            | Saate valida, kas kuluaruande jaotusi saab enne sisestamist redigeerida.                                                                                                                 |
|**Kuluhalduse poliitikate hindamine**                     | Saate valida, millal kulusid hinnatakse, et teha kindlaks, kas kulupoliitikat on rikutud. Kulusid saab kontrollida rikkumiste suhtes kulukande sisestamisel ja salvestamisel või kulu esitamisel kinnitamiseks. Kulurea salvestamisel kontrollitakse kohustuslike kviitungite poliitikareegleid.                   |
|**Luba kontsernisisesed kuluread**                         | Saate valida, kas lubada kuluaruandesse teiste juriidiliste isikute kulude sisestamine.                                                                                                          |
|**Luba krediitkaardikulude vahetuskursi redigeerimine** | Valige see suvand, et lubada kasutajal redigeerida imporditud krediitkaardikulude vahetuskurssi.                                                                        |
|**Mitmetasandilise hierarhia kuvatavad väljad**                  | Saate valida, millised kinnitaja väljad kuvatakse, kui kuluaruande töövoo määramise tüübiks on valitud hierarhia ja hierarhia valik on määratud kasutama kulude mitmetasandilist kinnitushierarhiat. Kui töövoo jaoks kasutatakse mitmetasandilist kinnitushierarhiat, kuvatakse valitud väljad kuluaruandes ja need on redigeeritavad. |
|**Töövõtja krediitkaardi numbri sisestamine (2017. aasta juulivärskendus)**     | Saate valida, kas töötaja puhul saab lehel **Krediitkaardid** väljale **Kaardi ID** sisestada ja salvestada 15- või 16-kohalise numbri.                                                                          |

### <a name="financial"></a>Finants

| **Väli**                                                            | **Kirjeldus**     |
|----------------------------------------------------------------------|------------------------------------|
|**Pearaamatu päevase töölehe nimi**                                         | Saate valida pearaamatu töölehe nime, kuhu sisestatakse kinnitatud kuluaruanded.            |
|**Luba maksu korvamine kuludest**                                  | Valige see suvand kulu maksu korvamise lubamiseks sobilike kulude puhul. Seda suvandit ei saa lubada, kui USA käibemaksu ja kasutusmaksu reeglid on lubatud.      |
|**Sisesta avansimaksed kohe**                                     | Valige see suvand, et sisestada kinnitatud avansimaksed kohe, kui maksmise ja ülekande protsess on lõpule viidud. Kui see suvand pole valitud, loob maksmise ja ülekande protsess sisestamata pearaamatu töölehe. |
|**Paranda aruandluskuupäev sisestamise ajal**                             | Valige see suvand aruandluskuupäeva värskendamiseks kulude sisestamisel, kui praegune periood on ootel või suletud. Aruandluskuupäevaks määratakse järgmine avatud periood.   |
|**Luba kannete rühmitamine makseviisis määratud vastaskonto alusel**      | Valige see suvand kuluaruande kulukannete kokkuvõtte tegemiseks kulude makseviisis määratud vastaskonto põhjal.   
|**Maks on kaasatud**                                                   | Valige see suvand käibemaksu vaikimisi kaasamiseks kulusummasse.             |
|**Vabasta pandiõigused reisiplaanide sulgemisel**            | Valige see suvand pandiõiguste vahendite vabastamiseks kinnitatud reisiplaani sulgemisel.                                                                                   |
|**Luba reisiplaani edastamine eelarve ülekulu korra eelarveregistri ja projekti eelarve puhul** | Valige see suvand, et lubada töötajatel esitada kinnitamiseks reisiplaane, mis ületavad kas eelarveregistris määratud lubatud eelarvet või projekti puhul lubatud eelarvet.            |
|**Luba kuluaruande edastamine eelarve ülekulu korra eelarveregistri ja projekti eelarve puhul**    | Valige see suvand, et lubada töötajatel esitada kinnitamiseks kuluaruandeid, mis ületavad kas eelarveregistris määratud lubatud eelarvet või projekti puhul lubatud eelarvet.                |
|**Luba kuluaruande heakskiitmine eelarve ülekulu korral ainult eelarveregistri puhul**                | Valige see suvand, et lubada kinnitajatel kinnitada kuluaruandeid, mis ületavad eelarveregistris määratud lubatud eelarvet.                                                                       |

### <a name="per-diem"></a>Päevaraha

| **Väli**                             | **Kirjeldus**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Päevaraha minimaalne tundide arv**           | Saate sisestada töötundide minimaalse vaikearvu, mille töötaja peab päevas töötama, et saada päevaraha reisimisega seotud kulude jaoks.  Seda väärtust kasutatakse vaikeväärtusena ainult päevarahamäära kihtide välja Miinimumtunnid puhul.                                                                                      |
|**Toitlustusprotsent**                          | Saate sisestada päevaraha toitlustuse vaikeprotsendi, mida kasutati reisiga seotud kulu esimesel ja viimasel päeval, kui välja **Arvuta toitlustusega seotud vähendamine** sätteks on valitud kas **Söögikordade tüüp päevas** või **Söögikordade arv päevas**. Esimese ja viimase päeva tööpäev võib olla lühem kui tavaline tööpäev. Seetõttu võib erineda nende päevade päevaraha summa tavasummast. Kui protsendiks on määratud 0, on esimese ja viimase päeva mahaarvamised 0,00. |
|**Hotelliprotsent**                        | Saate sisestada päevaraha hotellide vaikeprotsendi, mida kasutatakse reisiga seotud kulu esimesel ja viimasel päeval. Esimese ja viimase päeva tööpäev võib olla lühem kui tavaline tööpäev. Seetõttu võib erineda nende päevade päevaraha summa tavasummast. Kui protsendiks on määratud 0, on esimese ja viimase päeva mahaarvamised 0,00.                                              |
|**Muud protsendid**                        | Saate sisestada päevaraha mitmesuguste kulude vaikeprotsendi, mida kasutatakse reisiga seotud kulu esimesel ja viimasel päeval. Esimese ja viimase päeva tööpäev võib olla lühem kui tavaline tööpäev. Seetõttu võib erineda nende päevade päevaraha summa tavasummast. Kui protsendiks on määratud 0, on esimese ja viimase päeva mahaarvamised 0,00.                                                                                                     |
|**Hommikusöökide vähendamise protsent** | Saate sisestada summa, mille võrra päevaraha hommikusöökide arvelt vähendatakse. Näiteks kui töötaja saab tasuta hommikusööki, võite vähendada päevaraha summat 10 protsendi võrra.                               |
|**Lõunasöögi vähendamise protsent**    | Saate sisestada summa, mille võrra päevaraha lõunasöökide arvelt vähendatakse. Näiteks kui töötaja saab tasuta lõunasööki, võite vähendada päevaraha summat 15 protsendi võrra.                                       |
|**Õhtusöökide vähendamise protsent**   | Saate sisestada summa, mille võrra päevaraha õhtusöökide arvelt vähendatakse. Näiteks kui töötaja saab tasuta õhtusööki, võite vähendada päevaraha summat 25 protsendi võrra.                                     |
|**Arvuta toitlustamisega seotud kulude vähendamine**         | Saate valida, kuidas süsteem peaks arvutama päevaraha toitlustamisega seotud vähendamise, valides, kas vähendamine põhineb toitlustustüübil reisi või päeva kohta või iga päev lubatud toidukordade arvul.|
|**Päevaraha ümardamine**                  | Saate valida päevaraha kulude puhul kasutatava ümardamise tüübi. Tavalise ümardamise valimisel ümardatakse päevarahade kulu summas 0,50 ülespoole summani 1,00 ja päevarahade kulu, mille summa on väiksem kui 0,50, ümardatakse allapoole kuni summani 0,00.                                                                                              |
|**Võta päevaraha arvutamise aluseks**         | Saate valida, kas päevaraha summa aluseks on kalendripäev või 24-tunnine periood.       |

### <a name="fax-cover-pages"></a>Faksi tiitellehed

| **Väli**                      | **Kirjeldus**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Juhised**                   | Saate sisestada juhised, mida töötajad peavad järgima, kui nad loovad tiitellehe faksile, mida kasutatakse kuluaruandega seotud kviitungite saatmiseks. Klõpsake nuppu **Tõlked**, et sisestada keelekohane tekst, mis kuvatakse olenevalt kasutaja keelest. |
|**Kasutaja ID (vöötkooditeave)** | Valige see suvand, et talletada töötaja kordumatu identifikaator faksi tiitellehel kasutatavasse vöötkoodi.                 |
|**Vöötkood**                      | Saate valida faksi tiitellehel kasutatava vöötkoodi. Kuluhalduse puhul toetatakse vöötkoode 39 ja 128.               |

### <a name="anti-corruption"></a>Korruptsioonivastane

| **Väli**                             | **Kirjeldus**      |
|---------------------------------------|------------------------------------------------------------------------|
|**Korruptsioonivastase atesteerimise kuvamine**   | Valige see suvand, et kuvada uue kuluaruande loomisel korruptsioonivastane tekst. Seejärel saate lubada konkreetsed kulukategooriad, mis nõuavad kuluaruandes korruptsioonivastase atesteerimise valimist. Näiteks võib riigiametniku kuluga seotud kingikategooria nõuda töötajalt kinnitust, et kulu vastab ettevõtte poliitikale riigiametnike kohta. |
|**Korruptsioonivastane sõnum edastajale** | Saate sisestada teksti, mis kuvatakse töötajale uue kuluaruande loomisel. Klõpsake nuppu **Tõlked**, et sisestada keelekohane tekst, mis kuvatakse olenevalt kasutaja keelest.         |
|**Korruptsioonivastane sõnum kinnitajale**  | Saate sisestada teksti, mis kuvatakse kinnitajale uue kuluaruande loomisel. Klõpsake nuppu **Tõlked**, et sisestada keelekohane tekst, mis kuvatakse olenevalt kasutaja keelest.        |

