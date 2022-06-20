---
title: Reisi loomise üksused
description: See artikkel annab teavet reisi loomise andmeüksuste kohta, mis grupeerivad andmeüksused, mis on vajalikud tööreisi loomiseks.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: cb2e2f53942015caf9462692515f24deb9689aed
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873894"
---
# <a name="voyage-creation-entities"></a>Reisi loomise üksused

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

Reisi loomise andmeüksused grupeerivad kokku andmeüksused, mis on vajalikud töö reisi loomiseks. Teie või teie ekspediitori saate kasutada neid andmeüksuseid reisi, konteineri saatmise, foolio ja reisirea kirjete loomiseks, mis viidatakse olemasolevatele sisseostjate tellimustele või üleviimistellimuse ridadele.

## <a name="voyages-itmtableentity"></a>Reisid (ITMTableEntity)

Reisi puhul tähistab reisi sissetulevate kaupade vedu ja toimib väljaminekukulu kõrgeima taseme kulualana. See sisaldab päise taseme teavet, mis on seotud laeva, päritolu pordi ja sihtportiga. Üksus toetab seda `ITMTableEntity` funktsiooni. Järgmises tabelis loetletakse väljad ja vastendamised, mis selle üksuse teete.

| Nimi | Vastendamine | Andmetüüp | Võti | Kohustuslik |
|---|---|---|---|---|
| Tarneviis | ItmTable.DlvModeId | Nvarchar(10) | Nr | Nr |
| Maakleri soovitus | ITMTable.ITMBrokerAdvised | Kuupäev ja kellaaeg | Nr | Nr |
| Kliendiga kohtumine | ItmTable.ITMCustomerAppointment | Kuupäev ja kellaaeg | Nr | Nr |
| Lattu tarnitud | ITMTable.ITMDelAtWarekoda | Kuupäev ja kellaaeg | Nr | Nr |
| Tarnejuhised | ITMTable.ITMDeliveryInstructions | Kuupäev ja kellaaeg | Nr | Nr |
| Väljumiskuupäev | ITMTable.ITMDepartureDate | Kuupäev ja kellaaeg | Nr | Nr |
| Kaubad on vabastatud | ItmTable.ITMGoodsReleased | Kuupäev ja kellaaeg | Nr | Nr |
| Kohaliku transpordi kuupäev | ItmTable.ITMLocalTransportDate | Kuupäev ja kellaaeg | Nr | Nr |
| Kohaliku transpordi kellaaeg | ItmTable.ITMLocalTransportTime | Int | Nr | Nr |
| Algne veokiri on saadetud | ITMTable.ITMOriginalBOLSebt | Kuupäev ja kellaaeg | Nr | Nr |
| Algdokumendid on vastu võetud | ITMTable.ITMOriginalDocsReceived | Kuupäev ja kellaaeg | Nr | Nr |
| Ostutellimuse olek | ItmTable.ITMPurchStatus | Int | Nr | Nr |
| Kinnitamise kuupäev | ITMTable.ITMVerificationDate | Kuupäev ja kellaaeg | Nr | Nr |
| Tollikirje identifikaator | ITMTable.ShipCustomsEntryId | Nvarchar(20) | Nr | Nr |
| Lähetuskuupäev | ITMTable.ShipDate | Kuupäev ja kellaaeg | Nr | Nr |
| Kirjeldus | ITMTable.ShipDescription | Nvarchar(60) | Nr | Nr |
| Dokumendid on vastu võetud | ITMTable.ShipDocReceived | Int | Nr | Nr |
| Eeldatav tarnekuupäev | ITMTable.ShipEstDlvDate | Kuupäev ja kellaaeg | Nr | Nr |
| Arvatav saabumisaeg sadamas | ITMTable.ShipEstPortDate | Kuupäev ja kellaaeg | Nr | Nr |
| Lähtesadam | ITMTable.ShipFromPort | Nvarchar(20) | Nr | Nr |
| Maja õhutee / veoarve | ITMTable.ShipHAWB | Nvarchar(20) | Nr | Nr |
| Reis | ITMTable.ShipId | Nvarchar(20) | **Jah** | **Jah** |
| Reserveerimise viide | ITMTable.ShipIdExternal | Nvarchar(20) | Nr | Nr |
| Teekonna mall | ITMTable.ShipJourlähetusId | Nvarchar(20) | Nr | Nr |
| Kohalik ekspediitor | ITMTable.ShipLocalForwarder | Nvarchar(20) | Nr | Nr |
| Põhitranspordi lennutee / veodokument | ITMTable.ShipMAWB | Nvarchar(20) | Nr | Nr |
| Mõõtmine | ITMTable.ShipMeasurement | Numbriline(32, 6) | Nr | Nr |
| Mõõtühik | ITMTable.ShipMeasurementUnit | Int | Nr | Nr |
| Kaubaaluste arv | ITMTable.ShipNoOfPallets | Int | Nr | Nr |
| Ootel reis | ITMTable.ShipPending | Int | Nr | Nr |
| Märkused | ITMTable.ShipRemarks | Nvarchar(MAX) | Nr | Nr |
| Rent | ITMTable.ShipRental | Int | Nr | Nr |
| Reisi olek | ITMTable.ShipStatusId | Nvarchar(20) | Nr | Nr |
| Paljune numbris | ITMTable.ShiptallyInNumber | Nvarchar(20) | Nr | Nr |
| Sihtsadam | ITMTable.ShipToPort | Nvarchar(20) | Nr | Nr |
| Hindamise kuupäev | ITMTable.ShipValuationDate | Kuupäev ja kellaaeg | Nr | Nr |
| Saatmisettevõte | ITMTable.ShipVendAccount | Nvarchar(20) | Nr | Nr |
| Laev | ITMTable.ShipVesselId | Nvarchar(20) | Nr | **Jah** |
| Välise reisi ID | ITMTable.ShipVoyage | Nvarchar(20) | Nr | Nr |

