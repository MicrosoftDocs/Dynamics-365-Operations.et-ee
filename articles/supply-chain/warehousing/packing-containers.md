---
title: Pakkekonteinerid lähetamiseks
description: Selles artiklis kirjeldatakse pakkimisprotsessi, mis võimaldab teil kinnitada laovaru kaupu ja pakkida need konteineritesse.
author: perlynne
ms.date: 7/13/2022
ms.topic: business-process
ms.search.form: WHSLocationType, WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup, WHSPack, WHSContainerTable,
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 171b9f1dcb1d4ece63bc0beeb71f45b9f8ae7bba
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220739"
---
# <a name="pack-containers-for-shipment"></a>Pakkekonteinerid lähetamiseks

[!include [banner](../../includes/banner.md)]

Konteineri pakkimisprotsess võimaldab teil kinnitada laokauba ja pakkida need konteineritesse. Selle protsessi ajal komplektivad laotöötajad tavaliselt laokauba hulgilaoalalt ja teisaldavad need pakkimisalale. Mitu laotöötajat kontrollib kauba koguseid ja tüüpe ning määrab need asjakohastele konteinerisuurustele. Kui konteiner on täielikult pakitud, siis see suletakse ja teisaldatakse väljastamisalasse, kus see on lähetamiseks valmis.

Konteinerid tähistavad füüsilisi struktuure, kus kaubad on pakitud, ja te saate jälgida konteineri teavet süsteemis. See teave võib olla kasulik transpordi planeerimisel, eriti kui arvutate konteinerite alusel saatekulud. Enne saatmist saate vaadata saadetises kasutatavate konteinerite arvu, kasutatavaid konteineritüüpe ja iga konteineri füüsilisi dimensioone (nt kogumaht ja kaal).

Konteineritega saab kasutada mitut seotud väljamineva lao võimalust. Lisateavet vt järgmistest artiklitest.

- [Voo konteinerite kogumine](wave-containerization.md)
- [Väljastuste sortimine](outbound-sorting.md)
- [Väikepaki saatmine](small-parcel-shipping.md)
- [Kinnitamine ja üleviimine](confirm-and-transfer.md)
- [Pakkimiseks ja ladustamiseks erinevate dimensioonide määramine](packing-vs-storage-dimensions.md)
- [Väljaminevate konteinerite ja saadetiste töötlemise pakketöö](packing-work.md)
<!-- KFM: Add link to upcoming topic when available (10.0.31): [Manual packing on the Warehouse management mobile app](manual-packing-on-the-warehouse-management-mobile-app.md) -->

## <a name="set-up-your-warehouse-to-use-manual-packing-operations"></a>Lao käsitsi pakkimistoimingute kasutamiseks

Väljaminevate operatsioonide korraldamiseks on kaks põhilist võimalust:

- **Voo loomine ja töötlemine** – töötajad komplekteeritud kaubad väljamineva lao töö põhjal. Seejärel asetavad kaubad otse väljaminevasse lähetusasukohta, kus nad on valmis koheseks lähetamiseks. Lisateavet selle protsessi häälestamise ja kasutamise kohta vt [voo loomine ja töötlemine](wave-processing.md).
- **Käsitsi pakkimine pakkimisel** – sellel protsessil on komplekteerimise ja lähetustoimingute vahel lisatoiming. Selle asemel, et panna varud *uksega lähetusasukohta*, asetavad töötajad selle *pakkimiskohta*. Seejärel haldavad nad pakkimisprotsessi pakkejaamas, kasutades **veebikliendi** pakkelehte. Selle protsessi lubamiseks peate konfigureerima oma süsteemi nii, nagu on kirjeldatud selles jaotises.

### <a name="set-up-warehouse-locations-for-packing"></a>Lao asukohtade häälestamine pakkimiseks

Teil peab olema vähemalt üks pakkimiskoht, kus töötajad panevad laokauba nii, et neid saab konteineritesse pakkida. Lisateavet ladude asukohtade loomise kohta vt WMS-iga [lubatud lao asukohtade konfigureerimine](tasks\configure-locations-wms-enabled-warehouse.md). Järgmised alamjaotised kirjeldavad, kuidas luua ja seadistada pakkimiskohti.

