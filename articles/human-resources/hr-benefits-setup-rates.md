---
title: Määrade konfigureerimine
description: Rakenduse Microsoft Dynamics 365 Human Resources määrad määratlevad, kui suure panuse tööandjad ja töövõtjad soodustusele annavad.
author: andreabichsel
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85cf561828aa8ef9d80df31436f473b29406e2fd
ms.sourcegitcommit: 08797bc43e93ea05711c5a70dd7cdb82cada667a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/13/2021
ms.locfileid: "6558341"
---
# <a name="configure-rates"></a>Määrade konfigureerimine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Määrad määratlevad, kui suure panuse tööandjad ja töövõtjad soodustusele annavad. Väärtus võib konfiguratsioonist olenevalt olla summa või teatud arv paindlikku krediiti.

Kasutage määrasid, et määratleda, kui palju töövõtjad ja tööandjad iga soodustuse eest maksavad, võttes aluseks mitu tegurit. Katvuse määrad on kuupäevapõhised, nii et saate säilitada määrade kohta ajaloolise kirje. 

## <a name="set-up-rates"></a>Määrade seadistamine

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Määrad**.

2. Valige suvand **Uus**.

3. Määrake järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Kurss** | Kordumatu nimi, mis tuvastab soodustuse määra. |
   | **Kirjeldus** | Soodustuse määra kirjeldus. |
   | **Jõustunud** | Kursi jõustumise kuupäev. Praegune süsteemikuupäev on vaikeväärtus. See kuupäev peab olema soodustusperioodil või enne seda. Hea tava on määrata see kuupäev hüvitiste plaani kuupäevaks. |
   | **Aegumine** | Määra lõpukuupäev. Vaikeväärtus on 12/31/2154 (mis tähendab mitte kunagi). |
   | **Kasuta järke** |  Kasutage seda välja, kui teil on loogika, mida tuleb kasutada määra määramiseks. Näiteks kui määr peab põhinema vanusel, valige siin väärtus. Valige **üheastmeline** üheastmelise hüvitise määra jaoks või **kaheastmeline** kaheastmelise hüvitise määra jaoks. Topelttaseme näide on sool ja vanusel põhinev tase. Pärast väärtuse valimist valige **Toimingud** ja seejärel valige **Järgu määrad**. Kui teil on fikseeritud määr, mis ei muutu, jätke see väli tühjaks. |
   | **Makse sagedus** | Täpsustage, kui sageli tuleks hüvitise pakkujale maksta hüvitise määra. Selles teemas hiljem kirjeldatud lehele sisestatud määrad põhinevad siin määratud maksesagedusel. Kui sisestate sellele väljale näiteks **igakuine** ja sisestate töötaja määraks **100 $**, siis eeldatakse, et soodustus maksab töötajale $100 kuu kohta. Töötajale võidakse siiski maksta kaks korda kuus, võttes aluseks töötajakirjes määratud hüvitiste maksesageduse. Sellisel juhul on töötaja iseteenindusse sisselogimisel summa, mille nad maksavad, 50 dollarit, kuna töötaja iseteeninduse näidatud määr põhineb töötaja maksesagedusel. |
   | **Maksesageduse määra ümardamine** | Määra ümardamise meetodid on: standardne, kärbitud, tavaline, allapoole ja ümardamine üles. </br></br><ul><li>**Standardne** – ümardage alati üles. Näiteks 10,611 ümardatakse 10,62-ni. -10,231 ümardatakse -10,23-ni. </li><li>**Kärbitud** - alati ümardatakse alla. Näiteks 10,619 ümardatakse 10,61-ni. -10,231 ümardatakse -10,24-ni. </li><li>**Tavaline** – kümnendarvud, mis lõppevad 5 või suurema arvuga, ümardavad nullist suuremaks. Kümnendarvud, mis lõppevad 4 või väiksema arvuga, ümardatakse nulli poole. Näiteks 10,615 ümardatakse 10,62-ni. -10,235 ümardatakse -10,24-ni. 10,614 ümardatakse 10,61-ni. -10,234 ümardatakse -10,23-ni. </li><li>**Allapoole** – ümardage nulli suunas. Näiteks 10,619 ümardatakse 10,61-ni. -10,231 ümardatakse -10,23-ni. </li><li>**Ümardamine üles** – ümardatakse nullist eemale. Näiteks 10,619 ümardatakse 10,62-ni. -10,231 ümardatakse -10,24-ni. |
   | **Mittesuitsetaja töövõtja summa** | Summa, mille hüvitise pakkuja küsib mittesuitsetava töövõtja eest. See on summa, mille töövõtja maksab soodustuse pakkujale, ja mis peaks põhinema määra seadistuse maksesagedusel. |
   | **Mittesuitsetaja tööandja summa** | Summa, mille hüvitise pakkuja küsib mittesuitsetava töövõtja eest. See on summa, mille töövõtja maksab soodustuse pakkujale, ja see peaks põhinema määra seadistuse maksesagedusel. |
   | **Suitsetaja töövõtja summa** | Summa, mille hüvitise pakkuja küsib suitsetava töövõtja eest. See on summa, mille töövõtja maksab soodustuse pakkujale, ja mis peaks põhinema määra seadistuse maksesagedusel. |
   | **Suitsetaja tööandja summa** | Summa, mille hüvitise pakkuja küsib suitsetava töövõtja eest. See on summa, mille töövõtja maksab soodustuse pakkujale, ja mis peaks põhinema määra seadistuse maksesagedusel. |
   | **Haldussumma** | Kolmandast poolest haldaja küsitav haldussumma. See on summa, mille töövõtja maksab kolmandast poolest haldajale, ja see peaks põhinema määra seadistuse maksesagedusel. |
   | **Paindlik krediidimäär** | Soodustusele kuluv paindliku krediidi hulk. Seda kohaldatakse ainult määradele, mis on paidliku krediidi programmidega seostatud soodustuse plaanide jaoks. Kui kasutate tasemete määrasid, määratletakse paidliku krediidi määr asukohas Tegevused > Taseme määrad. |
   | **Jõustumiskuupäeva muutmine** | Soodustuse määra muudatuse jõustumise kuupäev. Süsteem muudab automaatselt soodustuste määra ja uuendab kõiki selle määraga seotud soodustuse plaane, kui käitate määra muutmise uuendamise töötluse. Ärge seadke seda kuupäeva, kui te ei soovi, et süsteem uuendaks selle määra põhjal töövõtja soodustuse plaane automaatselt. See on tavaliselt reserveeritud automaatsele tulevase määra muutmise töötlusele. Muudatuse jõustumiskuupäev peab jääma soodustuse määra ja aegumiskuupäeva piiresse. |
   | **Määra muutmine on lõpule viidud** | Kui soodustuse määra muudatused on määra muutuse uuendamise protsessi raames lõpule viidud, siis märgistatakse **määra muutuse lõpule viimise** märkeruut automaatselt. |