### <a name="number-sequences-for-voyages"></a>Reiside numbriseeriad

Reisi ID-de eraldamist reguleerib ühiskasutusega numbriseeria.

Väärtus, mis edastatakse andmeüksusele reisi **ID** (`ShipId`)väärtusena, kasutatakse olemasoleva kirje tuvastamiseks värskendamiseks. Kui seda kirjet pole olemas, sõltub käitumine sellest, kas määratud numbriseeria on konfigureeritud lubama käsitsi sisestamist:

- Kui käsitsi sisestus on lubatud, luuakse uus kirje, mis kasutab edastatud väärtust.
- Kui käsitsi sisestus pole lubatud, kasutatakse edastatud väärtuse asemel määratud numbriseeria järgmist numbrit.

Impordiseansi ajal säilitatakse reisi ID-de säilitamisel imporditud kohatäitja väärtus. Selline käitumine tagab, et kohatäitjale viidatud saadetise konteiner ja reisi read kaasatakse reisi ning et need värskendatakse, et kajastada väärtust, mis on määratud numbriseeriast.

### <a name="automatic-cost-transactions"></a>Automaatsed kulukanded

Automaatseid kulusid saab reisile lisada **Microsofti automaatsete** Dynamics 365 Supply Chain Management kulude lehest (**omahinnale omahinna \> seadistamise automaatne \> kulu**). Automaatsete kulude kirjeid saab luua ka kasutades kulukande andmeüksuseid igale kulualale, mida väljaminev kulu toetab.

Automaatseid tarneahela halduses konfigureeritud kulusid rakendatakse reisile reisirea loomisel. Kirje kohta ei kuvata kulusid enne, kui päisekirje on seostatud reateabega.

## <a name="shipping-containers-itmcontainersentity"></a>Konteinerite lähetamine (ITMContainersEntity)

