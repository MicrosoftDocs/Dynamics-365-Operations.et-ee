---
title: Ostutellimuse sisestamine
description: See artikkel kirjeldab varude sisestusreeglite lehe ostutellimuste vahekaarti.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 0793c58b07d2c0a133e1a5bc0607483f22206b95
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849927"
---
# <a name="purchase-order-posting"></a>Ostutellimuse sisestamine

Lao **sisestusreeglite** lehel oleval **ostutellimuse** vahekaardil saate kontrollida, kuidas ostutellimused pearaamatusse sisestada. Kaks peamist ostutellimuse pearaamatusse sisestamist: 

- Toote sissetulek
- Arve

Füüsilise kande (toote sissetuleku) sisestamiseks ostutellimuse pearaamatusse peavad olema märgitud järgmised märkeruudud:

- Toote **sissetuleku pearaamatusse sisestamise** märkeruut lehel Varude **ja laohalduse parameetrid**
- Märkeruudud **Sisesta** füüsiline **ladu ja Kumul märkige** toote sissetulekul kauba **mudeligruppide** lehel.

Lao sisestusreeglite lehel tuleb määrata **põhikontod** järgmiste sisestustüüpide jaoks:

- Saadud ostumaterjalide omahind
- Ostu kulud, arvele taatamata
- Ost, tekkepõhine

Finantskande (arve) sisestamiseks pearaamatusse ostutellimusel peavad olema täidetud järgmised tingimused:

- Ostutellimuse **real valitud** kauba puhul peab olema **valitud** rahaliste varude sisestamise märkeruut kauba mudeligruppide lehel.
- Lao sisestusreeglite lehel tuleb määrata **põhikontod** järgmiste sisestustüüpide jaoks:
  - Arveldatud ostetud materjalide kulu
  - Toote ostu kulu
  - Kulu ostukulu
  - Allahindlus (valikuline)

## <a name="fixed-receipt-price-posting"></a>Fikseeritud jaehinna sisestamine

Saate kasutada fikseeritud omahinda toote **standardkuluna** **·** **·**, kui valite kauba mudeligruppide lehe laomudeli väljal suvandi Standardne omahind. Peamine erinevus on see, et **fikseeritud** jaehinna kasutamisel kasutatakse lao sissetuleku sisestamisel kauba praegust omahinda. Fikseeritud jaehinna kulu ümberhindamise **protsessi** pole olemas. Finantsvärskenduse sisestamisel kasutatakse praegust omahinda sisestamise ajal. Kui sissetulekul ja arvel kasutatud omahinna vahel on erinevus, sisestab hälve fikseeritud jaehinna kasumi- ja kahjumikontodele.

Toote fikseeritud jaehinna kasutamiseks tuleb teil konfigureerida järgmine:

- Kauba mudeligruppide **lehel valige** märkeruudud Sisesta **füüsiline** **ladu ja** Fikseeritud vastuvõtuhind. 
- Varude ja **laohalduse parameetrite lehel** märkige ruut Sisesta **saateleht pearaamatusse**.
- Määrake lehel **Lao sisestusreeglid** järgmiste sisestustüüpide põhikontod:
  - Fikseeritud jaehinna kasum
  - Fikseeritud jaehinna kahjum
  - Fikseeritud jaehinna vastaskonto

Lisateabe saamiseks minge fikseeritud [vastuvõtuhinnale](/supply-chain/cost-management/fixed-receipt-price.md).

## <a name="purchase-charges-and-stock-variation-posting"></a>Ostu kulude ja laovariatsiooni sisestamine

Kui plaanite arvestada ostukulusid ja lao muudatusi, tehke järgmist:

- Märkige vahekaardi **Arve ostureskontro** parameetrid **ruut** **Sisesta pearaamatusse.**
- Märkige ostutellimuse **real valitud** kauba mudeligruppide lehel ruut Sisesta füüsiline ladu, **·** **Sisesta** **finantsiline laovaru ja Viitkohustus** toote sissetulekul.
- **Hankeparameetrite lehel märkige** ruut Loo toote **sissetuleku kulud**.
- Varude ja **laohalduse parameetrite lehel** märkige ruut Sisesta **saateleht pearaamatusse**.

