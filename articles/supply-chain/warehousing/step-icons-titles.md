---
title: Přiřaďte ikony kroků a názvy pro mobilní aplikaci Warehouse Management
description: Toto téma popisuje, jak přiřadit ikony a názvy kroků pro nové nebo přizpůsobené toky úloh pro mobilní aplikaci Warehouse Management.
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a74847b50512d2f712e5a9a5125e520afc732591
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344484"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a>Přiřaďte ikony kroků a názvy pro mobilní aplikaci Warehouse Management

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak přiřadit ikony a názvy kroků pro nové nebo přizpůsobené toky úloh pro mobilní aplikaci Warehouse Management.

Následující ilustrace ukazují, jak se ikony kroků a názvy zobrazují v mobilní aplikaci Warehouse Management.

![Příklad ikony kroku a názvu kroku v mobilní aplikaci Warehouse Management.](media/step-icon-example.png "Příklad ikony kroku a názvu kroku v mobilní aplikaci Warehouse Management")

## <a name="turn-on-this-feature-in-your-system"></a>Zapnutí funkce ve vašem systému

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Uživatelská nastavení, ikony a názvy kroků pro novou aplikaci skladu*

## <a name="standard-step-ids-classes-and-icons"></a>Standardní ID kroku, třídy a ikony

Každý krok v toku úlohy je identifikován ID kroku a každé ID kroku má odpovídající třídu kroku. Ikona a název kroku jsou specifikovány v každé třídě kroků.

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a>ID kroku a třídy kroků

V následující tabulce je uvedeno každé ID kroku, které je aktuálně k dispozici, a jeho odpovídající třída kroku. Název kroku primárního vstupního pole se používá jako ID kroku.

