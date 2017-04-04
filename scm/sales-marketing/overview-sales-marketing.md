---
title: "Müük ja turundus"
description: "Müügi ja turunduse abil saate müügivoos hankida, talletada ja kasutada mitmesuguseid andmeid. Andmed hõlmavad algset müügialgatust, tulevasi järeltegevusi ja lisamüüki."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 92303
ms.assetid: 65ca9992-bbfa-4224-bf0e-067a25c7e6a4
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f9e79b5dad120e057193b97d9c87665c54fea023
ms.lasthandoff: 03/31/2017


---

# <a name="sales-and-marketing"></a>Müük ja turundus

Müügi ja turunduse abil saate müügivoos hankida, talletada ja kasutada mitmesuguseid andmeid. Andmed hõlmavad algset müügialgatust, tulevasi järeltegevusi ja lisamüüki.

<a name="marketing"></a>Turundus
---------

Saate kasutada turunduskampaaniaid ja tegevusi potentsiaalsete klientide leidmiseks ja nendega seoste loomiseks, et algsest suhtlusest saaksid kujuneda müügisuhted. Järgmine protsessivoog näitab turunduse äriprotsessi. [![Äriprotsessi turustamiseks](./media/marketing01.jpg)](./media/marketing01.jpg)

### <a name="relationships"></a>Seosed

Müügis ja turunduses võib algne suhtlus potentsiaalsete klientidega leida aset mitmesugustes olukordades. Näiteks võite leida tulevase kliendi ärimessilt või saada kliendi kohta müügivihje pärast seda, kui teie organisatsioon viib läbi hulgipostituse kampaania. On väga oluline mõista osapoole üksuse voogu, enne kui osapoolest saab klient. Järgmisel joonisel on näidatud üksuse seoste voog, kui potentsiaalsest kliendist saab tegelik klient. [![SalesandMarketing01](./media/salesandmarketing01.jpg)](./media/salesandmarketing01.jpg)

### <a name="campaigns"></a>Kampaaniad

Kampaania on suunatud potentsiaalsete klientide, müügivihjete, müügivõimaluste ja klientide kontaktidele, mis on valitud kampaanias osalema. Microsoft Dynamics 365 toiminguteks, saate luua mitut tüüpi kampaaniaid, nagu telemarketingi, posti ja e-posti kampaaniad, et maksimeerida teie potentsiaalne klient. Kui saate kampaania käigus positiivseid vastuseid, saate alustada müügiprotsessi nende saajatega, kes on kampaaniale positiivselt vastanud.

## <a name="sales"></a>Müük
Müügifunktsiooni abil saab koostada hinnapakkumisi, teha ülesmüüki ja ristmüüki uutele ja olemasolevatele klientidele, koostada müügitellimusi ja koostada klientidele müügiarveid. Järgmine protsessivoog näitab müügi äriprotsessi. [![Äriprotsessi müügi](./media/sales01.jpg)](./media/sales01.jpg)

### <a name="sales-quotations"></a>Müügipakkumised

Koostate müügipakkumisi klientidele pakutavate kaupade või teenuste pakkumise esitamiseks. Klient võib pakkumist küsida või võite koostada pakkumise vastuseks potentsiaalse või olemasoleva kliendi päringule. Kui klient müügipakkumise heaks kiidab, saab selle müügitellimuseks teisendada.

### <a name="up-sellcross-sell"></a>Ülesmüük/kaasmüük

Ülesmüük ja ristmüük on tehnikad toodete müügiks kliendi tellimuse sisestamisel. Ülesmüügi korral soovitatakse olemasoleva toote asemel teist toodet. Ristmüügi korral soovitatakse mõnda toodet lisaks olemasolevale tootele. Toodete nimekirja seadistamisel saate luua erieeskirju, mis näitavad, millal toode tuleks teha ettepanek ristsaastumise müüa või up-müüa toode.

### <a name="sales-orders"></a>Müügitellimused