Saatmiskonteineriks on füüsiline konteiner, kus kaupu transporditakse. See füüsiline konteiner võib olla veose konteiner veose jaoks või üks kaubaalus lennutranspordi jaoks. Saadetise konteiner sisaldab päise taseme teavet, mis on seotud saadetise konteineri ID, pitsati numbri ja saadetise konteineri tüübiga. (Saatmiskonteineri tüüp annab dimensiooniteavet.) Üksus toetab seda `ITMContainersEntity` funktsiooni. Järgmises tabelis loetletakse väljad ja vastendamised, mis selle üksuse teete.

| Nimi | Vastendamine | Andmetüüp | Võti | Kohustuslik |
|---|---|---|---|---|
| Väljumiskuupäev | ITMContainers.ITMDepartureDate | Kuupäev ja kellaaeg | Nr | Nr |
| Kohaliku transpordi kuupäev | ITMContainers.ITMLocalTransportDate | Kuupäev ja kellaaeg | Nr | Nr |
| Kohaliku transpordi kellaaeg | ITMContainers.ITMLocalTransportTime | Int | Nr | Nr |
| Algne reis | ITMContainers.OrigShipId | Nvarchar(20) | Nr | Nr |
| Tegelik kaal | ITMContainers.ShipActualWeight | Numbriline(32, 6) | Nr | Nr |
| Maakleri soovitus | ITMContainers.ShipBrokerAdvised | Kuupäev ja kellaaeg | Nr | Nr |
| Saatmiskonteiner | ITMContainers.ShipContainerId | Nvarchar(20) | **Jah** | **Jah** |
| Saatmiskonteineri tüüp | ITMContainers.ShipContainerTypeId | Nvarchar(20) | Nr | Nr |
| Ühiku tüüp | ITMContainers.ShipContainerUnitTypeId | Nvarchar(10) | Nr | Nr |
| Teisendatud renditavaks | ITMContainers.ShipConvertedToRental | Int | Nr | Nr |
| Kliendiga kohtumine | ITMContainers.ShipCustomerAppointment | Kuupäev ja kellaaeg | Nr | Nr |
| Lähetuskuupäev | ITMContainers.ShipDate | Kuupäev ja kellaaeg | Nr | Nr |
| Lattu tarnitud | ITMContainers.ShipDelAtWareudu | Kuupäev ja kellaaeg | Nr | Nr |
| Tarnejuhised | ITMContainers.ShipDeliveryInstructions | Kuupäev ja kellaaeg | Nr | Nr |
| Ülevaatuse sertifikaadi rakendamise kuupäev | ITMContainers.ShipECAppliedDate | Kuupäev ja kellaaeg | Nr | Nr |
| Ülevaatuse sertifikaadi aegumise kuupäev | ITMContainers.ShipECExpiryDate | Kuupäev ja kellaaeg | Nr | Nr |
| Ülevaatuse sertifikaadi number | ITMContainers.ShipECNum | Nvarchar(20) | Nr | Nr |
| Ülevaatuse sertifikaadi kättesaamise kuupäev | ITMContainers.ShipECReceivedDate | Kuupäev ja kellaaeg | Nr | Nr |
| Eeldatav tarnekuupäev | ITMContainers.ShipEstDlvDate | Kuupäev ja kellaaeg | Nr | Nr |
| Arvatav saabumisaeg sadamas | ITMContainers.ShipEstPortDate | Kuupäev ja kellaaeg | Nr | Nr |
| Eeldatav laadimiskuupäev | ITMContainers.ShipExpectedLoadingDate | Kuupäev ja kellaaeg | Nr | Nr |
| Lähtesadam | ITMContainers.ShipFromPort | Nvarchar(20) | Nr | Nr |
| Kauba kirjeldus | ITMContainers.ShipGoodsDesc | Nvarchar(60) | Nr | Nr |
| Kaubad on vabastatud | ITMContainers.ShipGoodsReleased | Kuupäev ja kellaaeg | Nr | Nr |
| GPS-jälgimisseade | ITMContainers.ShipGPSUnit | Nvarchar(30) | Nr | Nr |
| Maja õhutee / veoarve | ITMContainers.ShipHAWB | Nvarchar(20) | Nr | Nr |
| Reis | ITMContainers.ShipId | Nvarchar(20) | **Jah** | **Jah** |
| Teekonna mall | ITMContainers.ShipJourjourId | Nvarchar(20) | Nr | Nr |
| Kohalik ekspediitor | ITMContainers.ShipLocalForwarder | Nvarchar(20) | Nr | Nr |
| Mõõtmine | ITMContainers.ShipMeasurement | Numbriline(32, 6) | Nr | Nr |
| Mõõtühik | ITMContainers.ShipMeasurementUnit | Int | Nr | Nr |
| Pakkide arv | ITMContainers.ShipNoOfCartons | Numbriline(32, 6) | Nr | Nr |
| Algne veokiri on saadetud | ITMContainers.ShipOriginalBOLSebt | Kuupäev ja kellaaeg | Nr | Nr |
| Algdokumendid on vastu võetud | ITMContainers.ShipOriginalDocsReceived | Kuupäev ja kellaaeg | Nr | Nr |
| Meie pitsatinumber | ITMContainers.ShipLähetusSealNum | Nvarchar(20) | Nr | Nr |
| Kasutatud | ITMContainers.ShipPendingUsed | Int | Nr | Nr |
| Ostutellimuse olek | ITMContainers.ShipPurchStatus | Int | Nr | Nr |
| Külmutuse tüüp | ITMContainers.ShipRefrigerationTypeId | Nvarchar(10) | Nr | Nr |
| Märkused | ITMContainers.ShipRemarks | Nvarchar(MAX) | Nr | Nr |
| Rent | ITMContainers.ShipRental | Int | Nr | Nr |
| Tagastatav | ITMContainers.ShipReturnable | Int | Nr | Nr |
| Reisi olek | ITMContainers.ShipStatusId | Nvarchar(20) | Nr | Nr |
| Saatmisettevõtte pitsatinumber | ITMContainers.ShipTheirSealNum | Nvarchar(20) | Nr | Nr |
| Sihtsadam | ITMContainers.ShipToPort | Nvarchar(20) | Nr | Nr |
| Kinnitamise kuupäev | ITMContainers.ShipVerificationDate | Kuupäev ja kellaaeg | Nr | Nr |
| Laev | ITMContainers.ShipVesselId | Nvarchar(20) | Nr | **Jah** |