#### <a name="set-up-location-types-for-packing"></a>Pakkimiseks asukoha tüüpide häälestamine

Pakkimisasukohtade *jaoks* peate määratlema asukohatüübi. Asukohatüüpe saab kasutada filtreerimissuvanditena erinevate laohaldusprotsesside kontrollimiseks. Iga asukohatüübi nimi kirjeldab tavaliselt midagi selle kohta, kuidas seda asukohatüüpi tuleks kasutada. Siin seadistatud asukohatüüp tuleb seostada iga pakketoimingutes kasutatava asukohaga.

Asukoha tüübi häälestamiseks järgige neid samme.

1. Avage jaotis **Laohaldus \> Seadistus \> Ladu \> Asukoha tüübid**.
1. Tegevuspaanil valige **uus**, et lisada asukoha tüüp ruudustikku.
1. Seadke uuele asukohatüübile järgmised väljad:

    - **Asukoha** tüüp : sisestage asukoha tüübile nimi. Iga nimi peab olema kordumatu ja see peab kirjeldama midagi selle kohta, kuidas asukoha tüüpi kavatsetakse kasutada.
    - **Kirjeldus** : sisestage asukoha tüübi lühikirjeldus.

#### <a name="inform-the-system-about-the-packing-location-type"></a>Teavita süsteemi pakkimisasukoha tüübist

Pärast asukohatüübi loomist tuleb süsteemil see pakkimistoimingutes kasutamiseks asukoha tüübina tuvastada.

Pakketoiminguteks kasutatava asukoha tüübi tegemiseks järgige neid samme.

1. Mine laohalduse **häälestuse \>\> laohalduse parameetritele**
2. Seadke vahekaardi **Üldine** kiirkaardi Asukohatüübid **väljale** Pakkimiskoha tüüp selle asukoha tüüp, **mida** kasutate pakkimise tüüpide tuvastamiseks.

> [!NOTE]
> Versiooni uuendamisel Microsoft Dynamics AX *eemaldati* pakkimisel olek saadetistest ja koormatest, kuna see ei toiminud järjekindlalt ega põhjustanud liigseid andmeid. Seetõttu on saadetised **ja** koormad **saatelehelehtedel** taunitud. Pakitavad konteinerid jälgitakse asukoha tasemel.
>
> Eelmistes **versioonides** **määrati pakkimisasukoht, kasutades asukohaprofiili määramiseks pakkimiskoha vahekaardi Pakkimine välja Pakkimine ID-d.** **·** *·* Praeguses **versioonis** **·** **kasutate laohalduse parameetrite lehe vahekaardil Üldine pakkimiskoha tüübi välja Asukoha tüüp, et määrata asukoha tüüp, nagu selles artiklis** *kirjeldatud*. Uus väli on paremini joondatud protsessiga lähetuskohtade ja lõppsihtkohtade määratlemiseks.
>
> Kuigi saate pakkimisasukohas **kasutada ka vana profiili ID-d**, **on** soovitatav selle asemel alustada uue pakkimiskoha tüübi välja kasutamist, kuna vana väli on lõpuks taunitav.
>
> Kui tühjendate pakkimisasukoha **välja vana profiili** ID sätte ja seejärel salvestate lehe, keelatakse see väli jäädavalt. Installide puhul, kus **pakkimiskoha profiili** ID-d pole kunagi kasutatud, keelatakse see alati. Pärast pakkimisasukoha **profiili ID** sätte tühjendamist kasutage pakkimisasukoha seadistamiseks ja tuvastamiseks selles artiklis kirjeldatud sätteid.

#### <a name="set-up-location-profiles-for-packing-locations"></a>Pakkimisasukohtade asukohaprofiilide häälestamine

Iga *asukoha* profiil kehtestab teabe ja reeglid, mida rakendada seotud asukohtades. Kuna pakkimistoimingute jaoks peab kasutama vähemalt ühte asukohta, peate sellele lisaks asukohatüübile looma ka asukohaprofiili. Igat profiili saab kasutada mis tahes arvus asukohtades. Pakkimiseks kasutatavad asukohad tuleb häälestada litsentsiplaatide jälgimiseks.