Uue müügitellimuse loomisel peate valima loodava müügitellimuse tüübi. Teil on viis võimalust. **Märkus:** pärast müügitellimuse loomist saab iga tellimuse tüüpi muuta, välja arvatud tüüpi **Kaubavajadused**, kui müügitellimuse olek on **Tarnitud**.

| Müügitellimuse tüüp  | Kirjeldus                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tööleht           | Kasutage seda tüüpi müügitellimuse mustandina. See tüüp ei mõjuta laokoguseid ega loo kaubakandeid.                                                                                                                                                                    |
| Korduv tellimus      | Kasutage seda tüüpi kordustellimuste jaoks. Tellimuse arveldamisel määratakse tellimuse olekuks automaatselt Avatud tellimus. Tarnitud arveldatud kogus ja järelejäänud tarned uuendatakse. Seda müügitellimuse tüüpi ei saa kasutada, kui kasutate laohalduse funktsiooni. |
| Müügitellimus       | Kasutage seda tüüpi, kui klient on tellimuse esitanud või kinnitanud.                                                                                                                                                                                                                                        |
| Tagastatud tellimus    | Kasutage seda tüüpi, kui klient tagastab kauba. Tagastatava kauba kood (RMA-kood) määratakse automaatselt.                                                                                                                                                                                            |
| Kaubavajadused | See tüüp luuakse automaatselt kauba müümisel projekti kaudu.                                                                                                                                                                                                                       |

### <a name="sales-agreements"></a>Müügilepingud

Müügileping on lepe, mis kohustab klienti aja jooksul kindlates kogustes või kindla summa eest toodet ostma ja võimaldab seda teha erihinnaga või allahindlustega. Müügilepingute hinnad ja allahindlused alistavad kõik hinnad ja allahindlused, mis on märgitud olemasolevates kaubanduslepetes. Müügileping kehtib kindlaksmääratud aja jooksul. Soovitud lähetuskuupäev, mis on määratud müügile lehel **Müügitellimus**, peab jääma kehtivasse perioodi. Vaikimisi on müügileping ootel. Saate müügilepingul tellimuse esitada vaid juhul, kui selle olek on **Jõustunud**.

### <a name="backorders"></a>Järeltellimused

Tellimuste sisestamisel ja kinnitamisel võib olla vaja enne müügi lõpuleviimist järeltellimusi ja erandeid hallata. Järeltellimused on ostutellimused, mis pole veel hankijalt tarnitud, või müügitellimused, mida pole veel kliendile tarnitud. Järeltellimusi on oluline jälgida. Kui näiteks toodete tarnimine hankijalt hilineb, peate võib-olla muutma kliendile tarnimise kuupäeva ning klienti siis viivitusest teavitama. Järeltellimusi saab vaadata kauba, kliendi või hankija alusel.

#### <a name="viewing-backorders-by-item"></a>Järeltellimuste kuvamine kauba kohta

Järeltellimuste kuvamisel kauba kohta saate jälgida teatud kauba eeldatavat kannete voogu. Näiteks saate kontrollida järgmist teavet.

-   Kauba kohta esitatud müügitellimuste arv
-   Kas hankijate kaubatarne on endiselt puudu
-   Kas tuleks tellida veel kaupu, et saaksite kõik müügitellimused õigeaegselt kohale toimetada

Sel viisil kontrollides saate reageerida klientide soovidele kaubatarne ajastuse kohta. Lisaks sellele saate määrata müügi järeltellimuste tähtsusastmed ja laos olevad kaubad tellimuste vahel jaotada.

#### <a name="viewing-backorders-by-customer"></a>Järeltellimuste kuvamine klientide kaupa

Järeltellimuste kuvamisel kliendi kohta saate vaadata kliendi järelejäänud tellimuste olekut. Selline kontrollimine on abiks, kui peate vastama klientidele, kes ootavad viibivaid kaupu.