### <a name="voyage-id-validation"></a>Reisi ID kinnitamine

Saatmiskonteineri ID-d ei juhi numbriseeria. See on kordumatu ainult reisi kontekstis, kus seda kasutatakse.

Kui konteineri saatmise üksust (`ITMContainersEntity`) kasutatakse reisiüksusest (`ITMTableEntity`) sõltumatult, **peab reisi ID** (`ShipId`) väärtus ühtima reisitabelis olemasoleva kirjega. Vastasel juhul importimine nurjub.

Kui konteineri saatmise üksust (`ITMContainersEntity`) ja reisiüksust (`ITMTableEntity`) kasutatakse osana samast impordiseansist, peab reisiüksus enne saadetise konteineri loomist. Vastasel juhul ei **saa reisi ID** (`ShipId`) väärtust edukalt kinnitada. Kui reisi **ID (**) väärtuseks on kasutatud kohatäitja väärtust, saab seost luua ainult siis, `ShipId` kui saadetise konteineri üksuses kasutatakse sama kohatäitja väärtust, mida kasutatakse reisi **ID** (`ShipId`) väärtuses.

### <a name="other-field-validations"></a>Muud välja kinnitamised

Järgmine tabel näitab väljasid lähetuskonteinerite tabelis (`ITMContainers`), mida kontrollitakse väljaminev kulu seadistustabelite suhtes. See näitab ka väljasaadetud kuluandmete üksusi, mida ekspediiter saab kasutada olemasolevate väärtuste lugemiseks ja tagamaks, et kehtivad väärtused on teie keskkonnas vastu võetud.