Pakkimisasukoha asukohaprofiili häälestamiseks järgige neid samme.

1. Minge asukohta **Laohaldus \> Seadistus \> Ladu \> Asukohaprofiilid**.
1. Valige loendipaanilt olemasolev profiil või **valige** uue reegli loomiseks tegevuspaanil uus.
1. Seadke uue või valitud reegli päises järgmised väljad:

    - **Asukoha profiili ID** – sisestage profiili kordumatu ID.
    - **Nimi** : sisestage profiili kirjeldav nimi.

1. Määrake kiirkaardil **Üldine** järgmised väljad.

    - **Asukoha vorming** : valige asukoha vorming, mida praeguses asukohas kasutada. Asukoha vormingud on nimetamissüsteem, mida kasutatakse laos kasutatavatele erinevate asukoha asukohakohtade kohtade kordumatute ja järjepidevate nimede loomiseks. Kui teil ei ole veel soovitud vormingut, saate selle luua, **häälestades laohalduse seadistuse \> lao \> asukoha \> vormingud**. Lisateavet lugege teemast [Asukohtade konfigureerimine WMS-loaga laos](tasks/configure-locations-wms-enabled-warehouse.md).
    - **Asukoha tüüp** : valige laohalduse **parameetrite lehel pakkimisasukoha tüübina seadistatud asukoha tüüp, nagu on selles artiklis** varem kirjeldatud.
    - **Kasuta litsentsiplaadi jälgimist** – pakkimisasukohtade jaoks seadke selle valiku väärtuseks *Jah*. Süsteem peab saama jälgida litsentsiplaadi ID-sid pakkimisasukohtades, et see saaks pakkimisprotsessi juhtida.
    - **Luba negatiivne laovaru** – pakkimisasukohtade puhul määrake selle valiku väärtuseks *Ei*.
    - **Luba segaühikud** – määrake pakkimisasukohtade jaoks see valik väärtusele *Jah*. See säte on vajalik, kuna paljud erinevad kaubakoodid tuuakse tavaliselt samaaegselt pakkimisasukohta.
    - **Luba lao segaolekud** – pakkimisasukohtade jaoks seadke selle valiku väärtuseks *Jah*. See säte on vajalik, kuna erinevate varude olekuga kaubad tuuakse tavaliselt samaaegselt pakkimiskohtadesse.
    - **Luba lao segapartiid** – pakkimisasukohtade jaoks seadke selle valiku väärtuseks *Jah*. See valik seatakse automaatselt väärtusele *Jah,* kui suvandi **Luba segatud kaubad** väärtuseks on seatud *Jah*.

#### <a name="set-up-packing-locations"></a>Pakkimisasukohtade häälestamine

Teil peab olema vähemalt üks asukoht *, kus* töötajad panevad konteineritesse pakitavad laovarud.

Pakkimisasukoha lisamiseks järgige neid samme.

1. Avage **Laohaldus \> Seadistus \> Ladu \> Asukohad**.
1. Tegevuspaanil valige asukoha **lisamiseks** suvand Uus.
1. Seadke uuele asukohale järgmised väljad:

    - **Ladu**: määrake ladu, kus pakkimise asukoht peab olemas olema.
    - **Asukoht** : sisestage uue asukoha nimi.
    - **Asukoha profiili ID – määrake kindlasti eelmises jaotises loodud ID**.

## <a name="set-up-the-packing-process"></a>Pakkimisprotsessi häälestamine

See jaotis kirjeldab, kuidas konfigureerida sätteid, mis võimaldavad pakkimisprotsessi ja võimaldavad töötajatel varusid konteineritesse pakkida.

### <a name="set-up-container-packing-policies"></a><a name="packing-policy"></a>Konteineri pakkimise poliitikate seadistamine

Iga *konteineri pakkimispoliitika* määratleb konteineri töötlemise põhimõtted. Iga kord kui loote uue konteineri, valite sellele rakendamiseks ka konteineri pakkimispoliitika.

Konteineri pakkimispoliitika häälestamiseks tehke järgmist.