Lao sisestusreeglite **lehel** peate määrama põhikontod järgmistele sisestustüüpidele:

- Ostu kulud, arvele taatamata
- Toote ostu kulu
- Lao muudatus

> [!NOTE]
> Tasu **sisestamise** tüüpi ei kasutata, kui on valitud **pearaamatu parameetri suvand Sisesta kulukontole**.

Lisateavet vt jaotisest Sisesta kulukonto [raamatupidamispõhimõte](/supply-chain/cost-management/post-to-charge-account-accounting-principle.md).

## <a name="sample-posting-profile-configuration"></a>Sisestusprofiili näidiskonfiguratsioon

Järgmine tabel näitab vaikimisi sisestamistüüpide näiteid koos näidis põhikontode ja kirjeldustega:

- Kliiringukonto **veerg** näitab, et sisestamistüüp on kliiringukonto. Kontole sisestatud summa tühistatakse hilisema kande sisestamisel automaatselt. 
- Veerg **P/F näitab** füüsilise sisestamise **P-d** ja finantsilist **sisestamist** F. 
- Veerg **Järgi** näitab, kas kindla sisestustüübi põhikonto on tavaliselt sama mis mõni muu sisestamistüüp. Veeru väärtus näitab tavaliselt kasutatavat sisestustüüpi.

> [!NOTE]
> Põhikontod ja põhikonto nimed on ainult soovitused. Soovitame<!--note from editor: Via Writing Style Guide.--> , et töötate koos raamatupidajaga, et määrata oma ärivajaduste parim konfiguratsioon.