| Väli tabelis ITMContainers | Väljaminev kuluandmete üksus |
|---|---|
| Saatmiskonteineri tüüp | ITMShippingContainerTypeEntity |
| Kauba kirjeldus | ItMGoodsDescriptionEntity |
| Külmutuse tüüp | Atribuut ITMShippingContainerRefrigerationTypeEntity |

## <a name="folios-itmfolioentity"></a>Foolokus (ITMFo foolEntity)

Foolio esindab kaupade grupeerimist konteineris tollideklaratsioonide eesmärkidel. Foolio sisaldab päise taseme teavet, mis on seotud tollimaakleriga ja kaupade kirjeldust. Üksus toetab seda `ITMFolioEntity` funktsiooni. Järgmises tabelis loetletakse väljad ja vastendamised, mis selle üksuse teete.

| Nimi | Vastendamine | Andmetüüp | Võti | Kohustuslik |
|---|---|---|---|---|
| Maakleri soovitus | ITMFomaakleriTable.ShipBrokerAdvised | Kuupäev ja kellaaeg | Nr | Nr |
| Lasti kontrollnumber | ITMFovahenditetable.ShipCargoControlNumber | Nvarchar(20) | Nr | Nr |
| Kliendiga kohtumine | ITMFoexiTable.ShipCustomerAppointment | Kuupäev ja kellaaeg | Nr | Nr |
| Tollimaakler | ITMFonicTable.ShipCustomsBroker | Nvarchar(20) | Nr | Nr |
| Tolli ID | ITMFonicTable.ShipCustomsId | Nvarchar(60) | Nr | Nr |
| Ettevõte | ITMFopiirkondTable.ShipDataArea | Nvarchar(4) | Nr | **Jah** |
| Lattu tarnitud | ITMFoedastusTable.ShipDelAtWareware, | Kuupäev ja kellaaeg | Nr | Nr |
| Tarnejuhised | ITMFointTable.ShipDeliveryInstructions | Kuupäev ja kellaaeg | Nr | Nr |
| Dokumendid on vastu võetud | ITMFoetiTable.ShipDocReceived | Int | Nr | Nr |
| Eeldatav tarnekuupäev | ITMFodalTable.ShipEstDlvDate | Kuupäev ja kellaaeg | Nr | Nr |
| Arvatav saabumisaeg sadamas | ITMFodalTable.ShipEstPortDate | Kuupäev ja kellaaeg | Nr | Nr |
| Eksportija | ITMFoexiTable.ShipExporterId | Nvarchar(20) | Nr | Nr |
| Nimi | ITMFoexiTable.ShipExporterName | Nvarchar(60) | Nr | Nr |
| Foolio kuupäev | ITMFodalTable.ShipFolähetusDate | Kuupäev ja kellaaeg | Nr | Nr |
| Foolio | ITMFohuTable.ShipFolähetusId | Nvarchar(20) | **Jah** | **Jah** |
| Lähtesadam | ITMFo liigendtabelit.ShipFromPort | Nvarchar(20) | Nr | Nr |
| Kauba kirjeldus | ITMFoaadidTable.ShipGoodsDesc | Nvarchar(60) | Nr | Nr |
| Kaubad on vabastatud | ITMFohuTable.ShipGoodsReleased | Kuupäev ja kellaaeg | Nr | Nr |
| Maja õhutee / veoarve | ITMFohutable.ShipHAWB | Nvarchar(20) | Nr | Nr |
| Reis | ITMFo teisendatavtable.ShipId | Nvarchar(20) | Nr | **Jah** |
| Mõõtmine | ITMFohuTable.ShipMeasurement | Numbriline(32, 6) | Nr | Nr |
| Mõõtühik | ITMFonioTable.ShipMeasurementUnit | Int | Nr | Nr |
| Pakkide arv | ITMFoixTable.ShipNoOfCartons | Numbriline(32, 6) | Nr | Nr |
| Algne veokiri on saadetud | ITMFoenoTable.ShipOriginalBOLSebt | Kuupäev ja kellaaeg | Nr | Nr |
| Algdokumendid on vastu võetud | ITMFoenoTable.ShipOriginalDocsReceived | Kuupäev ja kellaaeg | Nr | Nr |
| Ostutellimuse olek | ITMFohutable.ShipPurchStatus | Int | Nr | Nr |
| Märkused | ITMFosihtotstarbeliseTable.ShipRemarks | Nvarchar(MAX) | Nr | Nr |
| Reisi olek | ITMFoaadidTable.ShipStatusId | Nvarchar(20) | Nr | Nr |
| Tollimaksu kood | ITMForiffTable.ShipTariffCode | Nvarchar(10) | Nr | Nr |
| Sihtsadam | ITMFotoolTable.ShipToPort | Nvarchar(20) | Nr | Nr |
| Hindamise kuupäev | ITMFohuTable.ShipValuationDate | Kuupäev ja kellaaeg | Nr | Nr |
| Kinnitamise kuupäev | ITMFodalTable.ShipVerificationDate | Kuupäev ja kellaaeg | Nr | Nr |
| Hankija konto | ITMFo liigendtabelit.VendAccount | Nvarchar(20) | Nr | Nr |