#### <a name="viewing-backorders-by-vendor"></a>Järeltellimuste kuvamine hankijate kaupa

Järeltellimuste kuvamisel hankijate kaupa saate jälgida puuduolevaid tarneid ning eeldatavaid tarnekuupäevi. Sellisest kontrollimisest on abi ka hankijatelt saabuvate järeltellimuste tähtsusastmete määramisel ning müügitellimuste komplekteerimisel tarneteks.

### <a name="invoices"></a>Arved

Müügiprotsessi ajal saate luua kolme tüüpi arveid.

-   Kliendiarve
-   Vabas vormis arve
-   Esialgne arve

#### <a name="customer-invoice"></a>Kliendiarve

Kliendiarve on arve, mille organisatsioon kliendile müügiga seoses edastab. Selline kliendiarve koostatakse müügitellimuse põhjal, milles on päis ja vähemalt üks rida kaupade või teenuste kohta. Kliendiarve lõpetab müügitellimuse, saatelehe ja müügiarve tsükli.  

Sisestada ja printida saab üksiku müügitellimusel või saatelehel ja kuupäeval põhineva kliendiarve. Samuti saab sisestada ja printida mitu saatelehtedel ja kuupäevadel põhinevat kliendiarvet koos. Üksiku kliendiarve sisestamisel müügitellimuse abil uuendatakse iga kauba kogus väljal **Arve jääk** arveldatud kogustega valitud müügitellimusest.  

Kui kõigi müügitellimuse kaupade kogused **Arve jääk** ja **Tarne jääk** on 0 (null), määratakse müügitellimuse olekuks **Arveldatud**. Kui ükskõik kumma välja kogus ei ole 0, siis müügitellimuse olekut ei muudeta ja sisestada saab täiendavaid arveid. Kui kavatsete sisestada ja printida vähemalt ühe saatelehtedel põhineva kliendiarve, peate olema juba sisestanud iga müügitellimuse kohta vähemalt ühe saatelehe. Kliendiarve aluseks on need saatelehed ja arve kajastab saatelehtedel olevaid koguseid.  

Saate luua kliendiarve, mis põhineb saatelehe tähtajaliselt välja saadetud reakaupadel, isegi kui kõik konkreetse müügitellimuse kaubad ei ole veel välja saadetud. Seda saate teha nt siis, kui teie juriidiline isik väljastab igale kliendile ühe arve kuus, mis katab kõik selle kuu tarned. Iga saateleht esindab müügitellimusel olevate kaupade osalist või täielikku väljasaatmist.  

Arve sisestamisel uuendatakse iga kauba kogus väljal **Arve jääk** tarnitud kogustega valitud saatelehtedelt. Kui kõigi müügitellimuse kaupade kogused **Arve jääk** ja **Tarne jääk** on 0 (null), määratakse müügitellimuse olekuks **Arveldatud**. Kui kogus ei ole 0, siis müügitellimuse olekut ei muudeta ja sisestada saab täiendavaid arveid. Laokandeid uuendatakse koos arvenumbritega ja olek müügitellimuse real muutub olekuks **Arveldatud**.

#### <a name="free-text-invoice"></a>Vabas vormis arve

Vabas vormis arve on arve, mis ei ole seotud müügitellimusega. See sisaldab tellimuse ridu, mille hulka kuuluvad pearaamatukontod, vaba tekstina sisestatud kirjeldused ja müügihind. Seda tüüpi arvele ei saa sisestada kaubakoodi ja sisestada tuleb vastav käibemaksuteave. Müügi põhikonto on näidatud igal arve real. Kliendi saldo sisestatakse vabas vormis arve puhul kasutatavatest sisestusreeglitest koondkontole.

#### <a name="pro-forma-invoice"></a>Esialgne arve

Esialgne arve on arve, mis on vormistatud hinnangulise arvesummaga enne arve sisestamist. Saate printida esialgse arve nii kliendiarve kui ka vabas vormis arve kohta.