| Sisestamistüüp | Põhikonto näide | Põhikonto nime näide | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Ette/tagasi | Järgige | Kirjeldus |
|--------------|---------------------|-------------------------|----------------|----------------|--------------------|----|----------|-----------|
| Saadud ostetud materjalide kulu | 140100</br>140101 | Materjalide laoseis</br>Saadetud, arveldamata materjalid | Vara | Deebet | Jah | P | Arveldatud ostetud materjalide kulu | Kasutatakse ostutellimuse toote sissetuleku sisestamisel. Konto vastaskonto on ostu kulu, arvelt eemaldamata. Selle konto summa tühistatakse ostutellimuse arve sisestamisel. |
| Ostu kulud, arvele taatamata | 600180 | Materjali sissetulekud | Kulu | Deebet | Jah | P | |Kasutatakse ostutellimuse toote sissetuleku sisestamisel. Sissetuleku jaoks luuakse kaks kannet ostuhinna hälvete jälgimiseks, kui kasutatakse standardkulu. Esimese kande vastaskontoks on ostu viitvõlg. Teise kande vastaskonto on saadud materjalide omahinna ja ostuhinna hälbe kontode summa. Sellele kontole sisestatud summad tühistatakse ostutellimuse arve sisestamisel. |
| Arveldatud ostetud materjalide kulu | 140100 | Materjalide laoseis | Vara | Deebet | Nr | R  |Saadud ostetud materjalide kulu | Kasutatakse ostutellimuse arve sisestamisel. Selle konto vastaskonto on toote ostu kulu. See konto tähistab teie bilansikonto varusid. Kasutatav konto on tavaliselt sama, mida kasutatakse tarnitud ühikute omahinna ja müügitellimuse arveldatud ühikute omahinna puhul. |
| Toote ostu kulu | 600180 | Materjalide sissetulek | Kulu | Krediit | Nr | R  | |Kasutatakse ostutellimuse arve sisestamisel. Selle konto vastaskonto on ostetud materjalide kulu. See konto tähistab teie bilansikonto varusid. |
| Fikseeritud jaehinna kasum (ost, fikseeritud jaehinna kasum*) | 510310 | Ostuhinna erinevus | Kulu | Krediit | Nr | R | Fikseeritud jaehinna kahjum | Kasutatakse ostutellimuse arve sisestamisel ning arveldatud hinna ja kauba vaikekulu vahel on erinevus. Seda kontot kasutatakse siis, kui erinevus on suurem. Selle konto vastaskonto on fikseeritud jaehinna vastaskonto. |
| Fikseeritud jaehinna kahjum (ost, fikseeritud jaehinna kahjum*) | 510310 | Ostuhinna erinevus | Kulu | Deebet | Nr | R | Fikseeritud jaehinna kasum | Kasutatakse ostutellimuse arve sisestamisel ning arveldatud hinna ja kauba vaikekulu vahel on erinevus. Seda kontot kasutatakse siis, kui erinevus on väiksem. Selle konto vastaskonto on fikseeritud jaehinna vastaskonto. |
| Fikseeritud jaehinna vastaskonto (ost, fikseeritud jaehinna vastaskonto*) | 140900 | Lao muudatus | Vara | Mõlemad | Nr | R  | |Kasutatakse ostutellimuse arve sisestamisel ning arveldatud hinna ja kauba vaikekulu vahel on erinevus. See konto on vastaskonto fikseeritud jaehinna kasumi- ja kahjumikontodele. |
| Tasu | – | – | – | – | – | – | – | Seda kontot enam ei kasutata. Kasutage selle asemel lao muudatust. |
| Lao muudatus | 600170 | Lao muudatus | Kulu | Krediit | Nr | Mõlemad | | Seda kontot kasutatakse siis, kui: <ul><li>Toote sissetuleku ja arve ühikuhinnad on erinevad.</li><li>Kulud sisestatakse kaubale.</li><li>Kaudsed kulud on olnud<!--note from editor: Edit okay?--> Lisati ostetud kaupadele. </li><li>Selle konto vastaskonto on ostu kulu, arvele lisamata konto.</li></ul> |
| Ost, tekkepõhine | 200140 | Tekkepõhised ostud | Kohustus | Krediit | Y | P | |Kasutatakse ostutellimuse toote sissetuleku sisestamisel ja ostusummade lisandumise valiku lubamisel. |
| Tekkepõhine käibemaks sissetulekul | 250500 | Viitmaks | Kohustus | Krediit | Y | Mõlemad  | |Seda kontot kasutatakse siis, kui valite **varude ja laohalduse** **parameetrites** suvandi Sisesta füüsiline maks ning teil on ostutellimus koos maksuga. Summa sisestatakse ostutellimuse füüsilisel uuendamisel (toote sissetulekul) ja tühistatakse, kui sisestate ostutellimuse finantsiliselt (arve). |
| Põhivara sissetulek (Põhivara deebet*) | 180100 | Materiaalsed põhivarad | Vara | Deebet | E | Mõlemad | Mõlemad | Seda kontot kasutatakse siis, kui valite põhivarade ostutellimuse real valiku. Ostutellimuse integreerimine on konfigureeritud põhivara soetuseks toote sissetulekul või arvel. Lisateavet põhivara ostutellimuse integreerimise kohta vt varade soetamine [hanke kaudu](/fixed-assets/acquire-assets-procurement). |
| Kulu ostukulu | 618900 | Mitmesugused kulud | Kulu | Deebet | E | Mõlemad | |Kasutatakse toote sissetuleku või arve sisestamisel ostutellimusele, kus kaubad ei ole ladustatud või kasutatakse hankekategooriat. |
| Ettemaks | 132190 | Ettemakstud kulu | Vara | Deebet | E | Mõlemad | | Kasutatakse ettemaksuarve töötlemisel ostutellimusel. |


\* Sulgudes kuvatud väärtused tähistavad väärtust, mida kasutatakse **kandelehe kande** **väljal Sisestustüüp**. Sisestustüüpi saate **vaadata** vahekaardi **Üldine** lehel Kande **kanded**.

## <a name="fixed-asset-posting-with-purchase-orders"></a>Põhivara sisestamine ostutellimustega

Kui kasutate moodulit **Põhivarad** ja plaanite põhivarasid ostutellimuste kaudu osta, **·** **·** **peate konfigureerima põhivara sissetuleku sisestustüübi vahekaardi Lao sisestusreeglid vahekaardil** Ostutellimus. Lisateabe saamiseks minge põhivarade integreerimisesse ning [looge ja](/fixed-assets/fixed-asset-integration.md) soege [varad Ostureskontrost](/fixed-assets/tasks/create-acquire-assets-accounts-payable.md).

## <a name="prepayment-purchase-order-invoice-posting"></a>Ettemaksu ostutellimuse arve sisestamine