### <a name="number-sequences-for-folios"></a>Fool siis, kui numbriseeriad on

Foolio ID-de eraldamist juhib foolio ID-de numbriseeria.

Väärtus, mis edastatakse andmeüksusele **Foolio ID** (`FolioId`) väärtusena, kasutatakse olemasoleva kirje tuvastamiseks värskendamiseks. Kui seda kirjet pole olemas, sõltub käitumine sellest, kas määratud numbriseeria on konfigureeritud lubama käsitsi sisestamist:

- Kui käsitsi sisestus on lubatud, luuakse uus kirje, mis kasutab edastatud väärtust.
- Kui käsitsi sisestus pole lubatud, kasutatakse edastatud väärtuse asemel määratud numbriseeria järgmist numbrit.

Impordiseansi ajal säilitatakse kohatäiteväärtus, mis imporditakse foolio ID-ga. Selline käitumine tagab, et kohatäitjale viidatud reisiread on õigesti seostatud ja et neid värskendatakse, et kajastada väärtust, mis on määratud numbriseeriast.

### <a name="field-validations"></a>Väljade kinnitamised

Kaupade **kirjelduse välja** foolio tabelis (`ITMFolioTable`) kontrollitakse sama nimega väljade kulu seadistustabeli suhtes. Ekspediiter saab kasutada välja `ITMGoodsDescriptionEntity` saadetud kulu andmeüksust olemasolevate väärtuste lugemiseks ja tagamaks, et kehtivad väärtused on teie keskkonnas vastu võetud.

## <a name="voyage-lines-for-purchase-orders-itmpurchaselineentity"></a>Ostutellimuste reisi read (ITMPurchaseLineEntity)

Reisirida tähistab ühte ostutellimuse rida, mis kaasatakse reisi. See seos luuakse ostutellimuse numbri **ja osturea** **numbri väljade** kaudu. Reisi rida viitab igale eelmisele kirjele, mis loodi reisi, saadetise konteineri ja foolio jaoks. Üksus toetab seda `ITMPurchaseLineEntity` funktsiooni. Järgmises tabelis loetletakse väljad ja vastendamised, mis selle üksuse teete.