Příklad, který ukazuje, jak se tyto ID a třídy kroků používají, najdete v implementaci metody `WHSMobileAppStepInfoBuilder.stepId()` v [Příklad: Přiřaďte ikony kroků a názvy pro vlastní tok](#example) dále v tomto tématu.

| ID kroku | Třída kroků |
|-|-|
| BatchDisposition | WHSMobileAppStepBatchDisposition |
| Dopravce | WHSMobileAppStepCarrier |
| CatchWeight | WHSMobileAppStepCatchWeight |
| CatchWeightQtyOutboundWeight | WHSMobileAppStepCatchWeight |
| CatchWeightTag | WHSMobileAppStepCatchWeightTag |
| CatchWeightTagWeight | WHSMobileAppStepCatchWeightTagWeight |
| ChangeWarehouseSuccess | WHSMobileAppStepChangeWarehouseSuccess |
| CheckDigit | WHSMobileAppStepCheckDigit |
| ClusterId | WHSMobileAppStepClusterId |
| ClusterPickQtyVerification | WHSMobileAppStepQtyVerification |
| ClusterPosition | WHSMobileAppStepClusterPosition |
| ConfigId | WHSMobileAppStepConfigId |
| Potvrzení | WHSMobileAppStepConfirmation |
| ConsolidateFromLicensePlateId | WHSMobileAppStepConsolidateFromLicensePlateId |
| ConsolidateLPConfirmation | WHSMobileAppStepConsolidateLPConfirmation |
| ConsolidateToLicensePlateId | WHSMobileAppStepConsolidateToLicensePlateId |
| ContainerType | WHSMobileAppStepContainerType |
| CountingReasonCode | WHSMobileAppStepCountingReasonCode |
| CycleCountingAddLPOrFinish | WHSMobileAppStepCycleCountingAddLPOrFinish |
| CycleCountQty1 | WHSMobileAppStepCycleCountQty |
| CycleCountQty2 | WHSMobileAppStepCycleCountQty |
| CycleCountQty3 | WHSMobileAppStepCycleCountQty |
| CycleCountQty4 | WHSMobileAppStepCycleCountQty |
| Dispozice | WHSMobileAppStepDisposition |
| DriverCheckInConfirmation | WHSMobileAppStepDriverCheckInConfirmation |
| DriverCheckInId | WHSMobileAppStepDriverCheckInId |
| DriverCheckOutConfirmation | WHSMobileAppStepDriverCheckOutConfirmation |
| DriverCheckOutId | WHSMobileAppStepDriverCheckOutId |
| ExpDate | WHSMobileAppStepExpDate |
| FromBatchDisposition | WHSMobileAppStepFromBatchDisposition |
| FromInventoryStatus | WHSMobileAppStepInventoryStatusFrom |
| FullQty | WHSMobileAppStepFullQty |
| InboundPut | WHSMobileAppStepInboundPut |
| InventBatchId | WHSMobileAppStepBatch |
| InventColorId | WHSMobileAppStepInventColorId |
| InventLocation | WHSMobileAppStepInventLocation |
| InventLocationId | WHSMobileAppStepWarehouse |
| InventSerialId | WHSMobileAppStepInventSerialId |
| InventSizeId | WHSMobileAppStepInventSizeId |
| InventStatusId | WHSMobileAppStepInventStatus |
| InventStyleId | WHSMobileAppStepInventStyleId |
| InventVersionId | WHSMobileAppStepInventVersionId |
| ItemId | WHSMobileAppStepItem |
| ITMContainerID | ITMMobileAppStepContainerId |
| ITMShipmentID | ITMMobileAppStepShipmentId |
| KanbanCardId | WHSMobileAppStepKanbanCard |
| KanbanCardToEmpty | WHSMobileAppStepKanbanCardToEmpty |
| KanbanOrCardId | WHSMobileAppStepKanbanCard |
| LicensePlateId | WHSMobileAppStepLicensePlate |
| LoadId | WHSMobileAppStepLoadId |
| LocationLicensePlatePosition | WHSMobileAppStepLocationLicensePlatePosition |
| LocOrLP | WHSMobileAppStepLocOrLP |
| LocOrLP_From | WHSMobileAppStepLocOrLPFrom |
| LocOrLP_To | WHSMobileAppStepLocOrLPTo |
| LocOrLPCheck | WHSMobileAppStepLocOrLPCheck |
| LocVerification | WHSMobileAppStepLocVerification |
| LPAdjustIn | WHSMobileAppStepLPAdjustIn |
| LPBreakChildLP | WHSMobileAppStepLPBreakChildLP |
| LPBreakParentLP | WHSMobileAppStepLPBreakParentLP |
| LPBuildChildLP | WHSMobileAppStepLPBuildChildLP |
| LPBuildParentLP | WHSMobileAppStepLPBuildParentLP |
| LPVerification | WHSMobileAppStepLPVerification |
| MergeContainerId | WHSMobileAppStepMergeContainerId |
| MixedLPLineNum | WHSMobileAppStepMixedLPLineNum |
| MobileDeviceQueueMessageCollectionIdentifierId | WHSMobileAppStepSelectOrder |
| MovementConfirmCancel | WHSMobileAppStepMovementConfirmCancel |
| NewCaptureWeight | WHSMobileAppStepCatchWeight |
| NewQty | WHSMobileAppStepNewQty |
| OutboundCatchWeightTag | WHSMobileAppStepCatchWeightTag |
| OutboundPut | WHSMobileAppStepOutboundPut |
| Odchozí hmotnost | WHSMobileAppStepCatchWeight |
| OverridePutNewLocation | WHSMobileAppStepOverridePutNewLocation |
| Potvrzení PieceByPiece | WHSMobileAppStepQtyVerification |
| POLineNum | WHSMobileAppStepPOLineNum |
| Číslo nákupní objednávky | WHSMobileAppStepPONum |
| PositionFull | WHSMobileAppStepPositionFull |
| PositionFullQty | WHSMobileAppStepPositionFullQty |
| Obsah | WHSMobileAppStepPotency |
| PrinterName | WHSMobileAppStepPrinterName |
| ProdId | WHSMobileAppStepProdId |
| ProdLastPalletConfirmation | WHSMobileAppStepProdLastPalletConfirmation |
| ProductConfirmation | WHSMobileAppStepProductConfirmation |
| ProductionScrapConfirmation | WHSMobileAppStepProductionScrapConfirmation |
| Vložit | WHSMobileAppStepPut |
| PutawayClusterId | WHSMobileAppStepPutawayClusterId |
| Množství | WHSMobileAppStepQty |
| QtyAdjust | WHSMobileAppStepQtyAdjust |
| QtyShort | WHSMobileAppStepQtyShort |
| QtyToConsume | WHSMobileAppStepQtyToConsume |
| QtyToPick | WHSMobileAppStepQtyToPick |
| QtyToPut | WHSMobileAppStepQtyToPut |
| QtyToScrap | WHSMobileAppStepQtyToScrap |
| QtyVerification | WHSMobileAppStepQtyVerification |
| QtyWithScanningLimit | WHSMobileAppStepQtyAdjust |
| ReasonString | WHSMobileAppStepReasonString |
| RecvLocationId | WHSMobileAppStepRecvLocationId |
| RemoveContainerId | WHSMobileAppStepRemoveContainerId |
| ReprintLabelConfirmation | WHSMobileAppStepReprintLabelConfirmation |
| RMANum | WHSMobileAppStepRMANum |
| ShortPickReason | WHSMobileAppStepShortPickReason |
| SortConOrLP | WHSMobileAppStepSortConOrLP |
| SortLicensePlateId | WHSMobileAppStepSortLicensePlateId |
| SortPositionId | WHSMobileAppStepSortPositionId |
| SortVerification | WHSMobileAppStepSortVerification |
| StartLocationId | WHSMobileAppStepStartLocationId |
| StartProdOrderConfirmation | WHSMobileAppStepStartProdOrderConfirmation |
| TargetLicensePlateId | WHSMobileAppStepTargetLicensePlateId |
| TOLineNum | WHSMobileAppStepTOLineNum |
| ToLocation | WHSMobileAppStepToLocation |
| Do čísla | WHSMobileAppStepTONum |
| ToWarehouse | WHSMobileAppStepWarehouseTo |
| TransportLoadId | WHSMobileAppStepTransportLoadId |
| WaveLabelId | WHSMobileAppStepWaveLabelId |
| WaveLblQty | WHSMobileAppStepWaveLblQty |
| Váha | WHSMobileAppStepWeight |
| WeightToConsume | WHSMobileAppStepWeightToConsume |
| WHSAdjustmentType | WHSMobileAppStepWHSAdjustmentType |
| WHSReceivingException | WHSMobileAppStepWHSReceivingException |
| WHSWorkException | WHSMobileAppStepWHSWorkException |
| WHSWorkLicensePlateId | WHSMobileAppStepWorkLicensePlateId |
| WMSLocationId | WHSMobileAppStepLocation |
| WorkId | WHSMobileAppStepWorkId |
| WorkIdToCancel | WHSMobileAppStepWorkIdToCancel |
| WorkLPIdPutawayCluster | WHSMobileAppStepWorkLPIdPutawayCluster |
| WorkPoolId | WHSMobileAppStepWorkPoolId |
| ZoneId | WHSMobileAppStepZoneId |

### <a name="available-step-icons"></a><a name="step-icons"></a>Ikony dostupných kroků

Systém obsahuje kolekci ikon standardních kroků, které můžete také použít pro vlastní kroky. Momentálně nemůžete nahrát vlastní ikony kroků. Proto musíte vždy vybrat jednu ze standardních ikon kroků.

Následující tabulka ukazuje každou ikonu standardního kroku, která je aktuálně k dispozici, a její název.

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Ikona O kroku"><br>O prognóze</td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Přidat registrační značku nebo ikonu kroku položky"><br>AddLpOrItem</td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Ikona kroku dávkové dispozice"><br>BatchDisposition</td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Ikona kroku dopravce"><br>Dopravce</td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Ikona kroku značky skutečné hmotnosti"><br>CatchWeightTag</td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Ikona kroku hmotnosti značky skutečné hmotnosti"><br>CatchWeightTagWeight</td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Ikona kroku kontrolní číslice"><br>CheckDigit</td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="Ikona kroku ID přihlášení nebo odhlášení"><br>CheckInOutId</td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Ikona kroku podřízené registrační značky"><br>ChildLP</td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Ikona kroku ID clusteru"><br>ClusterId</td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Ikona kroku pozice clusteru"><br>ClusterPosition</td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Ikona kroku ID konfigurace"><br>ConfigId</td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Ikona kroku nakonfigurovaného pole"><br>ConfiguredField</td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Ikona kroku kon. nebo reg. zn."><br>ConOrLP</td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Ikona kroku Konsolidace z ID registrační značky"><br>ConsolidateFromLicensePlateID</td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Ikona kroku Konsolidace do ID registrační značky"><br>ConsolidateToLicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Ikona kroku typu kontejneru"><br>ContainerType</td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Ikona kroku inventura"><br>Inventura</td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Ikona kroku kód důvodu inventury"><br>CountingReasonCode</td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Ikona kroku kódu země původu"><br>CountryOfOrigin</td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Ikona kroku dispozice"><br>Dispozice</td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Ikona kroku hotovo"><br>Hotovo</td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Ikona kroku potvrzení přihlášení ovladače"><br>DriverCheckInConfirmation</td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Ikona kroku ID přihlášení ovladače"><br>DriverCheckInId</td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Ikona kroku ID odhlášení ovladače"><br>DriverCheckOutId</td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Ikona kroku data vypršení platnosti"><br>ExpDate</td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Ikona kroku pole"><br>Pole</td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="Ikona kroku z dávkové dispozice"><br>FromBatchDisposition</td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="Ikona kroku ze stavu inventáře"><br>FromInventoryStatus</td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="Ikona kroku atributu ID"><br>IdAttribute</td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Ikona kroku ID dávky zásob"><br>InventBatchID</td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Ikona kroku ID barvy zásob"><br>InventColorID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Ikona kroku umístění zásob"><br>InventLocation</td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Ikona kroku ID sériových zásob"><br>InventSerialID</td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Ikona kroku ID velikosti zásob"><br>InventSizeID</td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Ikona kroku ID stavu zásob"><br>InventStatusID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Ikona kroku ID stylu zásob"><br>InventStyleID</td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Ikona kroku ID verze zásob"><br>InventVersionID</td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Ikona kroku ID položky"><br>ItemID</td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="Ikona kroku ID kontejneru ITM"><br>ITMContainerID</td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="Ikona kroku ID zásilky ITM"><br>ITMShipmentID</td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="Ikona kroku ID karty Kanban"><br>KanbanCardID</td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="Ikona kroku ID kanbanu nebo karty"><br>KanbanOrCardID</td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Ikona kroku ID registrační značky"><br>LicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Ikona kroku ID nákladu"><br>LoadId</td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Ikona ktoku umístění registrační značky místa"><br>LocationLicensePlatePosition</td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Ikona kroku umístění nebo registrační značky"><br>LocOrLP</td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Ikona kroku kontrola umístění nebo registrační značky"><br>LocOrLPCheck</td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Ikona kroku z umístění nebo registrační značky"><br>LocOrLPFrom</td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Ikona kroku do umístění nebo registrační značky"><br>LocOrLPTo</td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Ikona dokončeného kroku dlouhého procesu"><br>LongProcessCompleted</td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="Ikona kroku přešení reg. zn. nadřazené reg. zn."><br>LPBreakParentLP</td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Ikona kroku ID sloučení kontejneru"><br>MergeContainerId</td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Ikona kroku číslo řádku smíšené registrační značky"><br>MixedLPLineNum</td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Ikona kroku odchozí hmotnosti"><br>OutboundWeight</td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Ikona kroku vlastníka"><br>Vlastník</td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Ikona kroku nadřazené registrační značky"><br>ParentLP</td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Potvrďte prosím ikonu kroku"><br>PleaseConfirm</td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Ikona kroku čísla řádku nákupní objednávky"><br>POLineNum</td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Ikona kroku čísla nákupní objednávky"><br>Číslo nákupní objednávky</td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Ikona kroku plné pozice"><br>PositionFull</td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Ikona kroku koncentrace"><br>Obsah</td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Ikona kroku názvu tiskárny"><br>PrinterName</td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Ikona kroku ID prod."><br>ProdId</td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Ikona kroku potvrzení produktu"><br>ProductConfirmation</td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Ikona kroku vložit"><br>Vložit</td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Ikona kroku IDseskupení vyskladnění"><br>PutawayClusterId</td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Ikona kroku množství"><br>Množství</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Ikona kroku úpravy množství"><br>QtyAdjustIn</td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Ikona krátkého kroku množství"><br>QtyShort</td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Ikona kroku množství ke spotřebě"><br>QtyToConsume</td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Ikona kroku množství k vložení"><br>QtyToPut</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Ikona kroku množství k likvidaci"><br>QtyToScrap</td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Ikona kroku potvrzení množství"><br>QuantityConfirmation</td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Ikona kroku Nahlásit dokončení úlohy"><br>RAFEndJob</td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Ikona kroku ID místa příjmu"><br>RecvLocationID</td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Ikona kroku ID odebrání kontejneru"><br>RemoveContainerID</td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="Ikona kroku čísla RMA"><br>RMANum</td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Ikona kroku výběr objednávky"><br>SelectOrder</td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Ikona kroku důvod krátkého výdeje"><br>ShortPickReason</td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Ikona kroku ID pozice třídění"><br>SortPositionId</td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Ikona kroku ID cílové registrační značky"><br>TargetLicensePlateId</td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Ikona ktoku čísla řádku příjmu"><br>ToLineNum</td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Ikona kroku umístění příjmu"><br>ToLocation</td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Ikona kroku čísla příjmu"><br>ToNum</td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Ikona kroku skladu příjmu"><br>ToWarehouse</td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Ikona kroku ID dopravy nákladu"><br>TransportLoadId</td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Ikona kroku ID dávky dodavatele"><br>VendBatchId</td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Ikona kroku ID štítku vlny"><br>WaveLabelId</td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Ikona kroku množství štítku vlny"><br>WaveLblQty</td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Ikona kroku hmotnosti"><br>Váha</td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Ikona kroku hmostnosti ke spotřebě"><br>WeightToConsume</td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="Ikona kroku typu úpravy WHS"><br>WHSAdjustmentType</td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="Ikona kroku výjimky přijetí WHS"><br>WHSReceivingException</td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="Ikona kroku ID umístění WMS"><br>WMSLocationID</td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="Ikona kroku ID práce"><br>WorkId</td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="Ikona kroku ID práce ke zrušení"><br>WorkIdToCancel</td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="Ikona kroku ID registrační značky práce"><br>WorkLicensePlateId</td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="Ikona kroku ID seskupení výdeje registrační značky práce"><br>WorkLPIDPutawayCluster</td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="Ikona kroku ID fondu práce"><br>WorkPoolID</td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Ikona kroku ID zóny"><br>ZoneID</td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a>Příklad: Přiřaďte ikony kroků a názvy pro vlastní tok

Tento příklad vysvětluje, jak nastavit ikony a názvy kroků pro vlastní tok úkolů. Scénář je postaven na příkladu vlastního toku úloh, který je podrobněji představen a prozkoumán v následujícím příspěvku na blogu: [Přizpůsobení mobilní aplikace Warehousing](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app). Tok úloh funguje následujícím způsobem:

1. Aplikace zobrazuje stránku, která pracovníka vyzve k poskytnutí ID kontejneru (například skenováním čárového kódu).
1. Pokud je ID kontejneru platné, aplikace otevře novou stránku, která pracovníka vyzve k zadání hmotnosti. (Pokud ID kontejneru není platné, pracovník se vrátí na první stránku.)
1. Když pracovník zadá platnou hmotnost, systém váhu uloží a vrátí pracovníka na první stránku.

Následující obrázek znázorňuje tento tok úloh.

![Vývojový diagram úkolu.](media/step-icons-example-task-flow.png "Vývojový diagram úkolu")

### <a name="create-a-step-class-for-the-container-input-page"></a>Vytvořte třídu kroků pro vstupní stránku kontejneru

Na vstupní stránce kontejneru může pracovník skenovat nebo zadat ID kontejneru.

![Stránka vstupu do kontejneru.](media/step-icons-example-container-input.png "Stránka vstupu do kontejneru")

Na vstupní stránce kontejneru je název ovládacího prvku vstupního pole `ContainerId`. Protože tento název ovládacího prvku není v [seznamu ID kroků](#step-ids-classes), nenajdete existující krok, který je na něm založen. Proto musíte vytvořit třídu kroku, která představuje krok. Následuje příklad.

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

Identifikátor ikony kroku je uložen v členu třídy `defaultStepIcon` a název kroku je uložen v členu třídy `defaultStepTitle`.

Chcete-li přiřadit ikonu kroku, nastavte `defaultStepIcon` na jedno z ID ikon, které jsou uvedeny v sekci [Dostupné ikony kroků](#step-icons) dříve v tomto tématu.

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a>Pro zadání hmotnosti použijte standardní nebo vlastní ikonu a název kroku

Stránka pro zadání hmotnosti umožňuje pracovníkovi zadat hmotnost.

![Stránka pro zadání hmotnosti.](media/step-icons-example-weight-input.png "Stránka pro zadání hmotnosti")

Na stránce pro zadávání hmotnosti je název ovládacího prvku vstupního pole `Weight`, které je v [seznamu ID kroků](#step-ids-classes). Pokud tedy ikona a název kroku, které jsou definovány v třídě `WHSMobileAppStepWeight`, jsou pro vás přijatelné, pro tento krok nemusíte nic měnit.

Pokud však v tomto kroku dáváte přednost použití jiné ikony nebo názvu, můžete přepsat buď metodu `stepId()` nebo `stepInfo()` ve třídě tvůrce. Každý tok úloh má svůj vlastní nástroj pro vytváření informací o krocích.

#### <a name="override-the-stepid-method"></a>Přepsat metodu stepId ()

Následující příklad ukazuje jeden způsob, kterým můžete upravit třídu tvůrce přepsáním metody `stepId()`.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

Potom vytvoříte třídu kroků pro krok `NewWeight`. Kód by měl vypadat jako kód pro příklad `ContainerId`, který byl uveden dříve v tomto tématu.

#### <a name="override-the-stepinfo-method"></a>Přepsat metodu stepInfo()

Následující příklad ukazuje jeden způsob, kterým můžete upravit třídu tvůrce přepsáním metody `stepInfo()`.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

Potom vytvoříte objekt `WHSMobileAppStepInfo` a přímo nastavíte ikonu a/nebo název.

## <a name="additional-resources"></a>Další prostředky

- [Instalace a připojení mobilní aplikace Řízení skladu](install-configure-warehouse-management-app.md)
- [Uživatelská nastavení mobilního zařízení](mobile-device-user-settings.md)