1. Avage jaotis **Laohaldus \> Seadistus \> Konteinerid \> Konteineri pakkimise poliitikad**.
1. Valige loendipaanilt olemasolev poliitika või valige **uue poliitika** loomiseks tegevuspaanil uus.
1. Määrake uue või valitud poliitika päises järgmised väärtused:

    - **Konteineri pakkimispoliitika** – sisestage poliitikale kordumatu nimi.
    - **Kirjeldus** – sisestage poliitika kirjeldav nimi.

1. **Seadke vahekaardil** Ülevaade järgmised väljad. Need väljad lasevad teil määrata, milliseid tegevusi tuleks konteineri sulgemisel teha, kas töötada töö loomisega või ilma ning millal konteiner tuleb pakkimisjaamast vabastada.

    - **Ladu** : valige ladu, kus pakkimispoliitikat rakendatakse.
    - **Lõppsaadetise vaikeasukoht** – määrake konteineri eelistatud asukoht pärast selle sulgemist. See väli on saadaval ainult siis, kui **konteineri** vabastamise poliitika väli on *seatud tegema kättesaadavaks saadetise lõppsihtkohas*.
    - **Sortimise vaikeasukoht** – seda välja kasutatakse väljamineva [sortimise võimalusega](outbound-sorting.md).
    - **Kaaluühik** – valige konteineri sulgemisel ja manifestimisel kasutamiseks vaikimisi mõõtühik. Tavaliselt on see mõõtühik mõõtühik, mida pakkimisjaamas kaalus kasutab. See väli kehtib töö loomisega või ilma selleta poliitikatele.
    - **Konteineri sulgemise** poliitika – valige üks järgmistest suvanditest, et määrata, mis peaks toimuma konteineri sulgemisel:

        - *Automaatne vabastamine* – konteiner vabastatakse **pakkimisjaamast** ja käivitatakse konteineri vabastamise poliitika väljal määratud tegevus.
        - *Hilinenud* vabastus – konteinerit ei vabastata kohe pakkimisjaamast. Laotöötaja peab selle hiljem käsitsi vabastama.
        - *Valikuline* : kui töötaja sulgeb konteineri, on neil võimalik valida, kas konteiner tuleb vabastada.

        Kui pakkimisjaam tegeleb peamiselt ühe kaubakonteineriga, mis lähetatakse otse klientidele, on kõige loomulikum lähenemine konteinerite kohe välja vabastusele. Kui pakkimisjaam käsitseb saadetisi, mis koosnevad mitmest konteinerist või isegi kaubaalusest, on võimalik vabastamisega viivitada, kuni kogu saadetis või kaubaalus on pakitud ja on komplekteerimisks valmis.

    - **Konteineri vabastamise** poliitika – valige üks järgmistest suvanditest, et määrata, mis peaks toimuma, kui konteiner vabastatakse pakkimisasukeskusest:

        - *Tehke see kättesaadavaks saadetise lõppsihtkohas* : uuendage konteiner saadetise lõppsihtkohaks. Kui valite selle suvandi, kasutage **lõppsaadetise** välja vaikeasukohta, et määrata konteinerile pärast selle sulgemist eelistatud asukoht.
        - *Looge töö konteineri teisaldamiseks pakkimisjaamast* – looge töö, et liigutada konteiner pakkimisjaamast pakkejaamast pakkealasse või otse välisustesse. Kasutage töömalli **välja**, et määrata töömall, mis tuleks rakendada konteineri töö loomisel.
        - *Määra konteiner väljaminevale sortimispositsioonile* – seda valikut kasutatakse väljamineva [sortimise](outbound-sorting.md) võimalusega.

        Enamasti on soovitatav luua töö konteinerite teisaldamiseks, sest selline lähenemine esindab paremini laos tegelikke käsitsi protsesse. Kuid lihtsate stsenaariumide puhul või olukorras, kus pakkejaam asub otse windows-ukse alal, võib eelistada, et konteiner oleks saadetise lõppsihtkohas kohe saadaval.

    - **Töömall** – valige töömall, mis rakendatakse konteineri töö loomisel. See väli on saadaval **ainult** *·* *siis, kui konteineri vabastamise poliitika väli on seatud looma tööd konteineri teisaldamiseks pakkimisjaamast ja töötellimuse tüübiga, mille nimi on Pakitud konteineri komplekteerimine.* Lisateavet vt töömallidest [ja asukohadirektiividest](control-warehouse-location-directives.md).

    Ülejäänud sammudes konfigureerite manifestiga seotud *sätted*. Manifesti loomine on konteineri, konteinerigrupi või saadetise kaalu ja transpordipakkujalt saadud jälgimis-ID määramise protsess. Dynamics 365 Supply Chain Management ei integreeru transpordipakkuja välissüsteemidega. Selle asemel peavad laotöötajad printima transpordipakkujalt saadud sildid ja siis skannima jälgimisnumbri, kui nad manifesti protseduuri läbivad.

    Kuna manifestinõuded varieeruvad klienditi ja isegi saadetisest saadetiseni, lubavad pakkimispoliitikad olulist paindlikkust töövoos. Saate luua konteinerite, konteinerigruppide ja saadetiste manifeste mis tahes kombinatsioonis.

    Kui kasutate mitmetasemelist manifesti protseduuri, peavad töötajad manifesti kõik konteinerid enne kui nad manifesti seotud konteinerigrupis peavad olema ja need peavad manifesti kõik konteinerigrupid enne, kui nad seotud saadetise manifesti teevad.