| Nimi | Vastendamine | Andmetüüp | Võti | Kohustuslik |
|---|---|---|---|---|
| Valuuta | ITMLine.CurrencyCode | Nvarchar(3) | Nr | Nr |
| Netosumma | ITMLine.LineAmountMST | Numbriline(32, 6) | Nr | Nr |
| Osturea number | ITMLine.RefRecId | Numbriline(32, 6) | **Jah** | Nr |
| Saatmiskonteiner | ITMLine.ShipContainerId | Int | Nr | Nr |
| Ettevõte | ITMLine.ShipDataArea | Nvarchar(20) | **Jah** | Nr |
| Deklareeritud kogus | ITMLine.ShipDeclaredQty | Nvarchar(4) | Nr | Nr |
| Foolio | ITMLine.ShipFotelefoniId | Numbriline(32, 6) | Nr | Nr |
| Reis | ITMLine.ShipId | Nvarchar(20) | **Jah** | Nr |
| Kaubakood | ITMLine.ShipItemId | Nvarchar(20) | Nr | Nr |
| Mõõtmine | ITMLine.ShipMeasurement | Nvarchar(20) | Nr | Nr |
| Mõõtühik | ITMLine.ShipMeasurementUnit | Numbriline(32, 6) | Nr | Nr |
| Pakkide arv | ITMLine.ShipNoOfCartons | Int | Nr | Nr |
| Asukoht | ITMLine.ShipPosition | Numbriline(32, 6) | Nr | Nr |
| Kogus | ITMLine.ShipQty | Int | Nr | Nr |
| Ostutellimuse kood | ITMLine.TransRefId | Numbriline(32, 6) | **Jah** | Nr |
| Ühik | ITMLine.UnitId | Int | Nr | Nr |
| Helitugevus | ITMLine.Volume | Nvarchar(10) | Nr | Nr |
| Kaal | ITMLine.kaal | Numbriline(32, 6) | Nr | Nr |

## <a name="voyage-lines-for-transfer-orders-itmtransferlineentity"></a>Üleviimistellimuste reisi read (ITMTransferLineEntity)

Reisirida tähistab ühte üleviimistellimuse rida, mis kaasatakse reisi. See seos luuakse üleviimistellimuse **numbri ja üleviimisrea** **numbri väljade** kaudu. Reisi rida viitab igale eelmisele kirjele, mis loodi reisi, saadetise konteineri ja foolio jaoks. Üksus toetab seda `ITMTransferLineEntity` funktsiooni. Järgmises tabelis loetletakse väljad ja vastendamised, mis selle üksuse teete.

| Nimi | Vastendamine | Andmetüüp | Võti | Kohustuslik |
|---|---|---|---|---|
| Valuuta | ITMLine.CurrencyCode | Nvarchar(3) | Nr | Nr |
| Netosumma | ITMLine.LineAmountMST | Numbriline(32, 6) | Nr | Nr |
| Saatmiskonteiner | ITMLine.ShipContainerId | Int | Nr | Nr |
| Ettevõte | ITMLine.ShipDataArea | Nvarchar(20) | **Jah** | Nr |
| Deklareeritud kogus | ITMLine.ShipDeclaredQty | Nvarchar(4) | Nr | Nr |
| Foolio | ITMLine.ShipFotelefoniId | Numbriline(32, 6) | Nr | Nr |
| Reis | ITMLine.ShipId | Nvarchar(20) | **Jah** | Nr |
| Kaubakood | ITMLine.ShipItemId | Nvarchar(20) | Nr | Nr |
| Mõõtmine | ITMLine.ShipMeasurement | Nvarchar(20) | Nr | Nr |
| Mõõtühik | ITMLine.ShipMeasurementUnit | Numbriline(32, 6) | Nr | Nr |
| Pakkide arv | ITMLine.ShipNoOfCartons | Int | Nr | Nr |
| Asukoht | ITMLine.ShipPosition | Numbriline(32, 6) | Nr | Nr |
| Kogus | ITMLine.ShipQty | Int | Nr | Nr |
| Üleviimisrea number | ITMLine.TransferLineNumber | Numbriline(32, 6) | **Jah** | Nr |
| Üleviimistellimuse number | ITMLine.TransRefId | Numbriline(32, 6) | **Jah** | Nr |
| Ühik | ITMLine.UnitId | Int | Nr | Nr |
| Helitugevus | ITMLine.Volume | Nvarchar(10) | Nr | Nr |
| Kaal | ITMLine.kaal | Numbriline(32, 6) | Nr | Nr |

### <a name="reference-table"></a>Viitetabel