4. Soodustuse määra häälestuse muudatuste jälgimiseks ja säilitamiseks valige suvand **Tegevused** ning seejärel valige suvand **Versioonide haldamine**.

5. Valige käsk **Salvesta**. 

## <a name="set-up-tier-rates"></a>Taseme määrade seadistamine

Kui määr varieerub sõltuvalt erinevatest teguritest, saate kasutada määrade seadistamisel taseme määrasid. Näiteks saate konfigureerida taseme määrad nii, et kui teie vanus on kuni 34,99, siis mittesuitsetaja summa on 2. Kui teie vanus on kuni 39,99, siis mittesuitsetaja summa on 3.

Saate kasutada ka topelttasemeid. Kui valite suvandi **Topelttase** väärtuse **Kasuta tasemeid** jaoks vormil **Määra seadistamine**, saate määratleda määrad kahe dimensiooni põhjal. Näiteks saate konfigureerida topelttaseme süsteemi nii, et kui olete meesterahvas ja teie vanus on kuni 34,99, siis mittesuitsetaja summa on 2. Kui olete meesterahvas ja teie vanus on kuni 39,99, siis mittesuitsetaja summa on 3. Kui olete naisterahvas ja teie vanus on kuni 34,99, siis mittesuitsetaja summa on 1,8. Kui olete naisterahvas ja teie vanus on kuni 39,99, siis mittesuitsetaja summa on 2,8.