1. **Seadke konteineri manifesti** kiirkaardil järgmised väljad:

    - **Automaatne manifest konteineri sulgemisel** – valige see suvand väärtusele *Jah,* et rakendada manifesti teavet konteineri sulgemise protsessi osana. Kui te ei kasuta transpordi integratsiooni, tuleb teave käsitsi salvestada.
    - **Konteineri nõuete manifestimine** – valige üks järgmistest suvanditest:

        - *Pole* – manifestiprotsessi ei kasutata.
        - *Käsitsi* : pakkimise töövoog peab manifesti lisama. Süsteem ei luba konteinerit enne manifesti lõpetamist sulgeda ega vabastada.
        - *Transpordihaldus* – manifestimine toimub transpordihalduse (TMS) määra mootorite kaudu. Kuna see valik nõuab kohandatud arendust, et rakendada transpordipakkujale konkreetset mootorit, ei tööta see praeguses versioonis väljast välja.

    - **Prindi konteineri** sisu: kui soovite, *et* konteineri sulgemisel prinditakse konteineri sisu automaatselt, prinditakse selle suvandi väärtuseks Jah. Aruande saab printida ka nõudmisel.

1. **Valige konteinerigrupi manifesti** kiirkaardi väljal **Konteinerigrupi** manifesti nõuded üks järgmistest suvanditest:

    - *Pole* – konteinerigrupi manifesti ei lisata pakkimise töövoo nõudena.
    - *Käsitsi* – konteinerigrupi manifest kaasatakse pakkimise töövoo nõudena. Enne grupi manifesti saatmist tuleb sulgeda kõik gruppi kaasatud konteinerid. Valige see suvand, kui peate täitma manifesti iga konteinerigrupi kohta, mis on pakkimisjaamas pakitud. Tavaliselt valite selle suvandi, kui konteinerid on pakitud kaubaalusele ja kogu kaubaalus on manifestiks.

    > [!NOTE]
    > Praegune versioon ei toeta konteinerigruppide manifesti aruandeid ja konteinerigruppidel puudub TMS-i mootori tugi.

1. Seadke saadetise **manifesti** kiirkaardil järgmised väljad:

    - **Saadetise nõuete manifestimine** – valige üks järgmistest suvanditest:

        - *Pole* – saadetise manifesti ei lisata pakkimise töövoo nõudena.
        - *Käsitsi* – saadetise manifest kaasatakse pakkimise töövoo nõudena. Enne manifesti lõpetamist ei saa saadetise jaoks ühtki konteinerit vabastada.
        - *Transpordihaldus* – manifestimine toimub TMS-i määra mootorite kaudu. Kuna see valik nõuab kohandatud arendust, et rakendada transpordipakkujale konkreetset mootorit, ei tööta see praeguses versioonis väljast välja.

        Saadetise manifestimine peab olema lubatud, kui teilt nõutakse kogu pakkimisjaamas pakitud saadetise manifesti lõpule viimist. Seda kasutatakse tavaliselt siis, kui nõutav on üks konsolideeritud manifest, isegi kui saadetis koosneb mitmest konteinerist või konteinerigrupist.

    - **Prindi saateleht** : määrake selle suvandi väärtuseks *Jah,* et saateleht automaatselt saadetise manifesti osana printida. Saatelehe saab printida ka nõudmisel.