Reisiread luuakse seose kaudu avatud sissetuleva tellimuse reaga. See rida võib olla ostutellimusel või olla üleviimistellimuse vastuvõtukanne. Reisirea `RefTableId` tabeli () väli määrab`ITMLine`, millise tüübiga rida on seotud, viitades tabelinumbrile. Kui konkreetsele tabelinumbrile viidatakse tabelis, kus andmed luuakse, tükeldatakse üksused nende väärtuste alusel.

Viitetabeli () ja kandetüübi (`RefTableId``TransType`) väärtused on kas väljaminev kulu osturea olemi või väljaminev kuluülekanderea üksuse valimine otse.

### <a name="validation"></a>Kinnitus

Reisi rida viitab otse reisikirjele, konteineri saatmiskirjele ja foolio kirjele. Kui osturea üksust (`ITMPurchaseLinesEntity`) või ülekanderea üksust (`ITMPurchaseLinesEntity`) kasutatakse eraldi üksustest, mida kasutatakse nende viitekirjete loomiseks, **peavad reisi ID** (`ShipId`), **saadetise** konteineri (`ShipContainerId`) **ja Foolio** (`ShipFolioId`) väärtused vastama vastavates tabelites olemasolevale kirjele. Vastasel juhul importimine nurjub.

Kui ühte reaüksust kasutatakse sama impordiseansi osana, peavad need teised üksused olema enne reisirea loomist. Vastasel juhul ei saa väärtusi edukalt kinnitada. Kui reisi või foolio numbri puhul kasutatakse kohatäitja väärtust, saab seost luua ainult siis, kui reisirea üksuses kasutatakse reisi või foolio numbri jaoks sama kohatäitja.

Kui ostutellimus või üleviimistellimuse rida on juba määratud olemasolevale reisireale, uut reisirida ei looda. Enne, kui tellimuse rea saab määrata uuele reisile, tuleb see praegusest reisist eemaldada.

### <a name="order-line-identification"></a>Tellimuserea ID

Reisi read otse viitekirje ID-le (), varude **dimensiooni ID-le** (`RefRecId`) ja laokande **ID-väärtustele**`InventDimId`.**·**`InventTransId` Neid väärtusi ei pea enam andmeüksuse kasutamisel kaasama. Selle asemel tuleb nüüd kaasata tellimuserea number. Tellimuserea number ja tellimuse kood võimaldavad kõiki neid viiteväärtusi tuvastada.

### <a name="voyage-line-quantity"></a>Reisirea kogus

Kuna reisi rida on otseselt seotud tellimuse reaga, **nõuab** üksust kasutades sisestatud koguse (`ShipQty`) väärtus, et väärtused ühtiksid. Kinnitamine toimub kas ostutellimuse või üleviimisrea koguse suhtes. Kui kinnitamine nurjub, siis kirjet ei töödelda.

### <a name="calculated-fields"></a>Arvutatud väljad

Väljad **Kaal** **ja** Maht aktsepteerivad väärtusi, mis võetakse vastu andmeüksuse kaudu. Kui ühtegi väärtust ei ole antud, kasutatakse nende väljade uuendamiseks süsteemiväärtusi, kui süsteemiväärtused on saadaval. Omahinna puhul arvutatakse väärtused järgmiselt:

- *Kaalu* = *×* *kauba brutokaal*
- *Mahu* = *koguse* × (*kauba kogumaht* × kauba *kogukõrgus* × kauba *kogulaius*)

## <a name="sequencing"></a>Järjestus

Tabelite vaheliste sõltuvuste tõttu tuleb luua esmalt reisikirje. Reisi rida saab luua ainult pärast reisi, konteineri saatmist ja fool konteineri loomist.

Ilma kinnitamishoiatusteta reisi loomiseks peab süsteem töötlema üksused järgmises järjekorras:

1. Reisid (`ITMTableEntity`)
1. Konteinerite lähetamine (`ITMContainersEntity`)
1. Foolalane (`ITMFolioTableEntity`)
1. Reisi read (`ITMPurchaseLinesEntity` või `ITMTransferLinesEntity`)