Kui te kavatsete ostutellimuste **puhul** kasutada ettemaksuarve funktsiooni, **·** **peab** lao sisestusreeglite lehe ostutellimuse vahekaardil olema valitud ettemakse **sisestamistüüp.** Lisateavet vt ettemaksuarvete [vs. ettemaksete kohta](/accounts-payable/prepayments-invoices-vs-prepayments.md).

## <a name="purchase-requisition-and-purchase-order-confirmation-posting"></a>Ostutaotluse ja ostutellimuse kinnituse sisestamine

Ostutaotlusi ja ostutellimuse kinnitusi saab konfigureerida ka eelpandiõiguste ja pandiõiguste sisestamiseks pearaamatusse. Neid sisestusi kontrollib sisestamisdefinitsioon. Lisateabe saamiseks minge ostutellimuse [pandiõiguste kohta](/dynamicsax-2012/appuser-itpro/about-purchase-order-encumbrances).

## <a name="procurement-category-posting"></a>Hankekategooria sisestamine

Kõigi kaupade, kaubagrupi või üksiku kauba varude sisestamise seadistamise alternatiivina saate seadistada kategooriaid ja kontrollida pearaamatu sisestamist hankekategooriate kaupa. Lisateavet kategooriate seadistamise ja nende toodetele määramise kohta leiate käesoleva artikli varasemast [sisestusprofiili](#sample-posting-profile-configuration) konfiguratsioonist.

Ostutellimuste või hankija arvetega kategooriate **kasutamisel** **peab kategooriahierarhia olema määratud kategooriakategooria hierarhia tüübile kategooriahierarhia rolli määrangute** lehel.

### <a name="vendor-invoices-with-procurement-categories"></a>Hankija arved hankekategooriatega

Kui teie organisatsioon kasutab ostutellimusi mõne ostu, mitte teiste jaoks, saate töödelda mitteostutellimusega seotud arveid erinevatel viisidel. See hõlmab töölehti **Ostureskontros** **või lehte Ootel** hankija arved, mida kasutatakse ostutellimuste arvete loomiseks. Arvete loomisel mitteostutellimusega seotud arvetele peate looma hankekategooriad iga kulutüübi jaoks. Kategooria tuleb lehel Lao sisestamise profiilid vastendada õige **kulukontoga**.

Kategooriate täpne arv erineb kulukontode arvu alusel, mida kasutate oma arvete sisestamiseks. Vajate vähemalt üht hankekategooriat igale põhikontole, mille jaoks te ostutellimuse mitte-arveid kulute. Ühe põhikonto jaoks saab kasutada mitut kategooriat. See võib olla kasulik kasutatavuse, otsitavuse ja aruandluse jaoks teie kulusid.

### <a name="benefits-of-using-procurement-categories-for-vendor-invoices"></a>Hankija arvete hankekategooriate kasutamise eelised

Mõned hankija arvete hankekategooriate kasutamise eelised on järgmised.

- Kooskõlaline kasutajakogemus: kui konfigureerite hankekategooriaid kõigile nendega seotud mitteostutellimusega seotud kuludele, **võivad kasutajad saada teavet ühe arveldamisprotsessi kohta, kasutades lehte Ootel** hankija arved.
- Täiustatud aruandluskogemus: kui konfigureerite hankekategooriaid kõigile kaupadele ja kõigile nendega seotud mitteostutellimustele, analüüsib hankekulu aruanne kulumist hankija, kategooria jne alusel.
- Kooskõlaline töövoog: kui **kasutate ootel** hankija arveid kõikide arvete töötlemiseks, saate luua ühtse töövoo ja kinnitusprotsessi, kasutades üht töövoogu.

## <a name="consignment-inventory-posting"></a>Veose varude sisestamine

Veose kaubavaru kasutab sama pearaamatu sisestamist nagu teised ostetud kaubad. Võtmeerinevus on see, et varude kätte saades ei kirjendata ühtegi pearaamatu kannet. Omaniku üleviimine organisatsioonile varude **omaniku** muudatuste töölehe sisestamisel luuakse kanne kauba kulu kirjendamiseks. Lisateabe saamiseks minge saadetise [seadistama](/supply-chain/inventory/consignment.md).