### <a name="set-up-container-types"></a>Konteineri tüüpide seadistamine

Käsitsi pakkimisprotsessi ajal tuleb luua konteinerid enne, kui kaupu saab pakkida. Iga konteiner peab põhinema konteineri *tüübil*, mis määrab konteineri maksimaalse füüsilise mahu- ja kaaluvõimsuse.

Konteineritüübi loomiseks järgige neid samme.

1. Minge laohalduse **häälestuse \> konteineritüüpide \>\> juurde**.
1. Konteineritüübi lisamiseks valige **toimingupaanil** suvand Uus.
1. Seadke uuele konteineritüübile järgmised väljad:

    - **Konteineri tüübi** kood – sisestage konteineritüübi kordumatu ID.
    - **Kirjeldus** – sisestage uue konteineritüübi kirjeldus.
    - **Taakaal** – sisestage konteineri tegelik või hinnanguline kaal.
    - **Maksimaalne netokaal** – sisestage max kaal, mida konteiner maakleb.

1. Sisestage **konteineri dimensioonide** jaotise väljadele **Pikkus**, **Laius**, **·** **Kõrgus ja Maht** konteineri enda füüsilised dimensioonid.
1. Sisestage **jaotise Maksimumid** väljadele **Pikkus**, **Laius**, **Kõrgus** **ja Maht** maksimaalsed füüsilised dimensioonid, mida konteiner suudab käsitseda.
1. Saate määrata lisaatribuudid konteineritüüpidele, mis on seotud teiste konteineriid kasutavad operatsioonidega. Lisateavet vt teemast [Konteinerite kogumine](wave-containerization.md).

> [!NOTE]
> Käsitsi pakkimisprotsessi puhul kasutab süsteem **ainult välja Maksimaalne netokaal** **·** **väärtust** ja jaotises Maksimumid välja Maht väärtust.

### <a name="set-up-packing-profiles"></a>Pakkimisprofiilide seadistamine

*Pakkimisprotsessis* on pakkimisprofiilid nõutavad. Neid saab valida või määrata vaikimisi, kui alustate pakketoimingut lehel **Pakkimine**.

Pakkimisprofiili häälestamiseks tehke järgmist.