> [!IMPORTANT]
> Töötajakirje **isikuandmete** suvandi abil saate määrata, kas töötaja on suitsetaja. Kui töötaja kajastatakse suitsetajana, kasutatakse suitsetaja määra. (Suitsetaja märget ei näidata töötajale kunagi.)
   
1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Määrad**.

2. Valige loendist üks või mitu määra, valige suvand **Tegevused** ja seejärel valige suvand **Taseme määrad**.

3. Valige suvand **Uus**.

3. Määrake järgmiste väljade väärtused.

   | Field | Kirjeldus |
   | --- | --- | 
   | **Kirjeldus** | Välja **Kirjeldus** väärtus rakendatakse määra seadistamise kirje kirjeldusest. See aitab teil tuvastada, milliste määra seadistustega taseme määrad on ühendatud. |
   | **Järgukood** | Valige taseme kood. Taseme koodid määratletakse vormil Taseme koodid. Süsteem kuvab automaatselt taseme koodide kirjelduse vasakpoolses ruudustikus. |
   | **Järgu tüüp** | Määrab, millist välja tuleks kasutada taseme määra arvutamise protsessi valiku kriteeriumina. Näide:</br></br><ul><li>Kui kasutatakse suvandit **Vanus**, kasutab süsteem soodustuse määra arvutamise protsessis töövõtja sünnikuupäeva.</li><li>Kui kasutatakse suvandit **Palk**, kasutab süsteem soodustuse määra arvutamise protsessis aastast soodustuse palka.</li><li>Kui kasutatakse suvandit **Töö tüüp**, kasutab süsteem töövõtja praeguse aktiivse ametikoha kirjet, et määrata töö tüüp ametikohaga ühendatud töö kirje alusel.</li></ul></br></br>Taseme tüübid on **Vanus**, **Palk**, **Füüsiline**, **Sugu**, **Täistööaja vaste**, **Töö tüüp**, **Hüvituspiirkond** ja **Tase**. | 
   | **Tase** | Väärtus, mida kasutatakse soodustuse arvutamise protsessi ajal koos taseme tüübiga. Näide:</br></br><ul><li>Kui taseme tüüp on **Vanus**, on see vanuse väärtus.</li><li>Kui taseme tüüp on **Palk**, on see palga summa.</li><li> Kui taseme tüüp on **Töö tüüp**, on see töö tüüp.</li></ul></br></br>Taseme tüübi **Vanus** või **Palk** puhul tähistab välja **Tase** väärtus taseme ülemist piiri. Kui taseme tüüp on **Töö tüüp**, kasutab süsteem taseme määra valimisel täpse vaste lähenemisviisi. |
   | **Arvutuse tüüp** | Määrab, kuidas kasutada summat arvutussumma väljal ja millist matemaatilist arvutust vajadusel teha. Kui arvutamise tüüp on kindel summa, kasutab süsteem summa väljasid samal kujul. Kui arvutamise tüüp on palga või katvuse summa kohta, kasutab süsteem matemaatilises arvutuses arvutuse summat ja arvutuse suunda.</br></br>Kui arvutamise tüüp on palga summa kohta, kasutab süsteem järgmist matemaatilist võrrandit:</br></br>aastane soodustuse palk jagatud arvutuse summaga (ümardatud üles- või allapoole), korrutatud töövõtja või tööandja suitsetaja või mittesuitsetaja summadega.</br></br>Kui arvutamise tüüp on katvuse summa kohta, kasutab süsteem järgmist matemaatilist võrrandit:</br></br>katvuse summa jagatud arvutuse summaga (ümardatud üles- või allapoole), korrutatud töövõtja või tööandja suitsetaja või mittesuitsetaja summadega.</br></br>Mõlemas arvutuses kasutatakse arvutamise suunda, et määrata, kas ümardada arvutuse summaga jagatav aastase soodustuse palk või katvuse summa üles- või allapoole. |
   | **Arvutamissumma** | Soodustuse määra arvutamise toimingu ajal kasutatav summa. See summa saab olema taseme määra matemaatilise arvutamise ajal jagaja. |
   | **Arvutuse suund** | Suund, kuhu suunas arvutatud tulemuse summat tuleb ümardada. Süsteem toetab kolme arvutuse suunda: tühi (täpne meetod), **suurenemine** ja **vähenemine**.</br></br><ul><li>Kui väli on tühi, kasutab süsteem arvutamise summaga jagatava palga/katvuse summa täpset arvutust. Kui sellel väärtusel on murd, kasutab süsteem seda oma arvutustes.</li><li>**Suurendamise** korral suurendab süsteem arvutamise summaga jagatava palga/katvuse summa matemaatilise arvutuse järgmise täisarvuni, mis tähendab, et 12,25 suureneks 13-ni.</li><li>**Vähendamise** korral vähendab süsteem arvutamise summaga jagatava palga/katvuse summa matemaatilise arvutuse praeguse täisarvuni, mis tähendab, et 12,25 väheneks 12-ni.</li></ul> |
   | **Mittesuitsetaja töövõtja summa** | Summa, mille hüvitise pakkuja küsib mittesuitsetava töövõtja eest. See on summa, mille töövõtja maksab soodustuse pakkujale, ja see peaks põhinema määra seadistuse maksesagedusel. |
   | **Mittesuitsetaja tööandja summa** | Summa, mille hüvitise pakkuja küsib mittesuitsetava töövõtja eest. See on summa, mille töövõtja maksab soodustuse pakkujale, ja see peaks põhinema määra seadistuse maksesagedusel. |
   | **Suitsetaja töövõtja summa** | Summa, mille hüvitise pakkuja küsib mittesuitsetava töövõtja eest. See on summa, mille töövõtja maksab soodustuse pakkujale, ja see peaks põhinema määra seadistuse maksesagedusel. |
   | **Suitsetaja tööandja summa** | Summa, mille hüvitise pakkuja küsib mittesuitsetava töövõtja eest. See on summa, mille töövõtja maksab soodustuse pakkujale, ja see peaks põhinema määra seadistuse maksesagedusel. |
   | **Haldussumma** | Kolmandast poolest haldaja küsitav haldussumma. See on summa, mille töövõtja maksab kolmandast poolest haldajale, ja see peaks põhinema määra seadistuse maksesagedusel. |
   | **Paindliku krediidi mittesuitsetaja määr** | Soodustusele kuluv paindliku krediidi hulk, mis põhineb mitte-suitsetajate tasemete jaoks määratletud arvutusel. Näiteks kui arvutamise tüüp on **katvuse summa kohta**, arvutamise summa on 10 000 ja paindliku krediidi mittesuitsetaja määr on 6, siis see tähendab, et kui mittesuitsetajast töövõtja valib katvuse 10 000 dollarit, maksab see 6 paindlikku krediiti. Kui nad valivad katvuse 20 000 dollarit, siis maksab see 12 paindlikku krediiti jne. |
   | **Paindliku krediidi suitsetajate määr** | Soodustusele kuluv paindliku krediidi hulk, mis põhineb suitsetajate tasemete jaoks määratletud arvutusel. |

5. Valige käsk **Salvesta**. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