1. Avage jaotis **Laohaldus \> Seadistus \> Pakkimine \> Pakkimisprofiilid**.
1. Valige loendipaanilt olemasolev profiil või **valige** uue reegli loomiseks tegevuspaanil uus.
1. Seadke uue või valitud reegli päises järgmised väljad:

    - **Pakkimisprofiili ID** – sisestage profiili lühike ID.
    - **Kirjeldus** : sisestage pakkimisprofiili kirjeldus.
    - **Konteineri pakkimise** poliitika – valige profiilile rakenduv pakkimispoliitika. Lisateavet vt selle artikli jaotisest [Konteineri pakkimise](#packing-policy) poliitikate häälestamine.
    - **Konteineri ID režiim – valige, kas konteineri loomisel luuakse konteineri ID** automaatselt või tuleb see käsitsi luua.
    - **Konteineri** tüüp: valige konteineri tüüp, mida kasutatakse vaikimisi uue konteineri loomisel.
    - **Loo konteineri sulgemisel konteiner** automaatselt – märkige see ruut, et luua automaatselt uus konteiner, kui eelmine konteiner on suletud ja praegusesse saadetise jääb üks või mitu rida.

### <a name="set-up-warehouse-workers"></a>Laotöötajate häälestada

Igal **kasutajal** *·* *või töötajal, kes pakib konteinereid, kasutades veebikliendi pakkelehte või pakkimistegevuse koodi laohalduse mobiilirakenduses, peab olema kasutajakonto, mis on seotud töötaja/* isiku kirjega, millele on määratud nõutavad turbejuurdepääsu õigused. (Lisateavet kasutajate häälestamise kohta vt teemast [Saate luua uusi kasutajaid](../../fin-ops-core/dev-itpro/sysadmin/tasks/create-new-users.md).

Pakkeprotsessi jaoks töötaja */isiku kirje häälestamiseks* järgige neid samme.

1. Avage jaotis **Laohaldus \> Seadistus \> Töötaja**.
1. Töö kasutaja lisamiseks valige toimingupaanil **suvand** Uus.
1. Seadke väli **Töötaja** olemasolevale töötajakirjele, mis **on inimressursside moodulis** määratud kasutaja jaoks, kes pakkimisprotsessi lõpetab.
1. Määrake FastTab **Profiilil** järgmised väljad:

    - **Konteineri pakkimise poliitika** – valige konteineri pakkimispoliitika, mis määratleb, kuidas pakkejaama konteinereid tuleb töödelda. Valitud konteineri pakkimispoliitika eel valitakse töötajale, kui ta avab pakkimisjaama. Lisateavet vt järgmisest postitusest: täiustatud [pakkimisfunktsioon](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611).
    - **Pakkimisprofiili ID** – valige pakkimisprofiili ID, mis määratleb kasutatava pakkimispoliitika ja konteineri sätted. Kui valitud pakkimisprofiili ID on seostatud konteineri pakkimispoliitikaga, **ei** saa te muuta konteineri pakkimise poliitika välja sätet sellel lehel.

1. Pakkejaama **vaikekaardil** valige töötajale vaikimisi laoala, ladu ja asukoht.
1. Kui töötaja kasutab laohalduse mobiilirakendust, et hallata ja registreerida oma konteinerite pakkimistöid, **seadistage** kiirkaardil Kasutajad üks või mitu kontot, mida töötaja saab rakendusele sisse logida. Lisateavet vt mobiilse seadme [kasutajakontodest](mobile-device-work-users.md).

## <a name="example-scenario"></a><a name="scenario"></a>Näidisstsenaarium

See jaotis annab näide stsenaariumi, mis näitab, kuidas luua tellimus ja pakkida kaupu.

### <a name="make-sample-data-available"></a>Näidisandmete kättesaadavaks tegemine

Selle stsenaariumi kasutamiseks siin määratud näidiskirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/fin-ops/get-started/demo-data.md). Enne alustamist peate valima ka juriidilise isiku **USMF**.

Seda stsenaariumi saate kasutada ka tootmissüsteemis funktsiooni kasutamise juhistena. Sel juhul tuleb teil siiski sisestada oma väärtused iga siin kirjeldatud sätte jaoks.

### <a name="sign-in-as-a-user-that-can-do-packing-work"></a>Logige sisse kasutajana, kes saab tööd pakkida.

Logige tarneahela haldusse sisse, kasutades kasutajakontot, kus on konteinerite pakkimiseks vajalikud load. *Kasutaja Funderburk* on kaasatud demoandmete osana ja tal on vajalikud load. Sellel kasutajal on kasutaja ID *Admin*.

### <a name="create-a-sales-order-and-complete-the-work"></a>Müügitellimuse loomine ja töö lõpule viimine

Järgige neid samme müügitellimuse loomiseks ja lõpetage tellitud kaupade pakkimisjaama teisaldamise töö.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Valige toimingupaanil nupp **Uus**.
1. Valige dialoogiboksi **Müügitellimuse loomine** väljal **Kliendi konto** suvand *US-005*.
1. Valige dialoogiboksi sulgemiseks suvand **OK**.
1. Uus müügitellimus avatakse ja selle kiirkaardil Müügitellimus on üks **tühi** rida. Seadistage uuele tellimusereale järgmised väärtused:

    - **Kauba kood:** *A0001*
    - **Kogus:** *2*
    - **Tegevuskoht:** *6*
    - **Ladu:** *62*

1. Kui tellimuse rida on endiselt valitud, valige **kiirkaardi \>** Müügitellimus read tööriistaribal **suvand Varude reserveerimine**.
1. Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida laos kogu valitud rea kogus.
1. Müügitellimuse juurde naasmiseks sulgege leht **Reserveerimine**.
1. Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.

    Teade kuvab tellimuse saadetise ja voo ID-d.

1. Kui tellimuse rida on veel valitud, valige **müügitellimuse** \> **ridade kiirkaardi** tööriistaribal **lao töö** üksikasjad. Kui kasutate oma lainete käitamiseks pakktöötlust, võib olla vaja oodata lühikest aega töö loomiseni.
1. **Tööpaanil** oleval töö lehel valige **vahekaart** Lõpetatud **töö**.
1. Seadke töö **lõpetamise lehel välja** Kasutaja ID väärtuseks **62** *·*.
1. Tegevuspaanil valige valideeri **töö**.
1. Kui saate teate, mis näitab, et teie töö on kehtiv, valige täielik töö lao **kaupade** komplekteerimise lõpuleviimiseks *ja nende pakkimiskohta viimiseks*.
1. Tehke märkus saadetise **ID väärtuse kohta**, mis kuvatakse ülemises ruudustikus töö puhul.

### <a name="pack-the-ordered-items-into-a-container"></a>Paki tellitud kaubad konteinerisse

Laokauba koht on nüüd pakkimisalale toodud ja valmis konteineritesse pakkimiseks. Järgige neid samme, et luua süsteemis uus konteiner ja pakkida see.

1. Avage jaotis **Laohaldus \> Pakkimine ja konteinerisse paigutamine \> Pakkimine**.
1. Dialoogiboksis **Pakkimisjaama valimine** määrake järgmised väärtused.

    - **Tegevuskoht:** *6*
    - **Ladu:** *62*
    - **Asukoht:** *Pakkimine*
    - **Pakkimisprofiili ID:** *WH62*

1. Valige nupp **OK**.
1. Pakkelehe **litsentsiplaadil** **või saadetise väljal** sisestage saadetise ID, mille olete varem märkinud. Järelejäänud lahtipakkimata kaupu peaksite nüüd kuvama kiirkaardil **Avatud read**.
1. Tegevuspaanil valige süsteemis **konteineri** loomiseks uus konteiner.
1. **Uue konteineri dialoogiboksi ID-s** seadke konteineritüübi **välja väärtuseks** *SmallBox*.
1. Valige **konteineri loomiseks OK**.
1. Valige **OK**, et naasta **pakkelehele**. Avatud **konteinerite** kiirkaardil kuvatakse **nüüd loodud konteineri ID** väärtus.
1. Selle stsenaariumi puhul pakite ainult ühe tellitud kauba praegu. Seetõttu seadke kauba **pakkimise** kiirkaardil järgmised väärtused:

    - **Kogus:** *1.00*
    - **Identifikaator:** *A0001*

    Kohe pärast ID väärtuse **märkimist** **uuendab leht avatud ridu** **ja** kõiki ridade kiirkaarte, näitamaks, et üks kaup on pakitud. Nüüd peaksite pakkima ühe kauba *A0001 kahest tükist*.

1. Valige toimingupaanil nupp **Sule konteiner**.
1. Konteineri **sulgemise dialoogiboksis** valige väärtus Too **süsteemikaal,** et täita vaikimisi brutokaalu **väärtus**.
1. Valige **konteineri sulgemiseks OK**.

> [!TIP]
> Kontekstipõhiste konteinerite vaatamiseks on mitmeid viise. Näiteks saadetise pakkimisel on sageli kasulik vaadata kas konteinereid, mis on saadetise osa, või kõiki konteinereid, mis on pakkimisjaamas füüsiliselt olemas. Pakkimisjaama **lehel** on nupud, mida saate kasutada pakkimisjaamas kõigi avatud ja suletud konteinerite vaatamiseks. Need vaated ei ole piiratud konkreetse saadetisega. Need võivad olla väga kasulikud olukorras, kus üks töötaja pakib konteinerit ning teine töötaja manifestis ja vabastab konteineri.
>
> Saadaval on ka kõigi konteinerite konsolideeritud vaade. See vaade on kasulik enamasti kasutajatele, kes töötavad väljaspool ühe pakkimisjaama konteksti. Selle näeks minge laohalduse pakkimis **- ja \> konteineritesse pakkimise konteineritesse \>**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
